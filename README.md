A "Hello World" server in node.js sample for Bluemix.
  
  This repo contains a complete sample of a node.js program that you can deploy
 -on IBM's [BlueMix](https://bluemix.net/) PaaS, which is based on
 +on IBM's [Bluemix](https://bluemix.net/) PaaS, which is based on
  the [Cloud Foundry open source project](http://cloudfoundry.org/).
  
  Before jumping into the code, make sure you have an IBM ID, by
  registering at the
  [IBM ID registration](https://www.ibm.com/account/profile/us?page=reg)
 -page.  You will need the IBM ID to login to BlueMix from the command line.
 +page.  You will need the IBM ID to login to Bluemix from the command line.
  
  You will also need to install the `cf` command-line tool, available
  here:
 @@ -97,11 +97,11 @@ When you visit the above url the content will be Hello World
  
  
  
 -logging into BlueMix
 +logging into Bluemix
  --------------------------------------------------------------------------------
  
  Now that you have your IBM ID and the `cf` command-line tool (see above),
 -you can log into BlueMix and the deploy your app.
 +you can log into Bluemix and the deploy your app.
  
  First you should tell the `cf` command which environment you want to operate
  with, with the `cf api` command:
 @@ -117,11 +117,11 @@ You should see the following output:
      Not logged in. Use 'cf login' to log in.
      No org or space targeted, use 'cf target -o ORG -s SPACE'
  
 -Note that as long as you only ever interact with the BlueMix environment with the
 +Note that as long as you only ever interact with the Bluemix environment with the
  `cf` command (and not any other CloudFoundry environments), you won't have to
  run the `cf api` command again.
  
 -To login to BlueMix, use the following command:
 +To login to Bluemix, use the following command:
  
      cf login
  
 @@ -149,21 +149,21 @@ When complete, you should see the following:
  
  
  
 -deploying to BlueMix
 +deploying to Bluemix
  --------------------------------------------------------------------------------
  
 -You can deploy an application to BlueMix with the `cf push` command.
 +You can deploy an application to Bluemix with the `cf push` command.
  
 -Use the following command to have the application deployed to BlueMix:
 +Use the following command to have the application deployed to Bluemix:
  
      cf push
  
  `cf push` will read the default manifest file `manifest.yml` for some
  default values of options related to your application.
  
  Note that in the documentation below, the string `${random-word}` is a
 -place-holder for a random string that BlueMix will create, so that you
 -will have a unique hostname running within BlueMix.
 +place-holder for a random string that Bluemix will create, so that you
 +will have a unique hostname running within Bluemix.
  
  After running the `cf push` command above, you should see the following output:
  
 @@ -221,7 +221,7 @@ At this point, your application is running and you can visit it on the urls
      https://hello-node${random-word}.ng.bluemix.net
  
  If you'd like to continue to play with the server by changing the code, use
 -the following command when you are ready to push the new version to BlueMix:
 +the following command when you are ready to push the new version to Bluemix:
  
      cf push
  
 @@ -275,7 +275,7 @@ locally.
  
  `.cfignore`
  
 -List of file patterns that should **NOT** be uploaded to BlueMix.
 +List of file patterns that should **NOT** be uploaded to Bluemix.
  
  See the Cloud Foundry doc
  *[Prepare to Deploy an Application](http://docs.cloudfoundry.org/devguide/deploy-apps/prepare-to-deploy.html)*
 @@ -286,7 +286,7 @@ In this case, the contents of the file are:
      node_modules
  
  This indicates the node modules you installed with `npm install` will **NOT** be
 -uploaded to BlueMix.  When your app is "staged" (ie, built on BlueMix during
 +uploaded to Bluemix.  When your app is "staged" (ie, built on Bluemix during
  `cf push`), an
  `npm install` will be run there to install the required modules.  By avoiding
  sending your node modules when you push your app, your app will be uploaded
 @@ -330,7 +330,7 @@ Standard package.json file for node packages.  You will need this file for two
  reasons:
  
  * identify your node package dependencies during `npm install`
 -* identify to BlueMix that this directory contains a node.js application
 +* identify to Bluemix that this directory contains a node.js application
  
  See the npm doc
  *[package.json](https://npmjs.org/doc/json.html)*
