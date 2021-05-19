## If you have made this far then don't ever quit. 

Step 1: 
Create a folder in your local filesystem called cloudtrain  

Step 2: 
Create a file Called [Dockerfile](Dockerfile)  
With the contents from the file in this folder called Dockerfile


Step 3:  
Build the docker image
```
docker build -t cloudtrain .
```

Step 4: 
Run an interactive shell with this image 
```
docker run --rm -it cloudtrain bash
```

Step 5:
run top command
```
top
Ctrl-C
exit
```







