# DEPLOY APP WITH WEBPACK FROM TERMINAL
In the package.json file, within the "repository" object, edit the "url" value to be "git+https://github.com/USERNAME/REPONAME.git" where USERNAME and REPONAME are replaced with your GitHub username and your repository name, respectively.
It will be like this: 
"repository": {
    "type": "git",
    "url": "git+https://github.com/kybavitalii/momentum.git"
  },
In the package.json file, add the line: "homepage": "http://USERNAME.github.io/REPONAME", where USERNAME and REPONAME are replaced with your GitHub username and your repository name, respectively
Add these two lines to the scripts section of the package.json file:
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
In the terminal, run npm install --save-dev gh-pages
You should see these lines of JSON added to your package.json file:
"devDependencies": {
    "gh-pages": "^1.1.0"
}
Run npm run build in the command line
Run npm run deploy in the command line
All of this will create a gh-pages branch in your repo with the contents from the build directory.

If you go to the GitHub pages site (http://USERNAME.github.io/REPONAME) in a minute, you should see your app! If not, check out the console to see what errors you're getting and troubleshoot from there.
