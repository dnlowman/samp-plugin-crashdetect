[CrashDetect][github]
=====================

[![Donate][donate_button]][donate]
[![Build Status][build_status]][build]

This plugin helps you debug runtime errors and server crashes. When something
goes wrong you see a more or less detailed error message that contains a
description of the error and a stack trace.

See the [original][forum] topic on the SA-MP Forums for more information and
examples.

Download
--------

Get latest binaries for Windows and Linux [here][download].

Settings
--------

CrashDetect settings can be changed via the following `server.cfg` options:

* `trace <flags>`

  Enables function call tracing.

  If enabled, CrashDetect will show information about every function call in
  all running scripts, such as the name of the function being called and the
  values of its parameters.

  `flags` may be one or combination of the following:

  * `n` - trace native functions
  * `p` - trace public functions
  * `f` - trace normal functions (i.e. all non-public functions)

  For example, `trace pn` will trace both public and native calls, and
  `trace pfn` will trace all functions.

* `trace_filter <regexp>`

  Filters `trace` output based on a regular expression.

  Examples:

  * `trace_filter Player`     - output functions whose name contains `Player`
  * `trace_filter playerid=0` - show functions whose `playerid` parameter is 0

License
-------

Licensed under the 2-clause BSD license. See the LICENSE.txt file.

[github]: https://github.com/Zeex/samp-plugin-crashdetect
[donate]: http://pledgie.com/campaigns/19750
[donate_button]: http://www.pledgie.com/campaigns/19750.png
[build]: https://travis-ci.org/Zeex/samp-plugin-crashdetect
[build_status]: https://travis-ci.org/Zeex/samp-plugin-crashdetect.png?branch=master
[forum]: http://forum.sa-mp.com/showthread.php?t=262796
[download]: https://github.com/Zeex/samp-plugin-crashdetect/releases
