# Specify a base image
# alpine is a term in docker world for an image which is as small and compact as possible
# alpine version of an image means most strip down version of the image possible
# node:apline image will have just the node and nothing else, and just basic programs like ping or cat etc...
FROM node:alpine

# set a WORKDIR so that any resource/files/artifacts copied, or dependecies downloaded goes into a 
# pre-determined directory
# using a WORKDIR with specific pre-determined directory is a good idea. 
# Copying files/resources/dependencies in say, root directory could be problematic as it might conflict with
# existing folder structure of existing files, say, belonging to base image.
WORKDIR /usr/app 
# Install dependencies
# COPY everything from current working directory to inside the container
# this is required to pass package.json required by npm
COPY ./ ./ 
RUN npm install

# Default command
CMD ["npm","start"]