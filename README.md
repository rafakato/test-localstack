# Steps to reproduce
1) `npm install`
2) `npm run start:localstack` leave it running in the terminal and when it logs `Ready` continue to next step
3) `npm run deploy` in another terminal, if it thorws this error:
```sh
  Serverless plugin "serverless-localstack" not found. Make sure it's installed and listed in the "plugins" section of your serverless config file.
```
Then the [serverless-localstack](https://github.com/temyers/serverless-localstack) plugin is not properly installed. To fix this install the plugin without using NPM, like described [here](https://github.com/temyers/serverless-localstack#installation-without-npm).

## Current Scenario

After running the `deploy` command, the command finishes with error but without message, and in the localstack window it logs `AttributeError: 'NoneType' object has no attribute 'value'` error.