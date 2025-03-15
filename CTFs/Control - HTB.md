
nmap -sCV -T4 -p- -Pn 10.129.87.57 -vv           
Starting Nmap 7.95 ( https://nmap.org ) at 2025-03-15 08:32 EDT
NSE: Loaded 157 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:32
Completed NSE at 08:32, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:32
Completed NSE at 08:32, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:32
Completed NSE at 08:32, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 08:32
Completed Parallel DNS resolution of 1 host. at 08:32, 0.01s elapsed
Initiating SYN Stealth Scan at 08:32
Scanning 10.129.87.57 [65535 ports]
Discovered open port 80/tcp on 10.129.87.57
Discovered open port 135/tcp on 10.129.87.57
Discovered open port 3306/tcp on 10.129.87.57
SYN Stealth Scan Timing: About 22.12% done; ETC: 08:34 (0:01:49 remaining)
SYN Stealth Scan Timing: About 63.85% done; ETC: 08:33 (0:00:35 remaining)
Discovered open port 49666/tcp on 10.129.87.57
Discovered open port 49667/tcp on 10.129.87.57
Completed SYN Stealth Scan at 08:34, 108.28s elapsed (65535 total ports)
Initiating Service scan at 08:34
Scanning 5 services on 10.129.87.57
Completed Service scan at 08:34, 54.20s elapsed (5 services on 1 host)
NSE: Script scanning 10.129.87.57.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:34
Completed NSE at 08:35, 5.10s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:35
Completed NSE at 08:35, 0.34s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:35
Completed NSE at 08:35, 0.00s elapsed
Nmap scan report for 10.129.87.57
Host is up, received user-set (0.037s latency).
Scanned at 2025-03-15 08:32:12 EDT for 168s
Not shown: 65530 filtered tcp ports (no-response)
PORT      STATE SERVICE REASON          VERSION
80/tcp    open  http    syn-ack ttl 127 Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-title: Fidelity
|_http-server-header: Microsoft-IIS/10.0
135/tcp   open  msrpc   syn-ack ttl 127 Microsoft Windows RPC
3306/tcp  open  mysql   syn-ack ttl 127 MariaDB 10.3.24 or later (unauthorized)
49666/tcp open  msrpc   syn-ack ttl 127 Microsoft Windows RPC
49667/tcp open  msrpc   syn-ack ttl 127 Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:35
Completed NSE at 08:35, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:35
Completed NSE at 08:35, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:35
Completed NSE at 08:35, 0.00s elapsed
Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 168.62 seconds
           Raw packets sent: 131144 (5.770MB) | Rcvd: 75 (3.300KB)


####homepage index.php
<!DOCTYPE html>
<html lang="en">

<head>
	<title>Fidelity</title>
	<meta charset="utf-8">
	<script type="text/javascript" src="assets/js/functions.js"></script>
	<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
	<link rel="stylesheet" href="assets/css/main.css" />
	<noscript>
		<link rel="stylesheet" href="assets/css/noscript.css" /></noscript>
</head>

<body class="is-preload landing">
	<div id="page-wrapper">
		<!-- To Do:
			- Import Products
			- Link to new payment system
			- Enable SSL (Certificates location \\192.168.4.28\myfiles)
		<!-- Header -->
		<header id="header">
			<h1 id="logo"><a href="index.php">Fidelity</a></h1>
			<nav id="nav">
				<ul>
					<li><a href="index.php">Home</a></li>
					<li><a href="about.php">About</a></li>
					<li><a href="admin.php">Admin</a></li>
					<li><a href="admin.php" class="button primary">Login</a></li>
				</ul>
			</nav>
		</header>

		<!-- Banner -->
		<section id="banner">
			<div class="content">
				<header>
					<h2>The future has landed</h2>
					<p>And there are no hoverboards or flying cars.<br />
						Just apps. Lots of mother flipping apps.</p>
				</header>
				<span class="image"><img src="images/pic01.jpg" alt="" /></span>
			</div>
		</section>

		<!-- Search -->
		<section id="search" class="wrapper style2 special fade">
			<h4></h4>

			<div class="container">
				<header>
					<h2>Stay Tuned</h2>
					<p>Subscribe to our Newsletter</p>
				</header>
				<form id="subscribe" action="#" method="GET" class="cta">
					<div class="row gtr-uniform gtr-50">
						<div class="col-8 col-12-xsmall"><input type="text" placeholder="Email" /></div>
						<div class="col-4 col-12-xsmall"><input type="submit" value="Subscribe" class="fit primary" /></div>
					</div>
				</form>
			</div>
		</section>
		<!-- Footer -->
		<footer id="footer">
			<ul class="icons">
				<li><a href="#" class="icon brands alt fa-twitter"><span class="label">Twitter</span></a></li>
				<li><a href="#" class="icon brands alt fa-facebook-f"><span class="label">Facebook</span></a></li>
				<li><a href="#" class="icon brands alt fa-linkedin-in"><span class="label">LinkedIn</span></a></li>
				<li><a href="#" class="icon brands alt fa-instagram"><span class="label">Instagram</span></a></li>
				<li><a href="#" class="icon brands alt fa-github"><span class="label">GitHub</span></a></li>
				<li><a href="#" class="icon solid alt fa-envelope"><span class="label">Email</span></a></li>
			</ul>
			<ul class="copyright">
				<li>&copy; Fidelity. All rights reserved.</li>
			</ul>
		</footer>

	</div>
	<!-- Scripts -->
	<script src="assets/js/jquery.min.js"></script>
	<script src="assets/js/jquery.scrolly.min.js"></script>
	<script src="assets/js/jquery.dropotron.min.js"></script>
	<script src="assets/js/jquery.scrollex.min.js"></script>
	<script src="assets/js/browser.min.js"></script>
	<script src="assets/js/breakpoints.min.js"></script>
	<script src="assets/js/util.js"></script>
	<script src="assets/js/main.js"></script>
</body>

</html>

![[Pasted image 20250315085946.png]]



####about page about.php

<!DOCTYPE html>
<html lang="en">

<head>
	<title>Fidelity</title>
	<meta charset="utf-8">
	<script type="text/javascript" src="assets/js/functions.js"></script>
	<script type="text/javascript" src="assets/js/checkValues.js"></script>
	<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
	<link rel="stylesheet" href="assets/css/main.css" />
	<noscript>
		<link rel="stylesheet" href="assets/css/noscript.css" />
	</noscript>
</head>

<body class="is-preload landing">
	<div id="main" class="wrapper style1">
		<div class="container">

			<!-- Header -->
			<header id="header">
				<h1 id="logo"><a href="index.php">Fidelity</a></h1>
				<nav id="nav">
					<ul>
						<li><a href="index.php">Home</a></li>
						<li><a href="about.php">About</a></li>
						<li><a href="admin.php">Admin</a></li>
						<li><a href="#" class="button primary">Logout</a></li>
					</ul>
				</nav>
			</header>

			<!-- One -->
			<section id="one" class="spotlight style1 bottom">
				<span class="image fit main"><img src="images/bg.jpg" alt="" /></span>
				<div class="content">
					<div class="container">
						<div class="row">
							<div class="col-4 col-12-medium">
								<header>
									<h2>The Wifi of the future.</h2>
									<p>Control your networks.</p>
								</header>
							</div>
							<div class="col-4 col-12-medium">
								<p>Feugiat accumsan lorem eu ac lorem amet sed accumsan donec.
									Blandit orci porttitor semper. Arcu phasellus tortor enim mi
									nisi praesent dolor adipiscing. Integer mi sed nascetur cep aliquet
									augue varius tempus lobortis porttitor accumsan consequat
									adipiscing lorem dolor.</p>
							</div>
							<div class="col-4 col-12-medium">
								<p>Morbi enim nascetur et placerat lorem sed iaculis neque ante
									adipiscing adipiscing metus massa. Blandit orci porttitor semper.
									Arcu phasellus tortor enim mi mi nisi praesent adipiscing. Integer
									mi sed nascetur cep aliquet augue varius tempus. Feugiat lorem
									ipsum dolor nullam.</p>
							</div>
						</div>
					</div>
				</div>
				<a href="#two" class="goto-next scrolly">Next</a>
			</section>

			<!-- Two -->
			<section id="two" class="spotlight style2 right">
				<span class="image fit main"><img src="images/pic03.jpg" alt="" /></span>
				<div class="content">
					<header>
						<h2>Morbi accumsan sem ut magna pharetra finibus vel in tellus.</h2>
						<p>Nunc commodo accumsan eget id nisi eu col volutpat magna</p>
					</header>
					<p>Feugiat accumsan lorem eu ac lorem amet ac arcu phasellus tortor enim mi mi nisi praesent adipiscing. Integer mi sed nascetur cep aliquet augue varius tempus lobortis porttitor lorem et accumsan consequat adipiscing lorem.</p>
					<ul class="actions">
						<li><a href="#" class="button">Learn More</a></li>
					</ul>
				</div>
				<a href="#three" class="goto-next scrolly">Next</a>
			</section>

			<!-- Three -->
			<section id="three" class="spotlight style3 left">
				<span class="image fit main bottom"><img src="images/pic04.jpg" alt="" /></span>
				<div class="content">
					<header>
						<h2>Nunc eu ultricies ipsum</h2>
						<p>Sed ac diam vel odio facilisis accumsan facilisis nec purus</p>
					</header>
					<p>Feugiat accumsan lorem eu ac lorem amet ac arcu phasellus tortor enim mi mi nisi praesent adipiscing. Integer mi sed nascetur cep aliquet augue varius tempus lobortis porttitor lorem et accumsan consequat adipiscing lorem.</p>
					<ul class="actions">
						<li><a href="#" class="button">Learn More</a></li>
					</ul>
				</div>
				<a href="#four" class="goto-next scrolly">Next</a>
			</section>

			<!-- Four -->
			<section id="four" class="wrapper style1 special fade-up">
				<div class="container">
					<header class="major">
						<h2>Choose Fidelity</h2>
						<p>Iaculis ac volutpat vis non enim gravida nisi faucibus posuere arcu consequat</p>
					</header>
					<div class="box alt">
						<div class="row gtr-uniform">
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-chart-area"></span>
								<h3>Nam orci nisi.</h3>
								<p>Nulla sem massa, suscipit non condimentum id, malesuada nec erat.</p>
							</section>
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-comment"></span>
								<h3>Get Help!</h3>
								<p>Nullam convallis a lacus a dictum.</p>
							</section>
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-flask"></span>
								<h3>Nunc a velit quam.</h3>
								<p>Aenean risus lorem, viverra in pretium ut, dignissim vel libero. Proin euismod velit in orci dapibus feugiat.</p>
							</section>
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-paper-plane"></span>
								<h3>Are you bored?</h3>
								<p>Nunc laoreet, quam vitae suscipit facilisis, sapien elit ultricies augue, vitae euismod lorem libero et erat.</p>
							</section>
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-file"></span>
								<h3>Pellentesque porttitor .</h3>
								<p>Mauris id sapien neque. Phasellus eu tempor magna. Phasellus dapibus dui id vulputate lacinia.</p>
							</section>
							<section class="col-4 col-6-medium col-12-xsmall">
								<span class="icon solid alt major fa-lock"></span>
								<h3>Cras sollicitudin.</h3>
								<p>Nunc eu ultricies ipsum. Sed ac diam vel odio facilisis accumsan facilisis nec purus.</p>
							</section>
						</div>
					</div>
					<footer class="major">
						<ul class="actions special">
							<li><a href="#" class="button">Sign up Now</a></li>
						</ul>
					</footer>
				</div>
			</section>

			<!-- Five -->
			<section id="five" class="wrapper style2 special fade">
				<div class="container">
					<header>
						<h2>Want to learn more?</h2>
						<p>Sign up for our Newsletter</p>
					</header>
					<form method="post" action="#" class="cta">
						<div class="row gtr-uniform gtr-50">
							<div class="col-8 col-12-xsmall"><input type="email" name="email" id="email" placeholder="Your Email Address" /></div>
							<div class="col-4 col-12-xsmall"><input type="submit" value="Get Started" class="fit primary" /></div>
						</div>
					</form>
				</div>
			</section>
			<!-- Footer -->
			<footer id="footer">
				<ul class="icons">
					<li><a href="#" class="icon brands alt fa-twitter"><span class="label">Twitter</span></a></li>
					<li><a href="#" class="icon brands alt fa-facebook-f"><span class="label">Facebook</span></a></li>
					<li><a href="#" class="icon brands alt fa-linkedin-in"><span class="label">LinkedIn</span></a></li>
					<li><a href="#" class="icon brands alt fa-instagram"><span class="label">Instagram</span></a></li>
					<li><a href="#" class="icon brands alt fa-github"><span class="label">GitHub</span></a></li>
					<li><a href="#" class="icon solid alt fa-envelope"><span class="label">Email</span></a></li>
				</ul>
				<ul class="copyright">
					<li>&copy; Fidelity. All rights reserved.</li>
				</ul>
			</footer>
		</div>
		<!-- Scripts -->
		<script src="assets/js/jquery.min.js"></script>
		<script src="assets/js/jquery.scrolly.min.js"></script>
		<script src="assets/js/jquery.dropotron.min.js"></script>
		<script src="assets/js/jquery.scrollex.min.js"></script>
		<script src="assets/js/browser.min.js"></script>
		<script src="assets/js/breakpoints.min.js"></script>
		<script src="assets/js/util.js"></script>
		<script src="assets/js/main.js"></script>
</body>

</html>

####admin admin.php

|   |   |
|---|---|
||Access Denied: Header Missing. Please ensure you go through the proxy to access this page|

able to gain access to admin page by using X-forwarded-for and the IP obtained from the about page


<!DOCTYPE html>
<html lang="en">

<head>
	<title>Fidelity</title>
	<meta charset="utf-8">
	<script type="text/javascript" src="assets/js/functions.js"></script>
	<script type="text/javascript" src="assets/js/checkValues.js"></script>
	<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
	<link rel="stylesheet" href="assets/css/main.css" />
	<noscript>
		<link rel="stylesheet" href="assets/css/noscript.css" />
	</noscript>
</head>

<body class="is-preload landing">
	<div id="main" class="wrapper style1">
		<div class="container">

			<!-- Header -->
			<header id="header">
				<h1 id="logo"><a href="index.php">Fidelity</a></h1>
				<nav id="nav">
					<ul>
						<li><a href="index.php">Home</a></li>
						<li><a href="about.php">About</a></li>
						<li><a href="admin.php">Admin</a></li>
						<li><a href="index.php" class="button primary">Logout</a></li>
					</ul>
				</nav>
			</header>

			<!-- Search -->
			<section>
				<div>
					<h2>Find Products</h2>
					<form id="searchProducts" action="search_products.php" method="POST">
						<div class="row gtr-uniform gtr-50">
							<div class="col-8 col-12-xsmall"><input type="text" name="productName" id="productName" placeholder="Name" /></div>
							<div class="col-4 col-12-xsmall"><input type="submit" value="Search" class="primary" /></div>

						</div>
					</form>
				</div>
			</section>

			<!-- Latest Products -->
			<section>
				<h2>Latest Products</h2>
				<div class="table-wrapper">
					<table border="1" cellpadding="10">
						<thead>
							<tr>
								<th>Name</th>
								<th>Quantity</th>
								<th>Action</th>
							</tr>
						</thead>
						<tbody>
							<form id="viewProducts" method="POST">
								<input type="hidden" id="productId" name="productId" value="" />
								<tr><td> D-Link DWA-171</td><td>5</td><td><div class="row"><button class="button  small" type="button" onclick="viewProduct(32)">View</button>&nbsp;<button class="button small" type="button" onclick="updateProduct(32)">Update</button>&nbsp;<button class="button  small" type="button" onclick="deleteProduct(32)">Delete</button></td></td></div></tr><tr><td>Asus USB-AC53 Nano</td><td>25</td><td><div class="row"><button class="button  small" type="button" onclick="viewProduct(34)">View</button>&nbsp;<button class="button small" type="button" onclick="updateProduct(34)">Update</button>&nbsp;<button class="button  small" type="button" onclick="deleteProduct(34)">Delete</button></td></td></div></tr><tr><td>Asus USB-AC68</td><td>5</td><td><div class="row"><button class="button  small" type="button" onclick="viewProduct(37)">View</button>&nbsp;<button class="button small" type="button" onclick="updateProduct(37)">Update</button>&nbsp;<button class="button  small" type="button" onclick="deleteProduct(37)">Delete</button></td></td></div></tr><tr><td>Cloud Server</td><td>2</td><td><div class="row"><button class="button  small" type="button" onclick="viewProduct(26)">View</button>&nbsp;<button class="button small" type="button" onclick="updateProduct(26)">Update</button>&nbsp;<button class="button  small" type="button" onclick="deleteProduct(26)">Delete</button></td></td></div></tr><tr><td>p</td><td>1</td><td><div class="row"><button class="button  small" type="button" onclick="viewProduct(38)">View</button>&nbsp;<button class="button small" type="button" onclick="updateProduct(38)">Update</button>&nbsp;<button class="button  small" type="button" onclick="deleteProduct(38)">Delete</button></td></td></div></tr>							</form>
						</tbody>
					</table>
				</div>
			</section>
			<!-- Create Product -->
			<section>
				<h2>Create Product</h2>
				<form id="createProduct" action="create_product.php" method="POST" onsubmit="return checkValues('createProduct')">
					<table border="1" cellpadding="10">
						<thead>
							<tr>
								<th>Name</th>
								<th>Quantity</th>
								<th>Category</th>
								<th>Price</th>
							</tr>
						</thead>
						<tbody>
							<td><input name="name" type="text" value="" /></td>
							<td><input name="quantity" type="text" value="" /></td>
							<td><select name="category">
									<option value="2">Adapters</option><option value="1">Default</option><option value="6">Monitors</option><option value="5">Servers</option>								</select>
							</td>
							<td>
								<input name="price" type="text" value="" />
							</td>
						</tbody>
					</table>
					<ul class="actions">
						<li><button type="submit" class="button primary small">Create</button></li>
					</ul>
				</form>
			</section>
			<br>
			<br>
			<!-- Categories -->
			<section>
				<h2>Categories</h2>
				<div class="table-wrapper">
					<table border="1" cellpadding="10">
						<thead>
							<tr>
								<th>Name</th>
								<th>Action</th>
							</tr>
						</thead>
						<tbody>
							<form id="categoryOptions" method="POST" onsubmit="return checkValues('updateCategory')">
								<input type="hidden" id="categoryId" name="categoryId" value="" />
								<tr><td>Default</td><td>Not Allowed</td></tr><tr><td><input name="name" type="text" value="Adapters" /></td><div class="col-3 col-6-medium col-12-xsmall"><td><button class="button small" type="button" onclick="updateCategory(2)">Update</button>&nbsp;<button class="button small" type="button" onclick="deleteCategory(2)">Delete</button></td></tr><tr><td><input name="name" type="text" value="Servers" /></td><div class="col-3 col-6-medium col-12-xsmall"><td><button class="button small" type="button" onclick="updateCategory(5)">Update</button>&nbsp;<button class="button small" type="button" onclick="deleteCategory(5)">Delete</button></td></tr><tr><td><input name="name" type="text" value="Monitors" /></td><div class="col-3 col-6-medium col-12-xsmall"><td><button class="button small" type="button" onclick="updateCategory(6)">Update</button>&nbsp;<button class="button small" type="button" onclick="deleteCategory(6)">Delete</button></td></tr>							</form>
						</tbody>
					</table>
				</div>
			</section>
			<!-- Create Category -->
			<section>
				<h2>Create Category</h2>
				<form id="createCategory" action="create_category.php" method="POST" onsubmit="return checkValues('createCategory')">
					<div class="row gtr-uniform gtr-50">
						<div class="col-4 col-12-xsmall"><input type="text" name="categoryName" id="categoryName" placeholder="Name" /></div>
						<div class="col-4 col-12-xsmall"><input type="submit" value="Create" class="primary" /></div>
					</div>
				</form>
			</section>
		</div>
		<!-- Footer -->
		<footer id="footer">
			<ul class="icons">
				<li><a href="#" class="icon brands alt fa-twitter"><span class="label">Twitter</span></a></li>
				<li><a href="#" class="icon brands alt fa-facebook-f"><span class="label">Facebook</span></a></li>
				<li><a href="#" class="icon brands alt fa-linkedin-in"><span class="label">LinkedIn</span></a></li>
				<li><a href="#" class="icon brands alt fa-instagram"><span class="label">Instagram</span></a></li>
				<li><a href="#" class="icon brands alt fa-github"><span class="label">GitHub</span></a></li>
				<li><a href="#" class="icon solid alt fa-envelope"><span class="label">Email</span></a></li>
			</ul>
			<ul class="copyright">
				<li>&copy; Fidelity. All rights reserved.</li>
			</ul>
		</footer>
	</div>
	<!-- Scripts -->
	<script src="assets/js/jquery.min.js"></script>
	<script src="assets/js/jquery.scrolly.min.js"></script>
	<script src="assets/js/jquery.dropotron.min.js"></script>
	<script src="assets/js/jquery.scrollex.min.js"></script>
	<script src="assets/js/browser.min.js"></script>
	<script src="assets/js/breakpoints.min.js"></script>
	<script src="assets/js/util.js"></script>
	<script src="assets/js/main.js"></script>
</body>

</html>


