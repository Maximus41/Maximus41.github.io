# Connecting TeamCity to Slack inorder to send build success/failure notification
1. **Setup Slack**
* Create a slack workspace.
* Create a desired channel where you would like to receive teamcity build notifications
2. **Create a Slack App (This app will be responsible for sending notifications to Slack on behalf 
of teamcity project. It will make use of slack API to send the slack messages. To allow Slack app to
access slack api, the slack user needs to provide oauth access to the Slack App.**
* Create a Slack App
* Provide multiple OAUTH access to the Slack App.
* Install the Slack App to the Slack Workspace. While doing so Slack will ask for User permission
. Allow the installation.
* Once the installation is successful, a bot token will be generated. Save the token for future use.
* Once the app is installed in the Slack workspace , it will be visible under the Apps section in the workspace.
* Open the Slack App in the Slack workspace. Go to its settings and add the app to the channel where
you would like the notifications.
3. **Setup connection in Teamcity.**
* Go to project settings in the teamcity.
* Open the "Conenctions" menu.
* From the dropdown select "Slack" connection and proceed.
* This will open a form, with information on creating a Slack App and will also list the 
permissions the app will require.
* The "Basic Settings" of the Slack App will have information on Client Id and Client Secret.Save 
these information.
* Enter client id, secret and bot token into the respective fields of the form.
* Test the connection and save it. This connection will allow Teamcity to send notifications 
to Slack automatically on my behalf.


