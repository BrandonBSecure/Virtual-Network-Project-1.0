# Virtual-Network-Project-1.0
Virtual Network Diagram and Description.

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Network Diagram](https://user-images.githubusercontent.com/79088957/115844456-b03b4280-a3d4-11eb-84ed-55eb0579a77f.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YAML file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored the instance of DVWA(D*mn Vulnerable Web Application).

Load balancing ensures that the application will be highly reliable, in addition to restricting unwanted traffic to the network.

- Load Balancers protect the availability portion the CIA Triad by using redundancy to maintain access to the servers. What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system resources.

- Filebeat monitors log files or locations on your server.
- Metricbeat collects metrics from the system and services running on the system.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| TODO     |          |            |                  |
| TODO     |          |            |                  |
| TODO     |          |            |                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box-Provisioner machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 108.185.45.124 (My Personal Router/Machine)

Machines within the network can only be accessed by DVWA Docker Container.
 
Machines allowed to access my ELK server.
- Personal Machine 
108.185.45.124   
- Jummp-Box-Provioner 
52.191.131.161  

This was all made possible through Peering Connection Red-to- Elk and Elk-to-Red 

A summary of the access policies in place can be found in the table below.

| Name                 | Publicly Accessible | Allowed IP Addresses     |
|----------------------|---------------------|--------------------------|
| Jump-Box-Provisioner | Yes                 | 10.0.0.4  108.185.45.124 |
| WebVM1               | No                  | 10.0.0.4                 |
| WebVM2               | No                  | 10.0.0.4                 |
| WebVM3               | No                  | 10.0.0.4                 |
| ELK-Server           | No                  | 10.0.0.4  108.185.45.124 |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...


- Ansible allows quick and easy deployment without repetitious manual configuration. This minimizes if not completely eliminating human error.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- WebVM1 10.0.0.5
- WebVM2 10.0.0.6
- WebVM3 10.0.0.7

We have installed the following Beat on these machines:
- Filebeat

These Beats allow us to collect the following information from each machine:

- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
