# api documentation for  [servicebus (v2.0.9)](https://github.com/mateodelnorte/servicebus)  [![npm package](https://img.shields.io/npm/v/npmdoc-servicebus.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-servicebus) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-servicebus.svg)](https://travis-ci.org/npmdoc/node-npmdoc-servicebus)
#### Simple service bus for sending events between processes using amqp.

[![NPM](https://nodei.co/npm/servicebus.png?downloads=true)](https://www.npmjs.com/package/servicebus)

[![apidoc](https://npmdoc.github.io/node-npmdoc-servicebus/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-servicebus_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-servicebus/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-servicebus/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-servicebus/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matt Walters",
        "email": "mattwalters5@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/mateodelnorte/servicebus/issues"
    },
    "contributors": [
        {
            "name": "mattwalters5@gmail.com"
        },
        {
            "name": "timisbusy@gmail.com"
        },
        {
            "name": "mail@chrisabrams.com"
        }
    ],
    "dependencies": {
        "amqplib": "^0.4.0",
        "debug": "^2.2.0",
        "extend": "^3.0.0",
        "node-uuid": "^1.4.3",
        "readable-id": "0.0.3"
    },
    "description": "Simple service bus for sending events between processes using amqp.",
    "devDependencies": {
        "longjohn": "~0.2.9",
        "mocha": ">=2.3.3",
        "servicebus-retry": "0.0.9",
        "should": "7.1.0",
        "sinon": "~1.17.1"
    },
    "directories": {},
    "dist": {
        "shasum": "dc7f49239131402e1eba8245736f622510395dad",
        "tarball": "https://registry.npmjs.org/servicebus/-/servicebus-2.0.9.tgz"
    },
    "engines": {
        "node": "0.6 || 0.8 || 0.9 || 0.10 || 0.12"
    },
    "gitHead": "9ac6367f3a6bafa9595910235d5232a1c70862a0",
    "homepage": "https://github.com/mateodelnorte/servicebus",
    "maintainers": [
        {
            "name": "mateodelnorte",
            "email": "mattwalters5@gmail.com"
        },
        {
            "name": "timisbusy",
            "email": "timisbusy@gmail.com"
        }
    ],
    "name": "servicebus",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mateodelnorte/servicebus.git"
    },
    "scripts": {},
    "version": "2.0.9",
    "warnings": [
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.6 || 0.8 || 0.9 || 0.10 || 0.12"
            },
            "pkgid": "servicebus@2.0.9"
        },
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.6 || 0.8 || 0.9 || 0.10 || 0.12"
            },
            "pkgid": "servicebus@2.0.9"
        }
    ]
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module servicebus](#apidoc.module.servicebus)
1.  [function <span class="apidocSignatureSpan">servicebus.</span>bus (options, implOpts)](#apidoc.element.servicebus.bus)
1.  [function <span class="apidocSignatureSpan">servicebus.</span>namedBus (name, options, implOpts)](#apidoc.element.servicebus.namedBus)
1.  object <span class="apidocSignatureSpan">servicebus.</span>bus.prototype

#### [module servicebus.bus](#apidoc.module.servicebus.bus)
1.  [function <span class="apidocSignatureSpan">servicebus.</span>bus ()](#apidoc.element.servicebus.bus.bus)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.</span>super_ ()](#apidoc.element.servicebus.bus.super_)

#### [module servicebus.bus.prototype](#apidoc.module.servicebus.bus.prototype)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>correlate ()](#apidoc.element.servicebus.bus.prototype.correlate)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>correlationId (forceNew)](#apidoc.element.servicebus.bus.prototype.correlationId)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>createCorrelationId (forceNew)](#apidoc.element.servicebus.bus.prototype.createCorrelationId)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>handleIncoming ()](#apidoc.element.servicebus.bus.prototype.handleIncoming)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>handleOutgoing (queueName, message, options, callback)](#apidoc.element.servicebus.bus.prototype.handleOutgoing)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>logger (options)](#apidoc.element.servicebus.bus.prototype.logger)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>messageDomain (opts)](#apidoc.element.servicebus.bus.prototype.messageDomain)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>package ()](#apidoc.element.servicebus.bus.prototype.package)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>retry (options)](#apidoc.element.servicebus.bus.prototype.retry)
1.  [function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>use (middleware)](#apidoc.element.servicebus.bus.prototype.use)



# <a name="apidoc.module.servicebus"></a>[module servicebus](#apidoc.module.servicebus)

#### <a name="apidoc.element.servicebus.bus"></a>[function <span class="apidocSignatureSpan">servicebus.</span>bus (options, implOpts)](#apidoc.element.servicebus.bus)
- description and source-code
```javascript
function bus(options, implOpts) {
  return new rabbitmq.Bus(options, implOpts);
}
```
- example usage
```shell
...

## Sending and Receiving

Servicebus allows simple sending and recieving of messages in a 1:1 sender:listener configuration. The following two processes will
 send an event message called 'my.event' every second from process A to process B via RabbitMQ and print out the sent event:

Process A:

  var bus = require('servicebus').bus();
  bus.listen('my.event', function (event) {
    console.log(event);
  });

Process B:

  var bus = require('servicebus').bus();
...
```

#### <a name="apidoc.element.servicebus.namedBus"></a>[function <span class="apidocSignatureSpan">servicebus.</span>namedBus (name, options, implOpts)](#apidoc.element.servicebus.namedBus)
- description and source-code
```javascript
function namedBus(name, options, implOpts) {
  var bus = namedBuses[name];
  if ( ! bus) {
    bus = namedBuses[name] = new rabbitmq.Bus(options, implOpts);
  }
  return bus;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.servicebus.bus"></a>[module servicebus.bus](#apidoc.module.servicebus.bus)

#### <a name="apidoc.element.servicebus.bus.bus"></a>[function <span class="apidocSignatureSpan">servicebus.</span>bus ()](#apidoc.element.servicebus.bus.bus)
- description and source-code
```javascript
function Bus() {
  this.incomingMiddleware = [];
  this.outgoingMiddleware = [];
  EventEmitter.call(this);
  this.setMaxListeners(Infinity);
}
```
- example usage
```shell
...

## Sending and Receiving

Servicebus allows simple sending and recieving of messages in a 1:1 sender:listener configuration. The following two processes will
 send an event message called 'my.event' every second from process A to process B via RabbitMQ and print out the sent event:

Process A:

  var bus = require('servicebus').bus();
  bus.listen('my.event', function (event) {
    console.log(event);
  });

Process B:

  var bus = require('servicebus').bus();
...
```

#### <a name="apidoc.element.servicebus.bus.super_"></a>[function <span class="apidocSignatureSpan">servicebus.bus.</span>super_ ()](#apidoc.element.servicebus.bus.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.servicebus.bus.prototype"></a>[module servicebus.bus.prototype](#apidoc.module.servicebus.bus.prototype)

#### <a name="apidoc.element.servicebus.bus.prototype.correlate"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>correlate ()](#apidoc.element.servicebus.bus.prototype.correlate)
- description and source-code
```javascript
correlate = function () {
  return {
    handleOutgoing: addCorrelationId
  };
}
```
- example usage
```shell
...
   throw new Error('Tests require a RABBITMQ_URL environment variable to be set, pointing to the RabbiqMQ instance you wish to use
.');

 var busUrl = process.env.RABBITMQ_URL

 var bus = require('../').bus({ url: busUrl });

 bus.use(bus.package());
 bus.use(bus.correlate());
 bus.use(bus.logger());

 module.exports.bus = bus;
'''

Middleware may define one or two functions to modify incoming or outgoing messages:
...
```

#### <a name="apidoc.element.servicebus.bus.prototype.correlationId"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>correlationId (forceNew)](#apidoc.element.servicebus.bus.prototype.correlationId)
- description and source-code
```javascript
correlationId = function (forceNew) {
  if (process.domain && process.domain.correlationId && ! forceNew) {
    return process.domain.correlationId;
  }
  return readableId();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.createCorrelationId"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>createCorrelationId (forceNew)](#apidoc.element.servicebus.bus.prototype.createCorrelationId)
- description and source-code
```javascript
createCorrelationId = function (forceNew) {
  if (process.domain && process.domain.correlationId && ! forceNew) {
    return process.domain.correlationId;
  }
  return readableId();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.handleIncoming"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>handleIncoming ()](#apidoc.element.servicebus.bus.prototype.handleIncoming)
- description and source-code
```javascript
handleIncoming = function () {
  var index = this.incomingMiddleware.length - 1;
  var self = this;

  var args = Array.prototype.slice.call(arguments);

  var callback = args.pop();

  function next (err) {
    if (err) return callback(err);

    var layer;
    var args = Array.prototype.slice.call(arguments, 1);

    layer = self.incomingMiddleware[index];

    index = index - 1;

    if ( undefined === layer) {
      return callback.apply(self, args);
    } else {
      args.push(next);
      return layer.apply(self, args);
    }
  }

  args.unshift(null);

  return next.apply(this, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.handleOutgoing"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>handleOutgoing (queueName, message, options, callback)](#apidoc.element.servicebus.bus.prototype.handleOutgoing)
- description and source-code
```javascript
handleOutgoing = function (queueName, message, options, callback) {
  if (typeof options === 'function') {
    callback = options;
    options = null;
  }

  var index = 0;
  var self = this;


  function next (err) {
    if (err) return callback(err);

    var layer;
    var args = Array.prototype.slice.call(arguments, 1);

    layer = self.outgoingMiddleware[index];

    index++;

    if ( undefined === layer) {
      return callback.apply(self, args);
    } else  {
      args.push(next);
      return layer.apply(self, args);
    }
  }

  return next(null, queueName, message, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.logger"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>logger (options)](#apidoc.element.servicebus.bus.prototype.logger)
- description and source-code
```javascript
logger = function (options) {
  options = options || {};
  label = options.label || 'servicebus';
  var log = options.log || debug(label);
  fnIncoming = options.fnIncoming || function (channel, message, options, next) {
    log(util.format('received %j via routingKey %s', message.content, message.fields.routingKey));
  };
  fnOutgoing = options.fnOutgoing || function (message, queueName) {
    log(util.format('sending %j to %s', message, queueName));
  };

  function logIncoming (channel, message, options, next) {
    fnIncoming(channel, message, options);
    var args = Array.prototype.slice.call(arguments);
    var next = args.pop();
    args.unshift(null);
    next.apply(this, args);
  }

  function logOutgoing (queueName, message, options, next) {
    if (typeof options === 'function') {
      next = options;
      options = null;
    }

    fnOutgoing(message, queueName);
    next(null, queueName, message, options);
  }

  return {
    handleIncoming: logIncoming,
    handleOutgoing: logOutgoing
  };
}
```
- example usage
```shell
...

  var busUrl = process.env.RABBITMQ_URL

  var bus = require('../').bus({ url: busUrl });

  bus.use(bus.package());
  bus.use(bus.correlate());
  bus.use(bus.logger());

  module.exports.bus = bus;
'''

 Middleware may define one or two functions to modify incoming or outgoing messages:

'''
...
```

#### <a name="apidoc.element.servicebus.bus.prototype.messageDomain"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>messageDomain (opts)](#apidoc.element.servicebus.bus.prototype.messageDomain)
- description and source-code
```javascript
function messageDomain(opts) {

  opts = opts || {};

  return {

    handleIncoming: function json (channel, message, options, next) {

      var d = domain.create();

      if (opts.onError) {
        d.on('error', function (err) {
          if (opts.onError) {
            opts.onError(err, message, channel, d);
          } else {
            throw err;
          }
        });
      }

      d.run(function() {

        if (message.properties.correlationId) {
          d.correlationId = message.properties.correlationId;
        }

        next.bind(this, null, channel, message, options)();

      });

    },

  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.package"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>package ()](#apidoc.element.servicebus.bus.prototype.package)
- description and source-code
```javascript
package = function () {
  return {
    handleOutgoing: packageMessage,
    handleIncoming: handleIncoming
  };
}
```
- example usage
```shell
...
 if ( ! process.env.RABBITMQ_URL)
   throw new Error('Tests require a RABBITMQ_URL environment variable to be set, pointing to the RabbiqMQ instance you wish to use
.');

 var busUrl = process.env.RABBITMQ_URL

 var bus = require('../').bus({ url: busUrl });

 bus.use(bus.package());
 bus.use(bus.correlate());
 bus.use(bus.logger());

 module.exports.bus = bus;
'''

Middleware may define one or two functions to modify incoming or outgoing messages:
...
```

#### <a name="apidoc.element.servicebus.bus.prototype.retry"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>retry (options)](#apidoc.element.servicebus.bus.prototype.retry)
- description and source-code
```javascript
retry = function (options) {
  throw new Error('bus.retry() middleware is deprecated. please use https://github.com/mateodelnorte/servicebus-retry instead')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.servicebus.bus.prototype.use"></a>[function <span class="apidocSignatureSpan">servicebus.bus.prototype.</span>use (middleware)](#apidoc.element.servicebus.bus.prototype.use)
- description and source-code
```javascript
use = function (middleware) {
  if (middleware.handleIncoming) this.incomingMiddleware.push(middleware.handleIncoming);
  if (middleware.handleOutgoing) this.outgoingMiddleware.push(middleware.handleOutgoing);
  return this;
}
```
- example usage
```shell
...
 if ( ! process.env.RABBITMQ_URL)
   throw new Error('Tests require a RABBITMQ_URL environment variable to be set, pointing to the RabbiqMQ instance you wish to use
.');

 var busUrl = process.env.RABBITMQ_URL

 var bus = require('../').bus({ url: busUrl });

 bus.use(bus.package());
 bus.use(bus.correlate());
 bus.use(bus.logger());

 module.exports.bus = bus;
'''

Middleware may define one or two functions to modify incoming or outgoing messages:
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
