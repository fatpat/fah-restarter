# folding@home client retstarter

This little script connects to the Folding@home client (FAHClient) and watches its logs.
When it catches `Could not get an assignment` during `TIMEOUT` seconds (5 minutes by
default) it pauses the corresponding FS for `WAIT` seconds (1 minute by default).

Sometimes it helps to recover for having the client doing nothing looping with
`Could not get an assignment` exceptions.

See usage to change default information:
- `HOST`: `127.0.0.1`
- `PORT`: `36330`
- `AUTH`: `unset`
- `TIMEOUT`: `300`
- `WAIT`: `60`

## Usage
```
usage: FAHRestarter [-h] [-H HOST] [-P PORT] [-A AUTH] [-v] [-d] [-t TIMEOUT]
                    [-w WAIT]

optional arguments:
  -h, --help            show this help message and exit
  -H HOST, --host HOST  Client host/ip
  -P PORT, --port PORT  Client port
  -A AUTH, --auth AUTH  Client password if any
  -v, --verbose         Verbose
  -d, --debug           Debug
  -t TIMEOUT, --timeout TIMEOUT
                        Timeout before stopping FS
  -w WAIT, --wait WAIT  Time to wait before restarting FS
```

## License
Some code has been imported from FAHControl which uses GPLv3.
This project use the same.

See LICENSE file.
