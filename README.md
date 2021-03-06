# ShelterTech.org Non-Profit Informational Site

## Onboarding information
https://sheltertech.quip.com/oSdpAVfvDbPq/ShelterTech-AskDarcel-Developer-Engineer

## Requirements for Development
* node `^4.5.0`
* yarn `^0.17.0` or npm `^3.0.0`

```bash
$ yarn install     # Install project dependencies
$ yarn start       # Compile and launch (same as `npm start`)
$ yarn deploy:prod # Build deployable production build to /dist
```

## Deploy to Live Environment

We use an AWS S3 bucket to host this website. These are the steps to deploy changes to production.

### Preconditions

#### Homebrew

How to install: https://brew.sh/

#### Access to the Sheltertech AWS account

Contact the Technical Team if you need this, you will need to configure `aws` your first time.

Install the aws-cli tools. For OSX:
```bash
$ brew install awscli
```
Then to configure it run:
```bash
$ aws configure
```
You'll need to input these values.
```
AWS Key ID     : {{KEY_ID}}

AWS Secret Key : {{SECRET_KEY}}

Default Region : us-east-1
```
### Deployment to Staging
```bash
$ yarn update:staging
```
### Deployment to Production
```bash
$ yarn update:prod
```
