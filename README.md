# Splunk
My personal .bashrc settings for Splunk clustered environment

Usually the .bash files are located in each user's home directory - /home/user/.bashrc

You may need add this line to the .bash_profile file so it'll use the code in the .bashrc file:
Add: "source ~/.bashrc"

Just copy and paste the code from the bashrc.txt files to your user's .bashrc file. 

I personally customize specific .bashrc files depending on the Splunk server roles. 
So when you "sudo su - splunk", it'll contain and display specific aliases and welcome messages. 

You can modify all the Splunk's .bashrc file with Ansible. 
Just add all the appropriate hosts groups and names in your inventory file, example below. 
I added Ansible playbooks that I use in my current environment as an example in the master branch. 

# Example Ansible Inventory List
[all_splunk:children]

deployment_server
cluster_master
all_indexers
deployer
all_search_heads

[deployment_server]
deploymentserver.example.com

[cluster_master]
clustermaster.example.com

[all_indexers]
indexer[01:30].example.com

[deployer]
deployer.example.com

[all_search_heads]
searchhead[01:03].example.com


# References

Credit to Corey Schafer for teaching everyone how to customize their .bashrc file and teaching Linux stuff. 
https://www.youtube.com/user/schafer5/playlists


Check my "all_indexer_bashrc.yml" playbook that customize the .bashrc file for all indexers. 
Rinse and repeat for search head cluster members, heavy forwarders, and so on. 

I use this site for the Splunk server titles:
http://patorjk.com/software/taag/#p=display&c=echo&f=Slant&t=splunk%0A%0A

For color formatting ideas , I use this site:
https://misc.flogisoft.com/bash/tip_colors_and_formatting

For the little smiley faces in the terminal, I use this site:
https://textfac.es/
