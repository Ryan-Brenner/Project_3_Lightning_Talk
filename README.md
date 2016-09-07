
#Install meteor
``` curl https://install.meteor.com/ | sh ```

#Create App with Meteor 
``` meteor create [app Name] ```

#Install gulp 
 ``` npm install gulp ```

#Install gulp-shell 
``` npm install --save-dev gulp-shell ```
 /* save for dev mode package:gulp-shell */ 

#Make a gulpfile
 ``` touch gulpfile.js```

#require the proper files and build a CLI task

``` echo " var gulp = require('gulp'); " > gulpfile.js
echo >> gulpfile.js
echo "gulp.task('this-task', shell.task([ " >> gulpfile.js
echo "/* place CLI commands here for what you want to happen in response to 'gulp this-task' */" >> gulpfile.js
echo "/* separate lines of command with a ',' */"
echo " 'echo hello', " >> gulpfile.js
echo " 'echo world' " >> gulpfile.js
echo "]);" >> gulpfile.js ```

/* echo "text being written into file" > gulpfile.js */
/* echo "text being appended to file" >> gulpfile.js */

``` echo "gulp.task('mean rails', shell.task([ " >> gulpfile.js ``` /n
``` echo "'rvm use 2.3.0'," >> gulpfile.js ``` /n
``` echo "'gem install rails',"  >> gulpfile.js ``` /n
``` echo "'echo -n "Enter the name of your app"' " >> gulpfile.js ``` /n
``` echo "' read -n appName" >> gulpfile.js ``` /n
``` echo "'rails new "$appName"'," >> gulpfile.js ``` /n
``` echo "]);" >> gulpfile.js ``` 

*CD into your new app and run server

```	cd your_app_name ```
``` rails s ```

you've now built an app with a task



