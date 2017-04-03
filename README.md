This is a fork of rslurp from Thomas Habets. It seems to need some updating and I've been looking for a project to cut my teeth on go. So I'm gonna give this a whirl.

rslurp
======

A simple full-directory HTTP downloader.

Copyright 2013 Google Inc. All Rights Reserved.
Apache 2.0 license.

This is NOT a Google product.

Contact: jlkaiser@gmail.com
https://github.com/jlkaiser/

Reason for existing
-------------------
wget -nd -np -r creates garbage files (index*), isn't parallel, and to my
knowledge can't restrict itself to a subset of files. Also it's spammy in its
status output.

Building
--------
In a temporary dir:
```
GOPATH="$(pwd)" go get github.com/jlkaiser/slurpit/rslurp
cp bin/rslurp /usr/local/bin/
```

Example use
-----------
```
rslurp -workers=5 -matching='jpg$' http://foo.com/images/ http://foo.com/static/
```
