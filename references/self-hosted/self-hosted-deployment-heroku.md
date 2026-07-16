## Deploying on Heroku

Heroku has discontinued free dynos, postgres and redis. [Chatwoot will use basic/mini plans](https://blog.heroku.com/new-low-cost-plans) for all new Heroku deployments going forward.

Deploy Chatwoot on Heroku through the following steps:

1. Click on the [one click deploy button](https://heroku.com/deploy?template=https://github.com/chatwoot/chatwoot/tree/master) and deploy your app.
2. Go to the **Resources** tab in the Heroku app dashboard and ensure the worker dynos is turned on.
3. Head over to **Settings** tab in Heroku app dashboard and click **Reveal Config Vars**.
4. Configure the environment variables for [mailer](https://developers.chatwoot.com/self-hosted/configuration/environment-variables#configure-emails) and [storage](https://developers.chatwoot.com/self-hosted/deployment/storage/supported-providers) as per the [documentation](https://developers.chatwoot.com/self-hosted/configuration/environment-variables).
5. Head over to `yourapp.herokuapp.com` and enjoy using Chatwoot.

## Updating the deployment on Heroku

Whenever a new version is out for Chatwoot, you update your Heroku deployment through following steps:

1. In the **Deploy** tab, choose `GitHub` as the deployment option.
2. Connect Chatwoot repo to the app.
3. Head over to the manual deploy option, choose `master` branch and hit **Deploy**.

## Known Limitations

1. **Dyno Sleep**: If you are on a free tier and you don’t access the application for a while Heroku will put your dynos to sleep. You can fix this by upgrading the dynos to paid tier.
2. **Ephemeral Storage**: Heroku has an “ephemeral” hard disk. The files uploaded to Chatwoot would not persist after the application is restarted. By default, Chatwoot uses local disk as the upload destination. To overcome this problem, you will have to [configure a cloud storage](https://developers.chatwoot.com/self-hosted/deployment/storage/supported-providers).
3. **Build Version**: If the build version is shown as unknown on the settings page, enable the runtime dyno metadata feature. To enable, use:
	```shellscript
	heroku labs:enable runtime-dyno-metadata -a <app-name>
	```