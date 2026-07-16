This guide will help you to deploy Chatwoot to production!

## Architecture

Running Chatwoot in production requires the following set of services.

- Chatwoot web servers
- Chatwoot workers
- PostgreSQL Database
- Redis Database
- Email service (SMTP servers / SendGrid / Mailgun etc)
- Object Storage (S3, Azure Storage, GCS, etc)
![architecture](https://mintcdn.com/chatwoot-447c5a93/0ZKii1AePO4f9gzo/self-hosted/images/architecture.png?w=2500&fit=max&auto=format&n=0ZKii1AePO4f9gzo&q=85&s=9abf04b86ef5b83f01e4284889c00912)

architecture

## Updating your Chatwoot installation

A new version of Chatwoot is released around the first Monday of every month. We also release minor versions when there is a need for hotfixes or security updates.

You can stay tuned to our [Roadmap](https://github.com/chatwoot/chatwoot/milestones) and [releases](https://github.com/chatwoot/chatwoot/releases) on GitHub. We recommend you to stay up to date with our releases to enjoy the latest features and security updates.

The deployment process for a newer version involves updating your app servers and workers with the latest code. Most updates would involve database migrations as well which can be executed through the following Rails command.

```shellscript
bundle exec rails db:migrate
```

The detailed instructions can be found in respective deployment guides.

## Available deployment options

If you want to self host Chatwoot, the recommended approach is to use one of the recommended one click installation options from the below list. If you are comfortable with Ruby on Rails applications, you can also make use of the other deployment options mentioned below.

### Cloud Providers

- **[AWS](https://developers.chatwoot.com/self-hosted/deployment/aws)**
- **[Azure](https://developers.chatwoot.com/self-hosted/deployment/azure)**
- **[DigitalOcean](https://developers.chatwoot.com/self-hosted/deployment/digitalocean)**
- **[Google Cloud](https://developers.chatwoot.com/self-hosted/deployment/gcp)**
- **[Heroku](https://developers.chatwoot.com/self-hosted/deployment/heroku)**