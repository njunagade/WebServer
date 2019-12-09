# WebServer
Server running an Amazon AWS EC2 instance

# Instructions

1) Please download the Key-Pair file into your Downloads folder
2) Change permissions to allow execution of my-ohio-kp.pem -> chmod 400 my-ohio-kp.pem
3) SSH into the EC2 instance -> ssh -i "my-ohio-kp.pem" ec2-user@ec2-3-14-71-168.us-east-2.compute.amazonaws.com
4) Install Nginx -> yum install nginx
5) Launch nginx -> service nginx start
5) Change directory into /usr/share/nginx/html -> cd /usr/share/nginx/html
6) Create HTML file to deploy content -> vi index.html
7) Set-paste this HTML code to allow NGINX to deploy content ->

<!DOCTYPE html>
<html>
<body>

<p>Click the button to display the hostname of this server</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x = "ByteCubed Challenge ${"+window.location.hostname+"}";
  document.getElementById("demo").innerHTML= x;
}
</script>

</body>
</html>

8) Input the IPv4 address of the EC2 instance in your browser -> https://3.14.71.168
9) Click "Try it" button to output your hostname
