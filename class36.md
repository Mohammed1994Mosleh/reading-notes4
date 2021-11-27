# class 36 Reading Notes:Amplify and Cognito

- interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other  Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool.

![](https://d2908q01vomqb2.cloudfront.net/0a57cb53ba59c46fc4b692527a38a87c78d84028/2017/07/19/CognitoDiagram.png)

### Configure Auth Category

1- "amplify add auth"

2-


? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`


3- "amplify push"

### Install Amplify Libraries

Add the following dependency to your app's build.gradle:


dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}


### Initialize Amplify Auth

Add the Auth plugin before calling Amplify.configure. Update the code you added in Prerequisites:


Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());


### Check the current auth session


Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);


