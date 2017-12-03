Certificate Monitor
===================

## What is this?

This script monitors the ssl certificates expiration date and send you an email for eache certificate due to expire in the next weeks.

It currently handlex certificates configures in apache, dovecot and postfix.

## Installation

Simply copy certificate-monitor to your /etc/cron.daily directory and make it executable.

Configure the script by adjusting the variables on top of it.

## Usage

```
USAGE: certificate-monitor [-h] [-d] [-e <warning_time>] [-m] [-f <sender>] [-t <destination>] [-s] [-q]

Options:
  -h, --help    print usage message and exit
  -d, --debug   debug mode, show expiration date of older certs even if not in warning time period (only on STDOUT)
  -e <time>,    warn if cert expires in the given time period
  --expirein <time>
  -m, --mail    send warning by mail
  -f <sender>,  set warning mail sender address
  --from <sender>
  -t <dest>,    set warning mail destination address
  --to <dest>
  --nomail      do NOT send warning by mail even if enabled by default
  -s, --stdout  show warnings on stdout
  -q, --quiet   do NOT show warnings on stdout, even if enabled by default
```

