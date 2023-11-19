Command To create docket image
FROM node:20 #specifies the version of version that we want to have
WORKDIR /usr/src/app #directory from where we want to fetch src code to fetch image and store image to save directory


COPY . . #Here first . means that the files that we need to add during the creation of image for instance COPY ./index.js . means only index.js will we added to image that we created during image creation , second . means on which path we need to store docker image too


RUN npm install  #In this we install all dependencies that we listed on our package.json file 


EXPOSE 3000 #In our app we are using 3000 port so we instruct container to use this port
CMD ["node","index.js"] 




------------------------


.dockerignore this file instructs which file or folder does not need to be added in the image usually we add node_modules in this