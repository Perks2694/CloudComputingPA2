# CloudComputingPA2

In Order to run the program you simply Vagrant Up --provision.

The Vagrant script will build the local machine first and install the everything needed including moving files from the host machine to the local vm.
Ansible will then create the 2 cloud VMS and configure them with the SSH key.
VM2 is configured to run zookeeper and Kafka. VM3 has Kafka and COuchDB and runs the consumer python script
The Consumer on VM3 runs asynchronously while the ansible script continues to run the Producer.

Effort Expended - 

The creating of the Ansible and Vagrant files was not particularly challenging in this assignment, however finding the correct commands and ansible packages to use to get the correct results was a bit of a challenge.

I had issues getting the CouchDB to operate correctly using Ansible. After installing Couchdb with Ansible it never had permissions to connect, I tried to change its permissions and run it as different users. None of these worked. I also had issues just installing couchDB using ansible. I managed to do it after many different trial and errors, I had to remake the VMS a few times due to issues with getting CouchDB installed. In the end I could not get it to work with COuchdb.

