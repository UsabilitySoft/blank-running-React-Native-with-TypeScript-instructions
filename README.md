# blank-running-React-Native-with-TypeScript-instructions
Instructions for a quick way that works to fire up a React Native latest template with TypeScript March 2020.

I tried a couple of things to fire up a blank TypeScript template with my own app name but none seemed to work including Microsoft's repo or the official React Native docs, so I did it this way to get the result. I am sure there are other options such as with Ignite or something else but this process works for me right now. And uses the latest version of React Native and compatible TypeScript. I hope it can help you.

You will be creating two project folders and we will copy stuff from one to the other to get the desired result.
"NEW_APP_NAME" is the name of your new React Native app.

Presuming you have NPM and NPX installed.

*Navigate to your projects directory and run:*

`npx react-native init "NEW_APP_NAME" --template react-native-template-typescript`

*Create a folder in your projects directory for a second app (this will turn out to be your real app's source code), give it a temporary name e.g. "NEW_APP_NAME_TEMP".*


*Copy the content from [https://github.com/react-native-community/react-native-template-typescript/tree/master/template] into "NEW_APP_NAME_TEMP".*

`Rename folder "NEW_APP_NAME" to "NEW_APP_NAME_OLD"`
`Rename folder "NEW_APP_NAME_TEMP" to "NEW_APP_NAME"`

# Delete the ios folder that you copied from the template, because this has "HelloWorld" as the project name, and POD file references.

`Delete "NEW_APP_NAME/ios":`

# Copy the ios folder from the project that you inited with has the correct "NEW_APP_NAME" as the project name, and POD file references.

`Copy ios folder from "NEW_APP_NAME_OLD/ios" to "NEW_APP_NAME"`

*You can now delete "NEW_APP_NAME_OLD" which was the project you inited.*

`delete "NEW_APP_NAME_OLD"`

*Navigate to "NEW_APP_NAME" (the template project folder which is our new app)*

*Replace occurances of HelloWorld (this was the project name in the copied template)*

`Find (case sensitive) "HelloWorld" replace with "NEW_APP_NAME" in "NEW_APP_NAME" source code folder`
`Find (case sensitive) "helloworld" replace with "NEW_APP_NAME" in "NEW_APP_NAME" source code folder`

###That has completed the obscure steps to initiate your project, you can now do the normal steps to complete the setup###

*Navigate to your new folder using a terminal to install your Node.js packages:*
`npm install`

*Navigate to the ios folder using a terminal to run your iOS POD installation:*
`cd ios`
`pod install`

To test your new TypeScript app.

`yarn test`

`yarn ios`
