# 2. Download the Demo “Ops Buddy” Project
Y
ou can download a pre-zipped copy of the code at https://cdn.bitscoop.com/bitscoop-alexa-demo/0.1.0/bitscoop-alexa-demo-0.1.0.zip and then skip to step 3.

The SHA-256 hash for this file is

`77d59957c989c8be364afb31076a787884a73cb184f9d4f5933f5f90e988ac72.`

If you want to build the project yourself instead of using the pre-zipped copy above, you will need to have node.js and \`npm\` installed on your machine so that you can install the demo’s dependencies before uploading the code to Lambda. Download the project from

[bitscooplabs/bitscoop-alexa-demo](https://github.com/bitscooplabs/bitscoop-alexa-demo)

From the top level of this directory run

`npm install`

to install all of the project-wide dependencies, then go to the src/ directory and again run

`npm install`

Finally go up one level to the top-level directory and run the command

`grunt build`

to zip the project to

`dist/bitscoop-alexa-demo-<version>.zip`
