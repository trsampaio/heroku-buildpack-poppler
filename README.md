Heroku buildpack: Poppler
=======================

This [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) provides Poppler.

It should be used with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi).

## Current version

* Fontconfig 2.10.2
* Poppler 0.22.0

## How to compile Poppler by yourself?

To run a custom binary on Heroku, you need to compile it on their servers.
Set up a [vulcan build server](https://github.com/heroku/vulcan) with [this pull request applied](https://github.com/heroku/vulcan/pull/50).

After this, you can run the rake tasks defined in the right order.

```bash
bundle execute rake -T
```

Upload the files to Amazon S3 and reference your bucket and the new version in /bin/compile 

## Credits

This buildpack is maintained and funded by [BauCloud][]. Thank you to all the contributors.
[BauCloud]: http://www.baucloud.com
