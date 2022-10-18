# ansible-project-automation
For this project,  the EC2 instance created for Jenkins project will be re-used.  First the server is renamed as Jenkins-Ansible.
Then a new github repository is created and nameds as **ansible-config-mgt**

Next is the installation of Ansible on the EC2 instance as follow:
```bash
sudo apt update
sudo apt install ansible
```
<img width="453" alt="ansible-install" src="https://user-images.githubusercontent.com/61512079/196516715-3291615c-6903-47b1-9cc1-382d43dad022.PNG">\

After the installation,  the ansible version is confirmed as follow:\
<img width="684" alt="ansible version" src="https://user-images.githubusercontent.com/61512079/196517077-e85fa103-def0-4fcb-8010-80bb919a3392.PNG">\

Next we opened the Jenkins instance from the web browser and configure a Freestyle project to save the repository content every time an update is done.\

<img width="448" alt="webhook" src="https://user-images.githubusercontent.com/61512079/196519501-1b907e67-55c4-45f4-a197-d499003ce0e3.PNG">\
<img width="474" alt="Git_trigger_test" src="https://user-images.githubusercontent.com/61512079/196519712-e4276884-0ac4-4ccc-8a33-8682da3d1254.PNG">

The next procedure is the preparation of the development environment on Visual Studio cosde IDE. The VSC is set up to connect to our github repository.\
<img width="614" alt="Vscode_git_rep" src="https://user-images.githubusercontent.com/61512079/196520624-8fb369d3-d215-4f29-8d66-4c0f8edb4807.PNG">





