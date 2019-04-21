# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:8.11.4

# Using NODE_PATH will add the node modules to the image
# hence making it faster
ENV NODE_PATH=/node_modules
ENV PATH=$PATH:/node_modules/.bin

# Set the working directory to /app
WORKDIR /app

# copy package.json into the container at /app
COPY package*.json /app/

# Copy the current directory contents into the container at /app
COPY . /app/

# install dependencies
RUN npm install

# Make port 3000 available to the world outside this container
EXPOSE 3000
EXPOSE 35729

# Run the app when the container launches
CMD ["npm", "start"]
