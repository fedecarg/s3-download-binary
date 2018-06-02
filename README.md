# S3 Download Binary Payload - RESTful API

Boilerplate for building RESTful APIs with Node, ES6 and Express.

* ES6 support via [babel](https://babeljs.io)
* REST resources as middleware via [resource-router-middleware](https://github.com/developit/resource-router-middleware)
* CORS support via [cors](https://github.com/troygoode/node-cors)
* Body Parsing via [body-parser](https://github.com/expressjs/body-parser)


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
cd s3-download-binary-service

# Build Docker image
docker build -t aws/s3-download-binary-service .

# Rour Docker image
docker run -p 8080:8080 aws/s3-download-binary-service
```

## License

MIT
