# Base image
FROM node:18-alpine

# Set working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json
# COPY ./package.json /app/package.json  # Ensure package.json is present in the directory

# Install dependencies
RUN npm install

# Copy the entire project into the container
COPY . /app

# Expose ports used by the services
EXPOSE 4000 

# Environment variables (optional - can be passed in at runtime)
ENV LENS2_DEV_MODE=true \
    LENS2_REFRESH_WORKER=true

# Start the Lens application
CMD ["npm", "start"]
