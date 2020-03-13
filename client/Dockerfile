# Use a lighter version of Node as a parent imageFROM mhart/alpine-node:8.11.4
FROM mhart/alpine-node:12

# Set the working directory to /clientWORKDIR /client
WORKDIR /client

# copy package.json into the container at /clientCOPY package*.json /client/
COPY package*.json /client/

# install dependenciesRUN npm install
RUN npm install

# Copy the current directory contents into the container at /clientCOPY . /client/
COPY . /client/

# Make port 3000 available to the world outside this containerEXPOSE 3000
EXPOSE 3000

# Run the app when the container launchesCMD ["npm", "start"]
CMD ["npm", "start"]