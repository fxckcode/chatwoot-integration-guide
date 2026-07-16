## Chatwoot database migration

Follow along If you started out with a bundled install of postgres, redis and chatwoot in a single instance and now wants to migrate to managed database service.

In this guide, we assume you want to migrate to AWS RDS. This guide should be equally applicable to any other managed database service or even migrating data between different Chatwoot installations.

### Step 1: Stop Chatwoot service

Stop Chatwoot service to stop database activity.

```shellscript
sudo systemctl stop chatwoot.target
```

### Step 2: Back up the database

Back up the database using `pg_dump` tool.

```shellscript
pg_dump -Fc --no-acl --no-owner  -U postgres chatwoot_production > /tmp/cw.dump
```

### Step 3: Create RDS instance

Create an RDS Postgres instance in your AWS account. Refer to the [AWS documentation](https://aws.amazon.com/getting-started/hands-on/create-connect-postgresql-db/).

### Step 4: Verify connectivity

Verify connectivity to the new RDS instance from your Chatwoot installation.

```shellscript
psql -h <hostname> -u <username> -d postgres
```

### Step 5: Restore the database

Restore the database from the backup file.

```shellscript
pg_restore --verbose --clean --no-acl --no-owner --create -U postgres -d postgres /tmp/cw.dump
```

### Step 6: Update environment variables

Modify the Postgres related environment variables to use the new RDS credentials.

```shellscript
sudo -i -u chatwoot
cd chatwoot
vi .env
```

### Step 7: Start Chatwoot service

Start the Chatwoot service.

```shellscript
sudo systemctl start chatwoot.target
```

If you are getting the Chatwoot onboarding screen again on visiting your self-hosted Chatwoot URL, login to the rails console and run the following:

```shellscript
sudo cwctl --console
::Redis::Alfred.delete(::Redis::Alfred::CHATWOOT_INSTALLATION_ONBOARDING)
```