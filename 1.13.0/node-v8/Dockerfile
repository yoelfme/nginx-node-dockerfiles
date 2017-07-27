FROM nginx:1.13.0

MAINTAINER Yoel Monzon <yoelfme@hotmail.com>

# Install Node.js
RUN apt-get update
RUN apt-get install -y curl gnupg git
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs build-essential

# Copy a configuration file from the current directory
ADD nginx.conf /etc/nginx/conf.d/default.conf

# Append "daemon off;" to the beginning of the configuration
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Set the default command to execute when creating a new container
CMD service nginx start