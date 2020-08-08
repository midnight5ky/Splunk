# Splunk
My personal .bashrc settings for Splunk clustered environment

Usually the .bash files are located in each user's home directory - /home/user/.bashrc

Depending on how you installed Splunk or created a Splunk user, the .bashrc file is usually in /opt/splunk/ or /home/splunk/

You may need add this line to the .bash_profile file so it'll use the code in the .bashrc file:
Add: "source ~/.bashrc"

Just copy and paste the code from the .bashrc files to your user's .bashrc file. 

I personally customize specific .bashrc files depending on the Splunk server roles. 
So when you "sudo su - splunk", it'll contain and display specific aliases and welcome messages. 

You can modify all the Splunk's .bashrc file with Ansible. 
Just add all the appropriate hosts groups and names in your inventory file, check my "example_inventory_file". 
I added Ansible playbooks that I use in my current environment as an example in the master branch. 

Check my "all_indexer_bashrc.yml" playbook that customizes the .bashrc file for all indexers. 
Rinse and repeat for search head cluster members, heavy forwarders, and so on. 

# References

Credit to Corey Schafer for teaching everyone how to customize their .bashrc file and teaching Linux stuff. 
https://www.youtube.com/user/schafer5/playlists



I use this site for the Splunk server titles:
http://patorjk.com/software/taag/#p=display&c=echo&f=Slant&t=splunk%0A%0A

For color formatting ideas , I use this site:
https://misc.flogisoft.com/bash/tip_colors_and_formatting

For the little smiley faces in the terminal, I use this site:
https://textfac.es/
