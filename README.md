# azure-devops-api

By using this package lib we can create work item in azure devops.
only work item creation is supported in this version

# PAT
personnal access token is very important for using this library
https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page

# Install 
```
npm i azure-devops-api
```

# Usage

```
const addWorkItem = require("azure-devops-api");

let token = "PAT.............X";
let type   = "<type like Bug,Task,UserStory....>";
let title  = "<title>";
let description  = <desc about the item>;
let areaPath  ="<area path>";
let iterationPath  = "<iteration path>";
let assignedto  = "<assign email id>";
let parentLink = "<parent link url>" ; //--> this is optional  but you need to pass empty string if you dont have any parent link
const workItem = addWorkItem.createWorkItem(token,<org name>, <project name>, {
  type,
  title,
  description,
  areaPath,
  iterationPath,
  assignedto,
  parentLink
})

console.log(workItem.then((workItemId) => console.log(workItemId)));

```
 
# Package
https://www.npmjs.com/package/azure-devops-api

