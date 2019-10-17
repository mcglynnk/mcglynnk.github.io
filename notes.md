Requires:      
Ruby in Ubuntu, hugo gem for ruby      
Git bash       
Github account      
       
- Download zip file containing hugo files
https://sourcethemes.com/academic/docs/install/#install-with-zip
- I put this zip file in c/users/kelly/sites/hugosite
- follow instructions at link above
- hugosite folder should contain folders such as config, content, data, layouts, public, etc

(in git bash)      
- ```pwd``` to make sure you're in your hugosite folder
```     
git init      
git add .  
git commit -m "adding files"    
```

        
- Log in to github, make a new repository       
- After clicking 'make new repository,' copy the line from the following page that contains 
```git remote add origin https://[your github username].git``` and paste into git bash 
(use ```pwd``` to make sure you're in your hugosite folder)      
- ```git remote -v``` to make sure your remote is set correctly     
- Then type:
```git push origin master```     
       
       

 



