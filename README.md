# DEPLOY APP WITH WEBPACK FROM TERMINAL
In the package.json file, within the "repository" object, edit the "url" value to be "git+https://github.com/USERNAME/REPONAME.git" where USERNAME and REPONAME are replaced with your GitHub username and your repository name, respectively.<br/>
It will be like this:<br/>
"repository":<br/>
    "type": "git",<br/>
    "url": "git+https://github.com/kybavitalii/momentum.git"<br/>
  },<br/>
In the package.json file, add the line: "homepage": "http://USERNAME.github.io/REPONAME", where USERNAME and REPONAME are replaced with your GitHub username and your repository name, respectively.
Add these two lines to the scripts section of the package.json file:<br/>
    "predeploy": "npm run build",<br/>
    "deploy": "gh-pages -d dist"<br/>
In the terminal, run<br/>
npm install --save-dev gh-pages<br/>
You should see these lines of JSON added to your package.json file:<br/>
"devDependencies": {<br/>
    "gh-pages": "^1.1.0"<br/>
}<br/>
Run npm run build in the command line<br/>
Run npm run deploy in the command line<br/>
All of this will create a gh-pages branch in your repo with the contents from the build directory.

If you go to the GitHub pages site (http://USERNAME.github.io/REPONAME) in a minute, you should see your app! If not, check out the console to see what errors you're getting and troubleshoot from there.
