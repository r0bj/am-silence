# am-silence

Alertmanager add/delete silences

```
usage: am-silence [<flags>]

Flags:
      --help                     Show context-sensitive help (also try --help-long and --help-man).
  -m, --mode="show"              work mode: add/delete/show silence
      --silence-period=7200      default period for silenced alerts in seconds
  -l, --labels=LABELS            comma separated silence matching labels, eg. key1=value1,key2=value2
  -c, --creator="auto-silencer"  creator of the silence
  -C, --comment="auto-silencer"  comment attached to the silence
  -u, --URL="http://127.0.0.1"   Alertmanager URL
  -t, --timeout=3                Alertmanager connection timeout
      --version                  Show application version.
```

# Example
```
$ am-silence -u http://alertmanager.example.com -l job=mysql,instance=10.200.0.102 -m add
Adding silence [creator: auto-silencer, comment: auto-silencer, start: 2018-02-15T20:42:17Z, end: 2018-02-15T22:42:17Z]

$ am-silence -u http://alertmanager.example.com -l job=mysql,instance=10.200.0.102 -m delete
Deleting silence [creator: auto-silencer, comment: auto-silencer, start: 2018-02-15T20:42:17.961780991Z, end: 2018-02-15T22:42:17Z]
```
