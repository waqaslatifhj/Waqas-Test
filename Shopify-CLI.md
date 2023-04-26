## Package.json

This file contains all information about Node.js project and all external dependencies it uses all in JSON format.

### Scripts

These scripts are normally used to bundle(combine) large scripts so they can be typed easily by running `npm run <script name>`.
There are a few scripts already added like `"dev": "shopify theme dev"`  which can be run using `npm run dev`.If you prefer you can run these scripts directly as well by using  `shopify theme dev` and it will work the same.

### Dependencies
These are list of Javascript packages/libraries being used in project with their versions. So we have a record of all libaries used.Additionally these packages are stored in `node_modules` folder. We can download these packages from https://www.npmjs.com/. A few examples for these packages can be Jquery, React etc. All these  packages are public and can be installed by running `npm install <package name>`


## Private Packages 
Same as public packages,we can use private packages as well.These packages are can only be used inside an organization like github and require github access token to install. In this way we can create C2's internal packages for utilies and such.If anyone would like to create a package feel free to create it and update this read me with install instructions for others.


### Instructions to install private packages

#### Generate Github Access Token 
1 => Navigate to your C2 Github account > Settings> Developer Settings > Personal Access Tokens > Tokens (Classic)

2 => Press Generate New Token and select Classic

3 => In Note field type "Private Package", set any expiration and in permissions, check Read Packages and press Generate token

4 => This will generate a token which you can save to use later

####  Using The token
1=> Clone c2-theme repo if you haven't and follow the this [guide](https://github.com/C2Digital1/c2-theme/blob/main/README.md) to setup your project

2=> After setup is complete, duplicate `example.env` file and rename it as `.env` and add your github token this file.
(This file is ignored by git so your token does't get pushed to github when creating PRs)

#### Install Private Package
1=> As mentioned above, we need to use the github token to install these packages. To do that instead of using  `npm install <package name>` command you would use for public packages, you can use `private` script from Package.json and use it like so `npm run private <package.name>`. With this the package will be installed. You can find each package instructions in their README.



## List of Private Packages Available

-  [C2](https://github.com/C2Digital1/cli/pkgs/npm/c2)




