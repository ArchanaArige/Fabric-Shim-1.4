Instructions:

1. Log into the VM
2. mkdir temp
3. cd temp
4. Pull the needed file by replacing the name with appropriate file name


wget https://raw.githubusercontent.com/acloudfan/Fabric-Shim-1.4/master/bins/FILE-NAME

E.g., to download the fabric-ca-server execute the following

wget https://raw.githubusercontent.com/acloudfan/Fabric-Shim-1.4/master/bins/fabric-ca-server


5. Copy the file

sudo  cp * /usr/local/bin

6. Change the mod of the file - replace the FILE-NAME with the file you downloaded

chmod 755 /usr/local/bin/FILE-NAME

E.g., to change the mod for fabric-ca-server

chmod 755 /usr/local/bin/fabric-ca-server

8. Verify by executing

fabric-ca-server     version
