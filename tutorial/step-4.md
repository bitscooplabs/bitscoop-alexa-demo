# 4. Set up the skill in the Amazon Alexa Skills Developer Portal

Go to https://developer.amazon.com/edw/home.html#/skills and click ‘Add a New Skill’.


Pick ‘Custom Interaction’ for the Skill Type, enter ‘Ops Buddy’ for Name and Interaction Name, and click Save. Click on Interaction Model on the left-hand side. Under Intent Schema enter:
```
{
  "intents": [
    {
      "intent": "AboutIntent"
    },
    {
      "intent": "StackIntent"
    }
  ]
}```

and under Sample Utterances enter:
```
StackIntent how's the stack doing

StackIntent how is the stack doing

StackIntent how is the stack doing today
```

You can add more utterances if you wish; the key thing is that they must start with ‘StackIntent’ to call the right Intent in the Lambda function. Click Save when you’re done.

Next click on Configuration. Service Endpoint Type should be ‘AWS Lambda ARN’, and the geographical region should be whichever is closest to you. Paste the ARN from the end of Step 3 into the text box for the region you selected. Make sure ‘account linking’ is set to No and click ‘Save’. Click on Test and enable test mode if you wish. Finally, go to Privacy and Compliance and select ‘No’ for the three radio selections, then Save.

If everything has gone right, your skill should be ready to go. The following sections explain how to test the Lambda function and the Alexa Skill.

# Testing the Lambda function

Click the ‘Actions’ dropdown next to ‘Test’ and select ‘Configure Test Event’. Select the template ‘Alexa Intent — Recipe’. Copy the Alexa Skill ID into ‘session.application.applicationId’ and ‘context.System.application.applicationId’, as well as changing ‘request.intent.name’ to ‘StackIntent’. Click Save and Test and the function should run.

# Testing the Alexa Skill

Go to the ‘Test’ tab in the Alexa skill and enable testing if you have not already done so. In ‘Enter Utterance’ insert an utterance that you defined in step 4. Click ‘Ask <Skill name>’ to make a test request.

Congratulations! You are done with your first BitScoop Platform powered Alexa Skill! Users are only beginning to explore what is possible on BitScoop Should you have any questions, don’t hesitate to reach out at https://bitscoop.com/support.
