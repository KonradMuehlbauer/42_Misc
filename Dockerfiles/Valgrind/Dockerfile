# Use an official base image with a Linux distribution
FROM ubuntu:20.04

# Install Valgrind, Make, and GCC
RUN apt-get update && \
    apt-get install -y valgrind \
                       make \
                       gcc

# Create a working directory for your application
WORKDIR /app

# Copy the custom script into the container
COPY copy-and-run.sh /usr/local/bin/

# Make the script executable
RUN chmod +x /usr/local/bin/copy-and-run.sh

# Use the script as the entrypoint
ENTRYPOINT ["/usr/local/bin/copy-and-run.sh"]
