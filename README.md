# CompareSatelliteRepos
A python script used to compare a list of repos from two Redhat Satellites a pull out the unique repositories

#This script was developed as a method of determining repos that are enabled on one Satellite but not another. 
#It was also developed as a method of ensuring an identitcal set of repos are enabled on each Satellite Server 
#so that ISS will work. 
#To make this script work save the output of the following command on two Satellite Servers
#
# hammer repository list --organization-id 1 --full-result true
#
# save the output of the above command for each Satellite into a file such as Satellite1.txt
#
# within your config set one of the files as Sat1 and the other as Sat2
#Sat1=Satellite1.txt
#Sat2=Satellite2.txt
#if everything is correct the script will give you a list of repos enabled ONLY on Sat1
#you can run this script backwards by switching the variables as shown below
#Sat1=Satellite2.txt
#Sat2=Satellite1.txt
#giving you a list of repos enabled only on Satellite 2
#
#
#Inter Satellite Synchronization will only work if you recieve no repos as output from this script
#while running it forwards and backwards 
#
