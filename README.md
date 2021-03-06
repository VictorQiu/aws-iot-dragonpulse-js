#  aws-iot-dragonpulse-js

### Arrow DragonPulse

The DragonPulse project collects general system, disk, network, and process
information from a DragonBoard&trade;.  The collected information is
published to an MQTT topic of Amazon IoT where a Lambda function stores
it in a DynamoDB table.  A dashboard whose static web pages are stored
in s3 accesses endpoints hosted on the API Gateway display the collected
information.

# Getting Started
Please have the following information available:

* Amazon Account Number - (https://console.aws.amazon.com/billing/home#/account)
* Stage - Amazon API Gateway deploys to a stage, so it must be specified, By default 'dev' is used. (https://arrowelectronics.github.io/aws-iot-dragonpulse-js/admin/api.html)
* S3 Identifier - S3 is used to host the client, it would be best to give it something unique. By default the last 5 characters of the machine id is used. (https://arrowelectronics.github.io/aws-iot-dragonpulse-js/admin/dashboard.html)

After the setup has completed, there are a few urls that are provided. Please make note of them: AWS API Gateway, and Dashboard

1. Navigate to the root of Arrow DragonPulse `/home/linaro/arrow/aws-iot-dragonpulse-js`
2. Run the setup script
```sh
    $ cd scripts
    $ ./setup.sh
```
3. Start the Client
```sh
    $ cd DragonBoard
    $ sudo npm start
```
4. Visit the DragonPulse Dashboard (https://arrowelectronics.github.io/aws-iot-dragonpulse-js/execution/dashboard.html)

## Uninstall and Cleanup

All the settings from the install are stored `scripts/.settings`
```sh
    $ cd scripts
    $ ./uninstall.sh 
```

For more information on the DragonPulse project, including how it is
deployed and configured, visit the
<a href="https://arrowelectronics.github.io/aws-iot-dragonpulse-js/" target="_blank">DragonPulse Project</a>

# License
This SDK is distributed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0), see LICENSE.txt and NOTICE.txt for more information.
