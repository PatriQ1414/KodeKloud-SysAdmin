## NFS Troubleshooting
### The Nautilus production support team was trying to fix issues with their storage server. The storage server has a shared directory /webdata, which is mounted on all app servers at location /var/www/html so that whatever data they store on storage server under /webdata can be shared among all app servers. Somehow NFS server is broken and having some issues. Identify the root cause of the issue and fix it to make sure sharing works fine among all app servers and storage server.

#### ssh into NFS server using appropriate credentials
ssh user@ststor01

#### Runing the following commnads to check status, enable, and start NFS Service
sudo systemctl status nfs-server
sudo systemctl enable nfs-server
sudo systemctl start nfs-server

#### Confirm status Active(running)
sudo systemctl status nfs-server

#### Edit /etc/exports
sudo vi /etc/exports

#### Delete entry and insert the following
/webapps 172.16.238.10(rw,sync,no_root_squash) 
/webapps 172.16.238.11(rw,sync,no_root_squash)
/webapps 172.16.238.12(rw,sync,no_root_squash)

#### Make export available for mount
sudo exportfs

#### ssh into all servers listed in /etc/exports, run the following command in each
sudo mount <nfs server name>:/shared_folder /mount/location/on/server/

#### To confirm , run
  mount
  
  df -h
