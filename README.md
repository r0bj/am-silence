# am-silence

Alertmanager add/delete silences

```
usage: am-silence --labels=LABELS [<flags>]

Flags:
      --help                     Show context-sensitive help (also try --help-long and --help-man).
  -m, --mode="add"               work mode: add/delete silence
      --silence-period=7200      default period for silenced alerts in seconds
  -l, --labels=LABELS            comma separated silence matching labels, eg. key1=value1,key2=value2
  -c, --creator="auto-silencer"  creator of the silence
  -C, --comment="auto-silencer"  comment attached to the silence
  -u, --URL="http://127.0.0.1"   Alertmanager URL
  -t, --timeout=3                Alertmanager connection timeout
      --version                  Show application version.
```
