# Dokku-Single-App

Dokku-Single-App is a [Dokku](https://github.com/progrium/dokku) plugin designed to allow you to host a single Dokku deployed app on port 80 without using virtual hosts.

This will play well with zero downtime deploys, as it simply redirects 80 to the Dokku host port

__Right now, this requires you to allow all users to use the iptables command!__
__This could be very dangerous!__

## Setup

```
chmod u+s /sbin/iptables
cd /var/lib/dokku/plugins
git clone https://github.com/dudeofawesome/dokku-single-app.git
dokku plugins-install
```

Now, just restart your app.
