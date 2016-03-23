An Ansible role for installing Kibana on Ubuntu 15.10, including Elasticsearch and Oracle JDK.

### Default versions

Ubuntu 15.10
Kibana 4.4.2
Logstash 2.2.2
Java JDK 8u73

### Testing

A Vagrant/VirtualBox environment is provided in the /examples directory.  To get started:

1. Install Vagrant, Virtualbox, and Ansible
1. Change your directory into 'examples'
1. Run the 'install_role_requirements.sh' script.  This adds an Ansible role for installing prerequisite software.  Kibana requires both Elasticsearch and Java.
1. Run 'vagrant up' to bring up the VM.

### Additional notes

- For Vagrant installs, the install packages are downloaded once and cached locally.
- Each role in this Ansible playbook will check the version of each application before installing, and will not re-install if the installed version is the desired version.  This speeds up reprovisioning.
- To reprovision, use the 'vagrant provision' command.
