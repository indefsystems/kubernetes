# Use an existing docker image as a base
FROM alpine

# Download and insall a dependecy
# In this file, we have changed the order of RUN commands
# so "gcc" is downloaded and then "redis"
# In this case, Docker server will use cache only for STEP1 (FROM alpine) and not for "redis" as order of the command has changed
# So order of the command matters for Docker server to be able to use cache or not
RUN apk add --update gcc 

RUN apk add --update redis

# Tell the image what to do when it starts as a container
CMD ["redis-server"]