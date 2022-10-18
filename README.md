# ansible-project-automation
For this project,  the EC2 instance created for Jenkins project will be re-used.  First the server is renamed as Jenkins-Ansible.
Then a new github repository is created and nameds as **ansible-config-mgt**

Next is the installation of Ansible on the EC2 instance as follow:
```bash
sudo apt update
sudo apt install ansible
```
<img width="453" alt="ansible-install" src="https://user-images.githubusercontent.com/61512079/196516715-3291615c-6903-47b1-9cc1-382d43dad022.PNG">\

After the installation,  the ansible version is confirmed as follow:
<img width="684" alt="ansible version" src="https://user-images.githubusercontent.com/61512079/196517077-e85fa103-def0-4fcb-8010-80bb919a3392.PNG">

Next we opened the Jenkins instance from the web browser and configure a Freestyle project to save the repository content every time an update is done.

<img width="448" alt="webhook" src="https://user-images.githubusercontent.com/61512079/196519501-1b907e67-55c4-45f4-a197-d499003ce0e3.PNG">
<img width="474" alt="Git_trigger_test" src="https://user-images.githubusercontent.com/61512079/196519712-e4276884-0ac4-4ccc-8a33-8682da3d1254.PNG">

The next procedure is the preparation of the development environment on Visual Studio code IDE. The VSC is set up to connect to our github repository.
<img width="614" alt="Vscode_git_rep" src="https://user-images.githubusercontent.com/61512079/196520624-8fb369d3-d215-4f29-8d66-4c0f8edb4807.PNG">

After the github is set up on VSC,  we clone ansible-config-mgt repository on the jenkins EC2 instance
```bash
git clone https://github.com/digitalleks/ansible-configuration-management/
```
<img width="642" alt="git-clone-jenkins" src="https://user-images.githubusercontent.com/61512079/196526563-84053419-1bba-47c0-8276-bf355540aca8.PNG">

The next phase of the project is ansible configurations.  First we created a new branch labeled Feature, that will be used for development of a new feature.\
The newly created branch is then pulled by VS Code via git interface as shown below.  Other directory structure for the ansible projects were also created:\
<img width="274" alt="Ansible-feature-branch" src="https://user-images.githubusercontent.com/61512079/196531623-c5d332a0-af42-4143-a066-8bcdd1ce8f61.PNG">

<img width="236" alt="Ansible-directory1" src="https://user-images.githubusercontent.com/61512079/196531708-5bd030ab-a49c-4215-812f-6fee7a8f80cd.PNG">

THe third phase of the project is the inventory definition.  The snippet displayed below is saved in the dev.yml file created earlier:\
<img width="412" alt="dev-yml" src="https://user-images.githubusercontent.com/61512079/196550032-0a3cd3fd-05e6-49ba-aea1-06f9d09ea02d.PNG">

Next we install ssh agent on the local host using power shell and confirm the service is running.   The following snippets indicate the ssh-agent confirmation and connection to Jenkins server and the nginx load-balancer:\
<img width="611" alt="open-ssh-confirm" src="https://user-images.githubusercontent.com/61512079/196560031-9ed2f96c-86bc-4d6c-a72c-ae231e6ffe0e.PNG">

<img width="937" alt="sshd service" src="https://user-images.githubusercontent.com/61512079/196560063-d3ce4c92-3604-45e4-99a9-ca1c0ca64c45.PNG">

<img width="577" alt="ssh-agent-key-add" src="https://user-images.githubusercontent.com/61512079/196560096-4c86e134-7cf8-4d18-aa74-df43d8ae810a.PNG">

<img width="664" alt="ssh-add confirm" src="https://user-images.githubusercontent.com/61512079/196560128-3ccd8855-1ff5-49ea-a4a3-b30ad0c1ed99.PNG">

<img width="379" alt="jenkins-key-added" src="https://user-images.githubusercontent.com/61512079/196560159-6e16a47a-eb70-4aa1-9ce8-95334094712c.PNG">

<img width="503" alt="jenkins-connect-ssh-agent" src="https://user-images.githubusercontent.com/61512079/196560185-49abe155-1759-4fae-ac1a-6617be794683.PNG">

<img width="541" alt="lb-connect-ssh-agent" src="https://user-images.githubusercontent.com/61512079/196560210-3811db56-d5e4-4dbe-b93b-ffc36735ba66.PNG">







