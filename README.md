# automagic.py

## Example usage
```py
from pathlib import Path
from automagic import AutoMagic
from automagic.host import Host
from urllib.parse import urlparse
from automagic.tools import log

hosts = [
    Host("tablet", urlparse("http://my.tablet:1122", password="123")),
    Host("handy", urlparse("http://192.168.2.36:1122", password="456"))
]
am = AutoMagic(hosts)
log(str(am))

am.backup_flows(Path("devices"))
```
