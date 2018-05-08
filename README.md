# Installation

* Enable the papertrail module.
* Add the following to your services.yml to have logging enabled for both syslog and papertail.

```
parameters:
  monolog.channel_handlers:
    # Log to the syslog by default.
    default: ['syslog', 'papertrail']
    # Ignore log entries of "content" channel.
    content: ['null']

  papertrail.host: '[HOST].papertrailapp.com'
  papertrail.port: [PORT]
```
