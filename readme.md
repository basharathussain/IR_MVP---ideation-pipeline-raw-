# IR Pipeline ref
.
Start a **Docker Desktop 
**
**Enable Features on Windows: ** 
- Virtualization
- HyperV
- Hypervisor Platform
- VM Platform

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Crawl4AI docker image: **unclecode/crawl4ai** >> Search in docker images and pull it.

Docker Desktop: Containers tab -> run the container

Cmd (run as admin): 
- List all images: docker images
- List all containers: docker ps -a
- Create the container **with port binding**: docker run -p 11235:11235 unclecode/crawl4ai:latest
- Ensure in container the inspect tab and portbindings section:
		"PortBindings": {
			"11235/tcp": [
				{
					"HostIp": "",
					"HostPort": "11235"
				}
			]
		},
- Read **containerid** and then execute command: docker exec -it [2f5]  /bin/sh
- $ You can use the command "ls" to list documents in the container.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

WSL installation:
-----------------
You can install Ubuntu cleanly from the Microsoft Store:
Open Microsoft Store
Search for “Ubuntu”
Choose your version (e.g., "Ubuntu 24.04.1 LTS")
Click Install
You can just launch it, and it should complete the setup.

C:\Windows\system32>wsl --list -v
  NAME              STATE           VERSION
* docker-desktop    Running         2
  Ubuntu            Running         2

in CHrome now: [access](http://localhost:11235/) should display default page 

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

ngrok installation:
-----------------
 
Sign up here and download ngrok
https://dashboard.ngrok.com/login 

Register authtoken command on ngrok.

command: ngrok http http://localhost:11235/



%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


(base) PS E:\_src_agenticai\IR-platform-2025\n8n-variables> docker compose up -d

time="2025-07-06T16:01:56+05:00" level=warning msg="E:\\_src_agenticai\\IR-platform-2025\\n8n-variables\\docker-compose.yml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion"
[+] Running 13/15
 - crawl4ai [⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿]   885MB / 887.5MB Pulling                                                           317.0s
   ✔ 2d429b9e73a6 Pull complete                                                                                   57.9s
   ✔ ff0106aa50b2 Pull complete                                                                                  207.4s
   - 16954479144d Downloading [==================================================>]    ...                       313.3s
   ✔ 4f4fb700ef54 Already exists                                                                                   0.1s
   ✔ d447e55d51db Pull complete                                                                                   58.2s
   ✔ 3f0c8630a336 Download complete                                                                               16.3s
   ✔ 0169a1f3a742 Download complete                                                                               36.8s
   ✔ f4652d21edd3 Download complete                                                                                7.7s
   ✔ 293d8aa268c0 Pull complete                                                                                  277.3s
   ✔ 22370d9525db Pull complete                                                                                   59.6s
   ✔ 08b960408463 Pull complete                                                                                  221.9s
   ✔ 1725cd9e6d04 Download complete                                                                              135.0s
   ✔ 5862c84e1a84 Pull complete                                                                                    2.2s
   ✔ fd2c9b930c68 Pull complete                                                                                  226.3s

Note: Run the Docker Composer when both docker desktop and ubuntu are running:

C:\Windows\system32>wsl --list -v

  NAME              STATE           VERSION
  
* docker-desktop    Running         2
  
  Ubuntu            Running         2

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Postgres 17

digitalocean cloud


  
