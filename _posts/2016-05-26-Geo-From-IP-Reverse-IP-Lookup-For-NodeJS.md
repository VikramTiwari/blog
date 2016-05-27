---
layout: post
title: Geo-From-IP — Reverse IP lookup for NodeJS
date: '2016-05-26 10:50:00 -0800'
categories: tech nodejs
---

For a web service, either if it's a website or api or a web app, there are often times when you wanna use user's geolocation for a variety of use cases. Location based content curation, finding points of interest in user's area and location tagged status updates in social media to name a few.

Next challenge is to get this data. One way to do that is to use IP address of user and do a reverse IP lookup using some database. [MaxMind's GeoIP database](http://dev.maxmind.com/geoip/geoip2/geolite2/) is one of the most famous ones in the category. But one of the biggest challenges to using such a database is to keep them up-to date with current versions.

If you are building a NodeJS based API, [Geo-From-IP](https://www.npmjs.com/package/geo-from-ip) is here to help you in that. Few features:

- No frills install
- Downloads databases automatically during installation
- Run `npm install` to upgrade databases == automatic update on deployments

And it's really easy to use it. Just include package in your project by running:

```sh
npm install --save geo-from-ip
```

And then its easy cheesy:

```javascript
let geoip = require('geo-from-ip');
console.log(geoip.allData('199.188.195.120'));
```

This will give you geo data in JSON format:

```sh
{ code: { state: 'CA', country: 'US', continent: 'NA' },
  city: 'San Francisco',
  state: 'California',
  country: 'United States',
  continent: 'North America',
  postal: '94103',
  location:
   { accuracy_radius: 10,
     latitude: 37.7758,
     longitude: -122.4128,
     metro_code: 807,
     time_zone: 'America/Los_Angeles' } }
```

And you are done! Use this in your application logic to server your users in best possible manner.

Now whenever app gets deployed using a CI, if the database is at a lower version than deployed app, it gets updated to latest version. You can also force it to download latest version by running:

``` sh
npm install
```
in project directory. No need to manage file names and keeping tab on monthly updates.

Enjoy the package! If you have any comments, issues or suggestions, feel free to raise an issue on [GitHub](https://github.com/VikramTiwari/geo-from-ip/issues/new).
