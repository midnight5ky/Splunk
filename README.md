# Splunk
Personal bashrc settings for Splunk clustered environment

Usually the .bash files are located in each user's home directory - /home/user/.bashrc

You may need add this line to the .bash_profile file so it'll use the code in the .bashrc file:
Add: "source ~/.bashrc"

Just copy and paste the code from the bashrc.txt files to your user's .bashrc file. 

I personally customize specific .bashrc files depending on the Splunk server roles. 
So when you "sudo su - splunk", it'll contain and display specific aliases and welcome messages. 

You can modify all the Splunk's .bashrc file with Ansible. 
Just add all the appropriate hosts groups and names in your inventory file, example below. 
I added Ansible playbooks that I use in my current environment as an example in the master branch. 

[all_splunk:children]
cluster_master
all_indexers
deployer
all_search_heads

[cluster_master]
clustermaster.example.com

[all_indexers]
indexer[01:30].example.com

[deployer]
deployer.example.com

[all_search_heads]
searchhead[01:03].example.com
