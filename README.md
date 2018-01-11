Bumps buffers when there is activity on them, replicating the functionality of most mainstream chat programs.

# Examples
`autobump.py` works out of the box, but you can grant higher or lower priority to certain buffers. For example, to make any channel on network "freenode" or any channel named "#test" low priority:

```
/set var.plugins.python.autobump.lowprio_buffers "irc.freenode.*,*#test*"
```

You can also grant high priority with `var.plugins.python.autobump.highprio_buffers`. By default, high priority is granted to `irc.server.*,core.weechat`.

The syntax for the buffer list is identical to the one used for filters. See `/help filter` for further documentation.

As a shortcut, you can run `/autobump add high`, `autobump del high`, `autobump add low`, `autobump del low`, to add/delete the current buffer to the high/low priority list.
