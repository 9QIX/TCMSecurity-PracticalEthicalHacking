# Starting and Stopping Services

- Services are programs like web servers, SSH, or databases[1]
- To start a service, use the command `service <service-name> start`[1]
- To stop a service, use `service <service-name> stop`[1]
- Services are not automatically started on boot by default[1]

## Permanently Enabling Services on Boot

- To enable a service to start on boot, use `systemctl enable <service-name>`[1]
- This is useful for important services like databases that should always be running[1]
- For example, to enable the PostgreSQL database to start on boot:
  ````bash
  systemctl enable postgresql
  ```[1]
  ````

## Spinning Up a Simple Web Server with Python

- An easy way to quickly serve files is using Python's built-in HTTP server module[1]
- Run `python -m http.server 8000` to start a web server on port 8000 in the current directory[1]
- This avoids the need to configure Apache or edit web server config files[1]

## Challenges

- Try figuring out how to spin up an FTP server using Python as an exercise[1]
- Metasploit is a popular penetration testing framework that often uses a database like PostgreSQL, so enabling it on boot can save time[1]
