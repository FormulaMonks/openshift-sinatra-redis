# OpenShift-Sinatra-Redis

An OpenShift QuickStart for Ruby / Sinatra / Redis.

## Thanks
This QuickStart is based on the OpenShift Sinatra Example at https://github.com/openshift/sinatra-example .
Our Redis OpenShift Cart is by https://github.com/smarterclayton/openshift-redis-cart


## Installation

Requires rbenv. Install with "brew install rbenv" if you have Homebrew installed. http://brew.sh/

```
git clone git@github.com:citrusbyte/openshift-sinatra-redis.git
cd openshift-sinatra-redis
gem install rhc
rbenv rehash
```



## Creating an OpenShift Application

```
rhc app create APPNAME ruby-1.9 --from-code https://github.com/citrusbyte/openshift-sinatra-redis.git
rhc add-cartridge http://cartreflect-claytondev.rhcloud.com/reflect?github=smarterclayton/openshift-redis-cart
```

The "rhc app create" command should have output the URL to access your application on OpenShift.

