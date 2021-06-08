#ssh into server using appropriate credentials
ssh user@servername
#input password when asked
#run following command to create user
sudo useradd <new_user> -s /sbin/nologin
#Run the following command to confrm
cat /etc/passwd
#Confirm user created
