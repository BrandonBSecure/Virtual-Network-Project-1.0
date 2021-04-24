# Virtual-Network-Project-1.0
Virtual Network Diagram and Description.

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Network Diagram](https://github.com/BrandonBSecure/Virtual-Network-Project-1.0/blob/main/Virtual%20Network%20Diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YAML file may be used to install only certain pieces of it, such as Filebeat.

  [Filebeat Playbook](https://github.com/BrandonBSecure/Virtual-Network-Project-1.0/blob/main/Filebeat-Playbook.YAML)

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

| Name      | Function | IP Address | Operating System |
|-----------|----------|------------|------------------|
| Jump Box  | Gateway  | 10.0.0.4   | Linux            |
| WebVM1    | Webserver| 10.0.0.5   | Linux            |
| WebVM2    | Webserver| 10.0.0.6   | Linux            |
| WebVM3    | Webserver| 10.0.0.7   | Linux            |               
| ELK-Server| Webserver| 10.1.0.4   | Linux            |


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
| Jump-Box-Provisioner | No                  | 108.185.45.124           |
| WebVM1               | yes                 | Any                      |
| WebVM2               | yes                 | Any                      |
| WebVM3               | yes                 | Any                      |
| ELK-Server           | No                  | 108.185.45.124           |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...


- Ansible allows quick and easy deployment without repetitious manual configuration. This minimizes if not completely eliminates human error.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![ELK "docker ps" Screenshot](https://github.com/BrandonBSecure/Virtual-Network-Project-1.0/blob/main/ELK%20%22docker%20ps%22.png)

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
- Copy the filebeat-playbook.yamlfile to /etc/ansible/????.
- Update the filebeat-config.yaml file to include ELK-Server private IP on lines 1106 and 1806.
- Run the playbook, navigate to Kibana GUI by entering the ELK-Server Public IP into web browser to verify the installation executed as expected.
