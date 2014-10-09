# Network Configuration

## Log Drain Blacklists

The loggregator component allows application log drains.
An application developer deploying their app to Cloud Foundry can bind a drain
to a log analysis service.

Your cloud performance can be affected if the application developer attempts to bind that drain to an internal Cloud Foundry component

To guard against this, you can blacklist the range of IP addresses that you allocate to Cloud Foundry components in your manifest.

To blacklist an IP address range, add the `loggregator.blacklisted_syslog_ranges` property to your manifest.
Specify starting and ending IP addresses for each IP address range.

Example manifest excerpt:

```
properties:
  ... other properties ...

  loggregator:
    blacklisted_syslog_ranges:
    - start: 10.10.16.0
      end: 10.10.31.255
    - start: 10.10.80.0
      end: 10.10.95.255
```

