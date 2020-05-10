# CVE-2020-8816
A Python script to exploit CVE-2020-8816, a remote code execution vulnerability on the Pi-hole.

This script uses the techniques found by [François Renaud-Philippon](https://natedotred.wordpress.com/2020/03/28/cve-2020-8816-pi-hole-remote-code-execution/) to achieve remote code execution on a [Pi-hole](https://pi-hole.net/) running a web interface version less than 4.3.3. The exploit requires the path for the www-data user to be `/opt/pihole:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`.

```
> python3 .\CVE-2020-8816.py -h
usage: CVE-2020-8816.py [-h] url password ip port

Receive a reverse shell on a Pi-hole with access to the admin web console

positional arguments:
  url         The URL of the Pi-hole console
  password    The admin password for the Pi-hole console
  ip          The IP address for the reverse shell to connect to
  port        The port for the reverse shell to connect to

optional arguments:
  -h, --help  show this help message and exit
```

![The script in action](example.gif "The script in action")