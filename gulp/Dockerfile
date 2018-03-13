FROM node:alpine

ENV PATH=/app/node_modules/.bin:$PATH

# We add package.json first so that the  docker image build
# can use the cache as long as contents of package.json 
# hasn't changed.

RUN npm install --global gulp 

#&& \ 
#    npm install --global npm-check-updates

WORKDIR /home/node/app

ADD package.json /home/node/app/
ADD gulpfile.js /home/node/app/
#ADD https://raw.githubusercontent.com/zetagraph/monoset/master/package.json /app/


RUN npm install gulp
RUN npm install

#RUN npm-check-updates -u && \
#RUN npm install --save  && \
#    npm update 

CMD ["npm", "start"]
