# Legend of the Hidden Classroom

Metal Toad Hackathon

<img src="https://cf.geekdo-images.com/camo/27f6ea91e9272f4b5427ab3de34ba5683a54bf80/687474703a2f2f696d61676573332e77696b69612e6e6f636f6f6b69652e6e65742f5f5f636232303132303432393136353135372f67616d6573686f77732f696d616765732f662f66622f506172726f74732e6a7067" width="250" alt="Amazon Chime SDK Classroom Demo">

## Installation

#### Prerequisites
To deploy the classroom demo you will need:

- Node 10 or higher
- npm 6.11 or higher

And install aws and sam command line tools:

* [Install the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv1.html)
* [Install the AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

First deploy the stack:

```bash
script/deploy.js -r <region> -a <app name> -s <unique stack name> -b <unique bucket name>
```

At the end of the script you will see a URL to a download page. Save this link. To run the application locally in Electron run:

```bash
yarn dev
```

Before pushing your commit, ensure that the application works okay in production mode.

```bash
yarn cross-env DEBUG_PROD=true yarn start
```

## Troubleshooting

### I get "The application ... can't be opened" when opening the app

The default zipping tool on MacOS Catalina may incorrectly unzip the package. Download an alternative (such as "The Unarchiver"), and unzip the package by right clicking and selecting "Open as". You may also need to adjust your security & privacy settings if you get an "unidentified developer" message.
