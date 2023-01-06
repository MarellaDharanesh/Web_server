# Developing a Simple Webserver

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<hl>Welcome</hl>
<h1>Marella Dharanesh</h1>
<h1>22000785</h1>
</body>
<html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address=('',80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()


# OUTPUT:
![model](/WhatsApp%20Image%202023-01-06%20at%201.15.22%20PM.jpeg)

# RESULT:

The program is executed succesfully