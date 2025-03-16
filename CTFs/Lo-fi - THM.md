
####Nmap scan

nmap -sC -sV -p- -T4 -Pn 10.10.15.133 -vv
Starting Nmap 7.95 ( https://nmap.org ) at 2025-03-16 12:56 EDT
NSE: Loaded 157 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 12:56
Completed NSE at 12:56, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 12:56
Completed NSE at 12:56, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 12:56
Completed NSE at 12:56, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 12:56
Completed Parallel DNS resolution of 1 host. at 12:56, 0.00s elapsed
Initiating SYN Stealth Scan at 12:56
Scanning 10.10.15.133 [65535 ports]
Discovered open port 80/tcp on 10.10.15.133
Discovered open port 22/tcp on 10.10.15.133
SYN Stealth Scan Timing: About 7.44% done; ETC: 13:03 (0:06:26 remaining)
SYN Stealth Scan Timing: About 11.89% done; ETC: 13:04 (0:07:32 remaining)
SYN Stealth Scan Timing: About 18.48% done; ETC: 13:04 (0:06:41 remaining)
SYN Stealth Scan Timing: About 27.42% done; ETC: 13:03 (0:05:20 remaining)
SYN Stealth Scan Timing: About 35.41% done; ETC: 13:03 (0:04:35 remaining)
SYN Stealth Scan Timing: About 45.23% done; ETC: 13:02 (0:03:39 remaining)
SYN Stealth Scan Timing: About 52.07% done; ETC: 13:02 (0:03:14 remaining)
SYN Stealth Scan Timing: About 59.43% done; ETC: 13:02 (0:02:45 remaining)
SYN Stealth Scan Timing: About 69.90% done; ETC: 13:02 (0:01:57 remaining)
SYN Stealth Scan Timing: About 77.59% done; ETC: 13:02 (0:01:27 remaining)
SYN Stealth Scan Timing: About 85.76% done; ETC: 13:02 (0:00:55 remaining)
Completed SYN Stealth Scan at 13:02, 375.38s elapsed (65535 total ports)
Initiating Service scan at 13:02
Scanning 2 services on 10.10.15.133
Completed Service scan at 13:02, 6.45s elapsed (2 services on 1 host)
NSE: Script scanning 10.10.15.133.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 5.75s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 0.83s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 0.01s elapsed
Nmap scan report for 10.10.15.133
Host is up, received user-set (0.20s latency).
Scanned at 2025-03-16 12:56:04 EDT for 389s
Not shown: 65533 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 61 OpenSSH 8.2p1 Ubuntu 4ubuntu0.4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 59:cd:6c:05:0c:2d:c0:8f:17:a1:0d:62:25:d5:79:fe (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCmJ+YKkgTr9ASPx+hWd6rTZ+9dJRKpg7jXrAfpqYvnZwXw1mXUfmtLv2Jk6Pdzc6uCGuK8lPEoOH58Trm1lAlNmlIIp7OLb4xzYn/16FwtF5NhWWWgECDoFOhS/rT2jzXQZ2wa7GecUCGN7NlUjFLZTMOXmFqZLvl3ePFYfITeCOil1ofoVNjDmsBeAAOZZGHZdteGZ6jJGlTCGn3O8Wa3Kvji/+jAjM3t1OunjKRttTIYSQbF80WfeAjLzL7DJGj7U+0y53OI10wkUVcXUbtGd45u4xaALn/JO3w5LUSa0JDgQVbAtyCHvD/4XrDr9mA4jwWbmN3J5JnomB814qdP2ljG3bZSdr2zLKF+eOKxrW74mQqS5AW4MVh5MMAlVsKGt5Lee23g3x1gUKSCbDOpEvxFgHGU25p4rH83zsOq9mspn+oQ2aoshzuIykgcYbM1mWQmFwRlm4He4YszGoS7F56yg2qdzAYFKCBI2yk4Ves40DRMSNmUu8pzx75U9ZU=
|   256 bf:7c:8c:a2:41:4b:83:ca:60:7b:b0:d3:02:eb:0f:af (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBNHrqjLCg43hhAMK5WkqLHU7K09TM/pJe4IXjJ6aRyAWCh3ezrELqBDy7MzlpqDkc3LbCq+srPvJ8vJKOQkhJqw=
|   256 30:f7:3d:31:87:9c:20:06:55:c1:90:d6:81:e1:c1:b6 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAII4L4ELhB6A72+Mqsi3SVWmGo3ArjTvi+fACKlE0McXP
80/tcp open  http    syn-ack ttl 60 Apache httpd 2.2.22 ((Ubuntu))
|_http-server-header: Apache/2.2.22 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: Lo-Fi Music
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 13:02
Completed NSE at 13:02, 0.00s elapsed
Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 388.99 seconds
           Raw packets sent: 69820 (3.072MB) | Rcvd: 68243 (2.734MB)






####web collecttion

<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <link rel="stylesheet" href="[https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css](view-source:https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css)"
        integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">

    <style>
        body {
            padding-top: 56px;
            padding-bottom: 56px;
            min-height: 100vh;
            position: relative;
        }
        .footer {
            bottom: 0;
            width: 100%;
            position: absolute;
            height: 56px;
        }
    </style>

    <title>Lo-Fi Music</title>
</head>

<body>

    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="[/](view-source:http://10.10.15.133/)">Lo-Fi Music</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive"
                aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarResponsive">
            </div>
        </div>
    </nav>

    

        <!-- Page Content -->
    <div class="container">

        <div class="row">

            <!-- Blog Entries Column -->
            <div class="col-md-8">

                <h1 class="my-4">Cool beats to listen to</i></h1>

                <!-- Blog Post -->
                <div class="card mb-4">
					<div class="card-body">

						<h2 class="card-title">Relax</h2>

<p class="card-text">
    <iframe width="680" height="360" src="[https://www.youtube.com/embed/5qap5aO4i9A](view-source:https://www.youtube.com/embed/5qap5aO4i9A)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>                	</div>
                </div>

            
            </div>

            <!-- Sidebar Widgets Column -->
            <div class="col-md-4">

                <!-- Search Widget -->
                <div class="card my-4">
                    <h5 class="card-header">Search</h5>
                    <div class="card-body">
                        <form action="[/](view-source:http://10.10.15.133/)" method="get">
                            <div class="input-group">
                                <input type="text" class="form-control" name="search" placeholder="Search for...">
                                <span class="input-group-btn">
                                    <button class="btn btn-secondary" type="submit">Go!</button>
                                </span>
                            </div>
                        </form>
                    </div>
                </div>

                <!-- Categories Widget -->
                <div class="card my-4">
                    <h5 class="card-header">Discography</h5>
                    <div class="card-body">
                        <div class="row">
                            <div class="col-lg-6">
                                <ul class="list-unstyled mb-0">
                                    <li><a href="[/?page=relax.php](view-source:http://10.10.15.133/?page=relax.php)">Relax</a></li>
                                    <li><a href="[/?page=sleep.php](view-source:http://10.10.15.133/?page=sleep.php)">Sleep</a></li>
									<li><a href="[/?page=chill.php](view-source:http://10.10.15.133/?page=chill.php)">Chill</a></li>    
									<li><a href="[/?page=coffee.php](view-source:http://10.10.15.133/?page=coffee.php)">Coffee</a></li>
									<li><a href="[/?page=vibe.php](view-source:http://10.10.15.133/?page=vibe.php)">Vibe</a></li>
									<li><a href="[/?page=game.php](view-source:http://10.10.15.133/?page=game.php)">Game</a></li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
        <!-- /.row -->
    </div>
    <!-- /.container -->

    <!-- Footer -->
    <footer class="py-3 bg-dark footer">
        <div class="container">
                &nbsp;
        </div>
        <!-- /.container -->
    </footer>

</body>

</html>

