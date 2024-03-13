# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
from http.server import HTTPServer, BaseHTTPRequestHandler
```
<html>
<head>
<title align="centre">TOP SOFTWARE COMPANIES WITH REVENUE TABLE </title>
</head>
<body>
  

TOP SOFTWARE COMPANIES WITH REVENUE TABLE 
<table border="3" cellspacing="4" cellpadding="6" height="500" width="1000">
<caption >TOP FIVE REVENUE GENERATING SOFTWARE COMPANY</caption>
<tr>
			<th>COMPANY NAME</th>
			<th>POSITION</th>
			<th>GOOD RATING</th>
		</tr>
		<tr>
			<td>TATA</td>
			<td>10th</td>
			<td>9.9</td>



		</tr>

		<tr>
			<td>JIO</td>
			<td>3rd</td>
			<td>9.8</td>

		</tr>

		<tr>
			<td>VI</td>
			<td>22th</td>
			<td>9.7</td>
		</tr>
<tr>
			<td>bsnl</td>
			<td>100rd</td>
			<td>9.8</td>

		</tr>

		<tr>
			<td>artiel</td>
			<td>2nd</td>
			<td>9.7</td>
		</tr>
	</table>
	</body>
</html>
</body>
</html>
```
```
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
## OUTPUT:
![WhatsApp Image 2024-03-13 at 08 17 47_54e8dede](https://github.com/ARAVIND23005370/simplewebserver/assets/148514836/a2d59052-0a9f-4270-8b06-fc29e4e439c0)

![WhatsApp Image 2024-03-13 at 08 17 59_985870b2](https://github.com/ARAVIND23005370/simplewebserver/assets/148514836/b84cee57-70e5-4069-ad04-76fcbe85a6c0)

## RESULT:
The program for implementing simple webserver is executed successfully.
