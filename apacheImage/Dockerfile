# Step 1: Use an official Ubuntu base image
FROM ubuntu:22.04

# Step 2: Update the package list and install Apache
RUN apt update -y && apt install -y apache2

# Step 3: Ensure Apache runs in the foreground (Docker best practice)
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

# Step 4: Expose port 80
EXPOSE 80

# Step 5: Set the default command to run Apache in the foreground
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
