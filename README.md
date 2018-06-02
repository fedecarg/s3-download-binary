# Express & ES6 REST API

This is a straightforward boilerplate for building REST APIs with ES6 and Express.

- ES6 support via [babel](https://babeljs.io)
- REST resources as middleware via [resource-router-middleware](https://github.com/developit/resource-router-middleware)
- CORS support via [cors](https://github.com/troygoode/node-cors)
- Body Parsing via [body-parser](https://github.com/expressjs/body-parser)

> If you are using [Mongoose](https://github.com/Automattic/mongoose), you can automatically expose your Models as REST resources using [restful-mongoose](https://git.io/restful-mongoose).


## Getting Started

```sh
# Clone repo
git clone git@github.com:fedecarg/s3-download-binary.git
cd s3-download-binary

# Make it your own
rm -rf .git && git init && npm init

# Install dependencies
npm install

# Start development server (with live-reload)
PORT=8080 npm run dev

# Start production server:
PORT=8080 npm start
```

## Docker Support

```sh
cd express-es6-rest-api

# Build your docker
docker build -t aws/s3-download-binary-service .

# run your docker
docker run -p 8080:8080 aws/s3-download-binary-service
```

## License
---

MIT
