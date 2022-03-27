FROM node:14-alpine

RUN npm install -g @mockoon/cli@1.2.0

ADD data.json ./data
RUN adduser --shell /bin/sh --disabled-password --gecos "" mockoon

CMD ["sh", "-c", "mockoon-cli start -d ./data -p ${PORT}; sleep infinity & wait"]