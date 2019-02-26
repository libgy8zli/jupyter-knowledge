### configure jupyter
 - generate config file or copy your own to ~/.jupyter/jupyter_notebook_config.py
  ```
  jupyter notebook --generate-config
  ```
 - create hashed password, enter password and save the hashed string 
  ```
  from notebook.auth import passwd
  passwd()
  ```
 - create self-signed ssl cretificate 
  ```
  openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mykey.key -out mycert.pem
  ```
  
 sample configure file:
   ```
# Set options for certfile, ip, password, and toggle off
# browser auto-opening
c.NotebookApp.certfile = u'/absolute/path/to/your/certificate/mycert.pem'
c.NotebookApp.keyfile = u'/absolute/path/to/your/certificate/mykey.key'
# Set ip to '*' to bind on all interfaces (ips) for the public server
c.NotebookApp.ip = '*'
c.NotebookApp.password = u'sha1:bcd259ccf...<your hashed password here>'
c.NotebookApp.open_browser = False
# It is a good idea to set a known, fixed port for server access
c.NotebookApp.port = 9999 
   ```
