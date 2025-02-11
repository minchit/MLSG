# Use Node.js as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and yarn.lock (or package-lock.json) first
COPY package.json yarn.lock ./

# Install dependencies
RUN yarn install --frozen-lockfile

# Copy the rest of the Strapi application
COPY . .

# Expose the default Strapi port
EXPOSE 1337

# Start the Strapi application
CMD ["yarn", "develop"]
