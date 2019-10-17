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
           
In git bash:          
- ```pwd``` to make sure you're in your hugosite folder
```     
git init      
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


 



