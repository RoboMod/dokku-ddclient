# dokku-ddclient
Adds ddclient as DynDNS-option to dokku

## Install

### Plugin

```
dokku plugin:install https://github.com/robomod/dokku-ddclient.git ddclient
```

### ddclient

```
dokku plugin:install-dependencies 
```

## Configuration

Set DynDNS provider parameters

```
dokku ddclient:set:server <server>  (required before use!)
dokku ddclient:set:login <login>  (required before use!)
dokku ddclient:set:password <password>  (required before use!)

dokku ddclient:set:protocol <protocol>  (default: dyndns2)
dokku ddclient:set:use <use>  (default: web)
dokku ddclient:set:delay <delay> (seconds; default: 300)
dokku ddclient:set:ssl <yes|no> (default: yes)
```

## Usage

After installation, configure server, login and password. On each domain update the ddclient configuration is recreated. The ddclient daemon will be started automatically.
