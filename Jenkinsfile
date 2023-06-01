# Use Amazon Linux as the base image
FROM amazonlinux:latest

# Update the package repository and install Apache2
RUN yum update -y && \
    yum install -y httpd

# Copy your Apache config file to the container
COPY apache-config.conf /etc/httpd/conf.d/my-apache.conf

# Copy your web application files to the container
COPY . /var/www/html/

# Expose port 80 for Apache
EXPOSE 80

# Start Apache in the foreground
CMD ["httpd", "-D", "FOREGROUND"]
