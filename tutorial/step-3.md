# 3. Deploy the code to Amazon Lambda

You will now need to upload this code to Lambda.

Go to https://console.aws.amazon.com/lambda/home and click ‘Create a Lambda function’. Make sure you are in the eu-west-1, us-east-1, or us-west-2 regions.


For the blueprint select ‘Blank Function’. For the trigger, click the gray dashed box and select ‘Alexa Skills Kit’. Name the function whatever you want and set the runtime to Node.js 6.10.

For Code Entry Type click the dropdown and select ‘Upload a .ZIP file’, then click on the Upload button that appears and then navigate to and select the bitscoop-alexa-demo-<version>.zip file. The Handler should be ‘index.handler’.


You will need to add several Environment Variables, with the number depending on how many services you wish to run. You will always need to add the following variables:

- BITSCOOP_API_KEY (obtainable at https://bitscoop.com/keys)

- ALEXA_APP_ID (you will fill this in later)

If you are getting data from GitHub, you will need to add these:

- GITHUB_MAP_ID (The ID of the BitScoop API map you created for GitHub)

- GITHUB_USER (the username that owns the repo you’re interested in)

- GITHUB_REPO (the name of the repo you’re interested in)

If you are getting data from Google Analytics, you will need to add
these:

- GOOGLE_MAP_ID (The ID of the BitScoop API map you created for Google)
- GOOGLE_GA_VIEW_ID (the ID of the View you are monitoring)

- GOOGLE_CONNECTION_ID (the ID of the BitScoop Connection you created to the Google Analytics API Map)

If you are getting data from StatusCake, you will need to add these:

- STATUSCAKE_MAP_ID (The ID of the BitScoop API map you created for StatusCake)

- STATUSCAKE_TEST_ID (the ID of the Test you are monitoring)

If you are getting data from Postman, you will need to add these:

- POSTMAN_MAP_ID (The ID of the BitScoop API map you created for Postman)

- POSTMAN_MONITOR_ID (the ID of the Monitor you are running)

For the Role, create a new custom role and use the default policy for lambda_basic_execution, which should be

```
{
  "Version": "2012–10–17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
           "logs:CreateLogGroup",
           "logs:CreateLogStream",
           "logs:PutLogEvents"
        ],
      "Resource": "arn:aws:logs:*:*:*"
    }
  ]
}```

Open the Advanced Settings accordion. You’ll probably want to set the Timeout to 10 seconds. Make sure that VPC is set to ‘No VPC’. Hit next and you’ll be taken to a review screen, and then select ‘Create Function’ at the very bottom of the page.

If you did not set a trigger earlier, go to the details for the function and click the tab ‘Triggers’. Click ‘Add Trigger’, click on the dashed gray box, then select ‘Alexa Skills Kit’ and then click ‘Submit’.

In the upper-right-hand corner of the screen, just below the AWS toolbar, you should see:

`ARN — arn:aws:lambda:<region>:<id>:function:<function name>`


You will need this ARN for the next step, so copy it somewhere or do the following step in another tab.
