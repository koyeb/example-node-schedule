<div align="center">
  <a href="https://koyeb.com">
    <img src="https://www.koyeb.com/static/images/icons/koyeb.svg" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Koyeb Serverless Platform</h3>
  <p align="center">
    Deploy a `node-schedule` application on Koyeb
    <br />
    <a href="https://koyeb.com">Learn more about Koyeb</a>
    ·
    <a href="https://koyeb.com/docs">Explore the documentation</a>
    ·
    <a href="https://koyeb.com/tutorials">Discover our tutorials</a>
  </p>
</div>


## About Koyeb and the `node-schedule` example application

Koyeb is a developer-friendly serverless platform to deploy apps globally. No-ops, servers, or infrastructure management.

This repository contains is designed to show how a `node-schedule` application can be deployed to Koyeb.  The demo application aggregates the top ten most-commented on Hacker news posts and sends them to a designated email address using a cron-like schedule.

You can follow the [associated tutorial]() to learn more about the application and how it works.

## Getting Started

Follow the steps below to deploy and run the Nuxt application on your Koyeb account.

### Requirements

You need a Koyeb account to successfully deploy and run this application. If you don't already have an account, you can sign-up for free [here](https://app.koyeb.com/auth/signup).

You also need a [Mailgun account](https://www.mailgun.com/) to send the email with the aggregated links.  From your Mailgun account, you need to configure an [authorized recipient email address](https://help.mailgun.com/hc/en-us/articles/217531258-Authorized-Recipients) and then retrieve the following details associated with your account:

* `API_KEY`: The Mailgun private API key associated for your account.
* `DOMAIN`: The sandbox domain for your account.
* `EMAIL`: The `postmaster@` email address associated with your Mailgun domain.
* `RECIPIENT_EMAIL`: The authorized email address that you configured to receive email.

### Deploy using the Koyeb button

The fastest way to deploy the Nuxt application is to click the **Deploy to Koyeb** button below.

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?name=node-schedule-on-koyeb&service_type=worker&type=git&repository=koyeb/example-node-schedule&branch=main&env[API_KEY]=REPLACE_ME&env[DOMAIN]=REPLACE_ME&env[EMAIL]=REPLACE_ME&env[RECIPIENT_EMAIL]=REPLACE_ME&env[SCHEDULE]=REPLACE_ME)

Clicking on this button brings you to the Koyeb App creation page with most of the settings pre-configured to launch this application.  You will need to replace the values for the following variables:

| Environment variable | Required? | Description |
|---------|----------|-----------|
| `API_KEY` | yes | Mailgun account private API key |
| `DOMAIN` | yes | Mailgun account sandbox domain |
| `EMAIL` | yes | Mailgun domain's `postmaster@` email address |
| `RECIPIENT_EMAIL` | yes | The Mailgun authorized recipient email address |
| `SCHEDULE` | no | An optional [`node-schedule` cron schedule](https://github.com/node-schedule/node-schedule#cron-style-scheduling) (default: every 2 minutes) |

_To modify this application example, you will need to fork this repository. Checkout the [fork and deploy](#fork-and-deploy-to-koyeb) instructions._

### Fork and deploy to Koyeb

If you want to customize and enhance this application, you need to fork this repository.

If you used the **Deploy to Koyeb** button, you can simply link your service to your forked repository to be able to push changes.
Alternatively, you can manually create the application as described below.

On the [Koyeb Control Panel](//app.koyeb.com/), click the **Create App** button to go to the App creation page.

1. Click **Create App** in the Koyeb control panel.
2. Select **GitHub** as the deployment option.
3. Choose the GitHub **repository** and **branch** containing your application code.
4. Name your service, for example `node-schedule-service`.
5. Name the App, for example `example-node-schedule`.
6. Click **Advanced** to display additional settings and click the **Add Variable** button to fill in the environment variables outlined above.
6. Click the **Deploy** button.

Your `node-schedule` application will be deployed to Koyeb.  You can follow the build process as the repository is cloned, built, and deployed.  Once the deployment is complete, it will aggregate Hacker News post data and send it to the configured email address according to the schedule provided.

## Contributing

If you have any questions, ideas or suggestions regarding this application sample, feel free to open an [issue](//github.com/koyeb/example-node-schedule/issues) or fork this repository and open a [pull request](//github.com/koyeb/example-node-schedule/pulls).

## Contact

[Koyeb](https://www.koyeb.com) - [@gokoyeb](https://twitter.com/gokoyeb) - [Slack](http://slack.koyeb.com/)
