# Use the base App Engine Docker image, based on debian jessie.
FROM launcher.gcr.io/google/debian8

# https://yarnpkg.com/en/docs/install#linux-tab
RUN apt-get update && \
    apt-get install -y curl apt-transport-https git bzip2 && \

<<<<<<< HEAD
# Install the latest LTS release of nodejs
RUN mkdir /nodejs && curl https://nodejs.org/dist/v8.9.4/node-v8.9.4-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1
ENV PATH $PATH:/nodejs/bin

# Install the latest stable release of Yarn
RUN mkdir /yarn && curl -L https://github.com/yarnpkg/yarn/releases/download/v1.3.2/yarn-v1.3.2.tar.gz | tar xvzf - -C /yarn --strip-components=1
ENV PATH $PATH:/yarn/bin
=======
    # Install newer Node version.
    curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    apt-get install -y nodejs && \

    # Install Yarn
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && \
    apt-get install -y yarn
>>>>>>> upstream/master

ENTRYPOINT ["yarn"]
