# Residential Parking Permits

I ended up publishing this on [myStatesman](http://www.mystatesman.com/interactive/news/residential-permit-parking-map/) instead of projects so it could be metered.

## Deets
* Info came city of Austin through Lilly Rockwell.
* Addresses were in a weird format, so I used a combination of [Parserator](https://parserator.datamade.us/) and regex to get them in a decent order. Much hand editing as well.
* Map is via Google Fusion Tables in the statcomdata account. Residential Permit Blocks.



## Mobile and Social

* width is 100% on all devices. Standard social buttons.

Single-page project
==============================

Framework for a single page project, though it could be multiple pages. Just less complex than our immersive-template setup.

## Steps when you set up a project

* use `package.json` and `npm install`
* use `bower.json` and `bower install`
* use a public folder for the published files:
	* assets: images and other accces
	* dist: where js and css is compiled
	* fonts: for font-awesome
	* includes: files for metrics, advertising and other includes
* use a src for build components
	* js: for project specific files
	* less: for less css source files.

## Configurations

### ftpush

The path is in `Gruntfile.js`. Add the username/password into a file called `.ftppass` as per [ftpush docs](https://www.npmjs.com/package/grunt-ftpush). Make sure that file is in the .gitignore.


```
{
  "key": {
    "username": "username",
    "password": "password"
  }
}
```

### slack msg

The `grunt-slack-hook` plugin let's us publish finished url to slack as part of ftpush. Needs a .slack file with the Webhook URL from Slack configurations. Just a single line with that url and no return.
