Heroku buildpack: heroku-buildpack-ffmpeg-ffprobe
======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks)
for adding ffmpeg and ffprobe to your application.

Multipacks
----------

More likely, you'll want to use it as part of a larger project, which needs to use ffmpeg and ffprobe. The easiest way to do this is with a [multipack](https://github.com/ddollar/heroku-buildpack-multi),
where this is just one of the buildpacks you'll be working with.

Thanks to [jonathanong](https://github.com/jonathanong) for static build of [ffmpeg](https://johnvansickle.com/ffmpeg/)

    $ cat .buildpacks
    git://github.com/heroku/heroku-buildpack-ruby.git
    git://github.com/hasibulkabir/heroku-buildpack-ffmpeg-ffprobe.git

    $ heroku config:add BUILDPACK_URL=git://github.com/ddollar/heroku-buildpack-multi.git

By this you can use ffmpeg and ffprobe command.

### Another method
    heroku config:add BUILDPACK_URL=git://github.com/HasibulKabir/heroku-buildpack-ffmpeg-ffprobe.git"
