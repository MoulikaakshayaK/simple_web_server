# EX01 Developing a Simple Webserver

# Date:11-03-2025
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
NAME:Moulika Akshaya K

REGISTER NUMBER:212224040203
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Welcome<h1>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

# OUTPUT:
![image](https://github.com/user-attachments/assets/36976065-f73d-4efc-9b79-912787e91438)

![image](https://github.com/user-attachments/assets/ca307cd0-bb50-40ff-9787-457196f70977)


# RESULT:
The program for implementing simple webserver is executed successfully.
