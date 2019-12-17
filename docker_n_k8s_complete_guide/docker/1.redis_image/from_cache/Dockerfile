# Use an existing docker image as a base
FROM alpine

# Download and insall a dependecy
RUN apk add --update redis
# Run another command to add a new dependency "gcc"
# If you build this file, after building the first docker image with "redis" only
# then docker server will use cache for STEP1 and STEP2
RUN apk add --update gcc 

# Tell the image what to do when it starts as a container
CMD ["redis-server"]