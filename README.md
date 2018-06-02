# S3 Download Binary Payload - RESTful API

Boilerplate for building RESTful APIs with Node, ES6 and Express.

* ES6 support via [babel](https://babeljs.io)
* REST resources as middleware via [resource-router-middleware](https://github.com/developit/resource-router-middleware)
* CORS support via [cors](https://github.com/troygoode/node-cors)
* Body Parsing via [body-parser](https://github.com/expressjs/body-parser)


## Getting Started

```
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

```
cd s3-download-binary-service

# Build Docker image
docker build -t aws/s3-download-binary-service .

# Rour Docker image
docker run -p 8080:8080 aws/s3-download-binary-service
```

## Basic Auth

Express recommends using the basic-auth library. Here's an example of how to use:

```js
var http = require('http')
var auth = require('basic-auth')

// Create server
var server = http.createServer(function (req, res) {
  var credentials = auth(req)

  if (!credentials || credentials.name !== 'aladdin' || credentials.pass !== 'opensesame') {
    res.statusCode = 401
    res.setHeader('WWW-Authenticate', 'Basic realm="S3 Download Service"')
    res.end('Access denied')
  } else {
    res.end('Access granted')
  }
})

// Listen
server.listen(3000);
```

To send a request to this route you need to include an Authorization header formatted for basic auth.

Sending a curl request first you must take the base64 encoding of name:pass or in this case `federico:secret` which is equal to `ZmVkZXJpY286c2VjcmV0`

Your curl request will then look like:
```
curl -H "Authorization: Basic ZmVkZXJpY286c2VjcmV0" http://localhost:8080/api/download
```

## License

MIT
