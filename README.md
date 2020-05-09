## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _____, in addition to restricting _____ to the network.
- _Load balacers protect the machines from traffic: What aspect of security do load balancers protect? What is the advantage of a jump box?_Jumpbox manages machines in seperate security zones and control means of access between them

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _execute complex searches____.
- _Filebeat is built to collect data about specific files on remote machines: What does Filebeat watch for?_
- _Metricbeat collects machine metrics, such as uptime: What does Metricbeat record?_

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name      | Function | IP Address | Operating System |
|---------- |----------|------------|------------------|
| Jump Box  | Gateway  | 10.0.0.1   | Linux            |
| DVWA      | Testing  | 10.0.0.5   | Linux            |
| Elk-Server| Searches | 10.0.0.11  | Linux            |
| TODO      |          |            |                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _Jump Box: Which machine did you allow to access your ELK VM? What was its IP address?40.117.58.151_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _Ansible is Agentlees, you don't need to install any other software or firewall ports on the system you want to automate. ayaou also don't have to set up a seperate management structure: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- 
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
-: Specify which Beats you successfully installed_
I successfully Installed filebeat

These Beats allow us to collect the following information from each machine:
- _: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._
Filebeat collects log events and forward them to Elasticsearch or Logstash for indexing. Metricbeat collects and ships metrics to the output that you specify, such as Elasticsearch or Logstash. E.g. 'Audibeat' collects and centralize audit events from the Linux Audit Framework.
### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?
_  You update the host file and ansible configuration file. To specify which machine to install the ELK server on, you nano in to host file update the specific IP address and, For Filebeat, ssh in to your jumpbox, start your specific
   container, cd etc/ansible, ls and list of files will displayed. Then you can select and nano to install filebeat.  
- _Which URL do you navigate to in order to check that the ELK server is running? http://ELK server IP address(5601)

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

