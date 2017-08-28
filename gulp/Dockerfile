FROM node:alpine

WORKDIR /app
ENV PATH=/app/node_modules/.bin:$PATH

# We add package.json first so that the  docker image build
# can use the cache as long as contents of package.json 
# hasn't changed.

ADD https://raw.githubusercontent.com/zetagraph/monoset/master/package.json /app/
RUN npm install --global gulp && \ 
    npm install


