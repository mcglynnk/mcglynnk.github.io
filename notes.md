Requires:      
Ruby in Ubuntu, hugo gem for ruby      
Git bash       
Github account      
       
### Step 1        
- Download zip file containing hugo academic website files
https://sourcethemes.com/academic/docs/install/#install-with-zip
- I put this zip file in c/users/kelly/sites/hugosite
- follow instructions at link above
- hugosite folder should contain folders such as config, content, data, layouts, public, etc
           
In git bash: *you could run all of the git commands here in Ubuntu, but will have to enter your github username/password for every git push*         
- ```pwd``` to make sure you're in your hugosite folder
```     
git init      # only need to do this once
git add .  
git commit -m "adding files"    
``` 
                 
- Log in to github, make two new repositories:   
1. <your username>.github.io (this one is for Step 3)
2. academic-kickstart (or any other name)    
      
  
- After clicking 'make new repository' for the academic-kickstart repository, copy the line from the following page that contains 
```git remote add origin https://[your github username].git``` and paste into git bash 
(use ```pwd``` to make sure you're in your hugosite folder)      
- ```git remote -v``` to make sure your remote is set correctly     
- Then type:
```git push origin master```     


### Step 2     
- Now you can edit the website files (I use Sublime Text 3 to edit the files)     
- Edit files in hugosite/config/\_default for basic info, menu titles, etc.  Other website sections are in the other folders,
files you'll add to the site (like a CV) will go into static/files     
       
- When finished editing the files, in Ubuntu:      
(cd to your hugosite folder)      
Run this command to build your site files (it will create a new folder called public in your hugosite folder)
```    
hugo     
```      
- Run:  
```hugo serve --watch```     
This will allow you to view your site locally (go to localhost:1313, or the address listed after you entered this command)
and make sure your website looks how you want it to.
      
### Step 3      
If everything looks good, ctrl+C to stop serving the website.       
(From https://sourcethemes.com/academic/docs/deployment/):       
"In your config.toml file, set baseurl = "https://<USERNAME>.github.io/", where <USERNAME> is your Github username. Stop Hugo if it’s running and delete the public directory if it exists (by typing rm -r public/)."      
        
In Git bash:    
```git submodule add -f -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public```
    
In Git bash:    
First push your edited site files to your academic-kickstart repository, same as above: make sure you're in your hugosite folder,
```git remote -v``` to check your remote is correct (it should be the address to your academic-kickstart repo), ```git add .```, ```git commit -m "your commit message here"```, ```git push origin master```.      
        
In Ubuntu:    
```hugo```      
This will re-build the HTML files in the public folder.      
       
In Git bash:      
```
cd public      
git add .     
git commit -m "build website"    
git push origin master    
cd ..
```
         
Finally, go to your github repository <USERNAME>.github.io, go into settings > options, and configure Github Pages at the bottom of the page.        
The website should now be live!       


### To Update      
To update the website files later,
- modify files in your local hugosite folder    
- push everything to the academic-kickstart repo    
- ```hugo serve --watch``` to check your edits    
- ```hugo``` to re-build the HTML in the 'public' folder      
- ```cd public```, ```git remote -v``` *always make sure this is correct!  Should point to your <USERNAME>.github.io       
- git add ., commit and push the files in the public folder to your <USERNAME>.github.io repo       


