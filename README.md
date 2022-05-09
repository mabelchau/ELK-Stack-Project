# ELK-Stack-Project
## Automated ELK Stack Deployment
This project monitors a website on the Microsoft Azure Cloud Environment using the ELK Stack.

![Network Diagram](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/Diagrams_and_Images/ELK_Stack_Project_Network_Diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the **_yml_** and **_config_** files may be used to install only certain pieces, such as Filebeat.

* [My First Playbook](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/Docker/pentest.yml "My First Playbook")
* [Hosts](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/ansible-hosts/hosts "Hosts File")
* [Ansible Configuration](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/ansible-hosts/ansible.cfg "Ansible Configuration File")
* [Ansible ELK Installation and VM Configuration](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/ELK/elk-playbook.yml "ELK Installation and VM Configuration file")
* [Filebeat Config](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/Filebeat/filebeat-config.yml "Filebeat Configuration File")
* [Filebeat Playbook](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/Filebeat/filebeat-playbook.yml "Filebeat Playbook")
* [Metricbeat Config](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/Metricbeat/metricbeat-config.yml "Metricbeat Configuration File")
* [Metricbeat Playbook](https://github.com/mabelchau/ELK-Stack-Project/blob/Main/ansible/Metricbeat/metricbeat-playbook.yml "Metricbeat Playbook")

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.
What aspect of security do load balancers protect? 
  -  **Load balancers protect the servers from becoming overloaded with traffic. They reroute live traffic from one server to another. This is useful in case a server becomes victim to a DDoS attack or otherwise becomes unavailable.**

What is the advantage of a jump box?
 -  **The jump box prevents VMs from being exposed via a public IP Address. This allows us to monitor and log on using a single box. Also it restricts the IP addresses which are able to communicate with the Jump Box.**

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the **_network_** and **_system logs_** .
What does Filebeat watch for?
  -  **Filebeat watches for log files and collects events. It forwards them either to Elasticsearch or Logstash for indexing**  

What does Metricbeat record?
  -  **Metricbeat records statistical data from the OS and services running on the servers. It collects and ships them to the output that you specify, such as Elasticsearch or Logstash.**
