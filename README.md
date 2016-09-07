This walthrough will guide you through creating a basic app with meteor and then using a task runner (Gulp) to build a basic rails app.

#Install meteor
``` curl https://install.meteor.com/ | sh ```

#Create App with Meteor 
``` meteor create [app Name] ```

``` cd [app Name] ```

#Install gulp 
 ``` npm install gulp ```

#Install gulp-shell 
``` npm install --save-dev gulp-shell ```

#### save for dev mode package:gulp-shell 

#Make a gulpfile
 ``` touch gulpfile.js```

#Require The Proper Packages and Build a CLI Task

``` echo " var gulp = require('gulp'); " > gulpfile.js ```

``` echo " var shell = require('gulp-shell') " >> gulpfile.js ```

``` echo >> gulpfile.js ```

``` echo "gulp.task('this-task', shell.task([ " >> gulpfile.js ```

``` echo "/* place CLI commands here for what you want to happen in response to 'gulp this-task' */" >> gulpfile.js ```

``` echo "/* separate lines of command with a ',' */" ```

``` echo " 'echo hello', " >> gulpfile.js ```

``` echo " 'echo world' " >> gulpfile.js ```

``` echo "]);" >> gulpfile.js ```

### echo "text being written into file" > gulpfile.js 
### echo "text being appended to file" >> gulpfile.js 

``` echo "gulp.task('meanRails', shell.task([ " >> gulpfile.js ```

``` echo "'rvm use 2.3.0'," >> gulpfile.js ```

``` echo "'gem install rails',"  >> gulpfile.js ```

``` echo "'rails new [appName]'" >> gulpfile.js ```

``` echo "]))" >> gulpfile.js ``` 

# CD into your new app and run server

```	cd [appName] ```

``` rails s ```

Go to your localhost in your browser,
you've now built an app with a task



