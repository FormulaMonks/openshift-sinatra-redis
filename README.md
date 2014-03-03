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
ib```

The "rhc app create" command should have output the URL to access your application on OpenShift.




## Running this application locally

Before running any of these examples, you should run the below command to make sure that you have the correct ruby gems installed

```
  cd citrusbytesinatra
  bundle install
```

You will also need to have Redis installed and running locally. On OS X, I installed it with "brew install redis". That command gives examples on how to start the redis server.

You'll need to set the following environment variables:
* OPENSHIFT_REDIS_HOST
* OPENSHIFT_REDIS_PORT
* REDIS_PASSWORD

To run this application locally, cd into the citrusbyte-sinatra directory that you cloned and run

    bundle exec ruby -S rackup -w config.ru

