# EX01 Developing a Simple Webserver

# Date:19 09 2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content ='''
<!DOCTYPE html>
<html>
<head>
  <title>TCP/IP Protocol</title>
  <style>
    table {
      width: 70%;
      height:50%;
      margin: 20px auto;
      font-family:"Times New Roman",serif,georgia;
    }

    th {
      background-color:aqua;
      color:black;
    }
    caption {
      font-weight: bold;
    }
    td
    {
    background-color:black;
    color:white;
    }

  </style>
</head>
<body bgcolor="white">
  <table border="2.5">
    <caption ><b>TCP/IP Protocol Suite</b></caption>
    <tr>
      <th color="black">Layer</th>
      <th>Function</th>
      <th>Common Protocols</th>
    </tr>
    <tr>
      <td>Application</td>
      <td>Provides services to user applications</td>
      <td>HTTP, FTP, SMTP, DNS, DHCP, SNMP</td>
    </tr>
    <tr>
      <td>Transport</td>
      <td>Reliable or fast data transmission</td>
      <td>TCP, UDP</td>
    </tr>
    <tr>
      <td>Internet</td>
      <td>Routing and logical addressing</td>
      <td>IP, ICMP, ARP, RARP</td>
    </tr>
    <tr>
      <td>Network Access</td>
      <td>Physical data transmission</td>
      <td>Ethernet, Wi-Fi, PPP</td>
    </tr>
  </table>
</body>
</html>
'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()
```
# OUTPUT:
<img width="1920" height="1080" alt="p1" src="https://github.com/user-attachments/assets/c06fde6e-54c5-4435-81e5-e904b07d4b3b" />

<img width="1396" height="398" alt="p2" src="https://github.com/user-attachments/assets/5a250980-ebc5-4e9d-b91b-867bb5e52543" />






# RESULT:
The program for implementing simple webserver is executed successfully.
