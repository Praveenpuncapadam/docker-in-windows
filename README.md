# How to run docker on windiws without Docker Desktop.
In corperate environments, Devops engineers and developers often face challenges to test and deploy the docker in thier local development environment. To avoid this we normally realy on the Docker desktop. Docker Desktop required paid subscription for corperate use, which can be a concern for companies who looking minimize the costs.

To address this issue, an alternative approce is to leverage Windows Subsystem for Linux (WSL). By using WSL, Developers can setup and run Docker in linux environment directly on their wines mechine without the need for Docker Desktop. Tis solution not only eliminates the license cost but also provide a lightweight and efficient way to manage docker builds in the development environent.
## Install WSL:
Open powershell as an administrator and run teh following command
```
wsl --install
```
Note: You may need to restart your system for the changes to take effect.

## Setup Docker in WSL
- Open WSL (example Ubuntu) and run the following command:
  ```
  sudo apt update
  sudo apt-get install docker*
  ```
## Run a Web Application (eg. apache server) as a container in WSL:
- Start the application container in WSL.
- To access the application from your brower, tetrive the WSL IP address by running the following coammand in Windows PowerShell.
```
wsl -d ubuntu hostname -I
```
- Use  the retrived Ip address in your browser along with the application's port, for example :
```
http://172.20.131.172:8080
```
## Conclusion
Using WSL as an alternative to Docekr Desktop provides a cost-effective and efficient solution for managing in corperate environment and personal use. Developers can streamline their workflow and focus on building and deploying application without additional overhead.

If you find any issue on this or need to refer more then please refer below link.
- *Ref*: https://learn.microsoft.com/en-us/windows/wsl/setup/environment


