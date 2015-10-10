pyotrcut
========

pyotrcut is an interactive CLI tool to cut TV recordings from [OnlineTVRecorder](http://www.onlinetvrecorder.com)
using the cutlists from [cutlist.at](http://www.cutlist.at). Contrary to other
tools, it uses [avcut](https://github.com/anyc/avcut) for frame-accurate cuts
of h264 videos.

Usage
-----

`usage: pyotrcut [-h] [-s START_OFFSET] filename`

pyotrcut shows a list of available cutlists from cutlist.at and calculates
the cutpoints for the selected cutlist.

It looks like the cutlists meant for VirtualDub cause slightly inaccurate cuts.
Hence, a user can specify a offset that is added to the start timestamps.
In our experiments, adding 0.1s with `-s 0.1` worked well.