# @unstoppabledomains/tldsresolverkeys update script

@unstoppabledomains/tldsresolverkeys is an NPM / Yarn Package containing Unstoppable TLDs and Resolver Keys. This script is used to update the package at regular intervals.

**Prereq**
- Make sure you have node setup in your environment
- Make sure you have cloned the npm resolver keys package
- Make sure you are a contributer to both the UD NPM and Github orgs

## Install
`npm install`

## Running the Script
`node resolverkeys.js`

## Usage  
**Changes**
`File written successfully` printed in the console

 1. Copy the new objects over to the index.js file within the npm package
 2. Update the readme changelog with any changes showed in jsonMetaData.json
 3. Update readme variable definitions (use https://codebeautify.org/remove-extra-spaces to clean up the array(s))
 4. Update the package.json file with the new version number
 - <x.x.x>
 - Iterating the first digit should only occur if there is a change to the structure of the package's variables
 - Iterating the second digit should occur either when a TLD is added or removed
 - Iterating the third digit should occur either when a new token is added or removed
 5. Run `git add .`
 6. Run `git commit -m "ADD YOUR COMMIT MESSAGE"`
 7. Run `git push`
 8. Run `npm login`
 9. Run `npm publish`

**No Changes**
`Current data is up-to-date` printed in the console

You're done! :)

## To-Do 
- ✅ Allow teammates to use this code
- ✅ Check if single address token is now multi address token and deprecate
- Cleanup comments & JSDocs 
- Logic for checking the TLD array
- Automate the running of this package & Send an email / notification when changes are detected