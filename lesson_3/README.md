## Objective learn how to rebase your fork  

### 1) Connect to docker image from lesson 2 
Assuming your image name and tag are cloudtrain:lesson_2  
You can check with docker images what your images and tags are.   
It is important that you use the same image for which you got the ssh key from otherwise redo lesson 2  
```
docker run --rm -it cloudtrain:lesson_2 bash
```

### 2) Clone your fork
```
git clone git@github.com:cakomakako/cloudtrainer.git
```

### 3) Explore your fork 
Notice lesson 3 is missing 
Check web [your fork](https://github.com/cakomakako/cloudtrainer)  
```
cd /app/cloudtrainer
ls 
```

### 4) Rebase your fork 
```
cd /app/cloudtrainer
git config --global user.email "youremail@email.com" # customize this
git config --global user.name "Your name" # customize this
git remote remove upstream
git remote add upstream https://github.com/eric-sd/cloudtrainer.git
git fetch upstream
git rebase upstream/$(git branch --show-current)
git push -f origin $(git branch --show-current)
```

### 5) Explore your fork 
Notice lesson 3 is now present
Check web [your fork](https://github.com/cakomakako/cloudtrainer)  
```
cd /app/cloudtrainer
ls 
```
