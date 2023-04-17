## Requirements 
#### (These are for windows only. For Mac visit https://shopify.dev/docs/themes/tools/cli/install#requirements)
1=> Install Nodejs from this link https://nodejs.org/en/download

2=> Install Ruby from this link https://rubyinstaller.org/downloads/ (select MSYS2 while installing ruby)

3=> Install git from this link https://git-scm.com/downloads

4=> Install bundler by opening CMD/Terminal with admin access and typing `gem install bundler`

## Install Shopify CLI 

1 => Open CMD/Terminal again and type `npm install -g @shopify/cli @shopify/theme` to install Shopify and Shopify Theme CLI 

**NOTE** Shopify theme dev command is already setup so it can be used by following Start Project instructions. For instructions to run other commands view this [guide](https://github.com/C2Digital1/c2theme/blob/main/Shopify-CLI.md) 


## Setup Github
1=> Open CMD/Terminal in the folder where you would like to start the theme project 

2=> Clone this repo https://github.com/C2Digital1/c2theme using command `git clone https://github.com/C2Digital1/c2theme` 

3=> Git might ask you to login into your account, Use your c2 account for this 

4=> Type `git config --global user.email "YOUR_EMAIL"` to add your email for git.(replace YOUR_EMAIL with your c2 email used when creating github account)

5=> Type `$ git config --global user.name "YOUR_NAME"` to add your username for git.(replace YOUR_NAME with your github username)

6=> Type `cd c2theme` to move into project directory created by git clone command.

7=> Create a new branch using `git branch [Your Name here]-dev`

8=> Checkout into your branch by typing `git checkout [Your branch name]`

9=> Add a remote origin to c2theme repo by typing `git remote add c2 https://github.com/C2Digital1/c2theme.git`


## Setup Shopify

1 => Search store C2 Theme in Shopify partners and in `Apps> Theme Access > Create Password` generate your new password by filling your name and email, This will send a theme access token to your email


## Start Project

1=> In your project directory open CMD/Terminal and type command `npm install` to install dependencies 


2=> Duplicate **example.shopify.env.json** and rename it to **shopify.env.json** and update values in it like so 

`
"SHOPIFY_CLI_THEME_TOKEN": "Add Your Theme Access Token here"
`

`
"SHOPIFY_FLAG_THEME_ID": "Add Your Theme ID here if any. if there is no theme leave this empty"
`

`
"SHOPIFY_FLAG_STORE": "c2-theme"
` 


3=> Run `npm run dev` in CMD/Terminal to create a new preview theme and preview it locally

## Push changes

1=> After making changes to this theme ,follow below commands to push them to github

`git checkout [Your branch name]` to make sure you are in right branch

`git add .` Stage All changes

`git commit -m "Commit Name here(can be feature name)"` Add a commit 

`git push c2 [Your branch name]`


2=> Step 1 will update your branch with latest code, All that is left is to create a Pull Request to Main branch by going to https://github.com/C2Digital1/c2theme


## Keep your local theme up-to-date with Main branch for future changes

1=> When starting a new feature or fixing a bug, make sure your theme is up-to-date with Main branch first

2=> You can do it by using git's pull command, Below are the instructions

3=> First make sure you do not have any staged change by using command `git stash` to delete all staged changes

4=> Than type `git pull c2 main` to pull everything from main branch

5=> Resolve any conflicts(if any) and than continue with your work

6=> After all changes are done, You can follow **PUSH CHANGES** instructions to push the new changes again