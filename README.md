# azure-devops-api

using client library we can create work item in azure devops

# PAT
personnal access token is very important for using this library
https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page

# Install 
```
npm i azure-devops-api
```

# Usage

```
const createWorkItem = require('azure-devops-api');

let token = "PAT.............X";
let type   = "<type like Bug,Task,UserStory....>";
let title  = "<title>";
let description  = <desc about the item>;
let areaPath  ="<area path>";
let iterationPath  = "<iteration path>";
let assignedto  = "<assign email id>"
createWorkItem(token,<org name>, <project name>, {
  type,
  title,
  description,
  areaPath,
  iterationPath,
  assignedto
})
```
 
