# Pull the ruby base image
FROM ruby:3.2.2

# Set the working directory for the Docker container
WORKDIR /myapp

# Copy the Gemfile and Gemfile.lock from your app into the Docker image
COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock

# Install the gems specified in your Gemfile
RUN bundle install

# Copy the rest of your app into the Docker image
COPY . /myapp

# Expose port 3000 for the Rails server
EXPOSE 3000

# Start the Rails server
CMD ["rails", "server", "-b", "0.0.0.0"]
