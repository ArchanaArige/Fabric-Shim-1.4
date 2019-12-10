# http://bcmentors.com
# Part of the Hyperledger Fabric courses by Rajeev Sakhuja


# Issue:
Some students have informed that they are unable to pull the Fabric shim. My investigation has revealed that Fabric developers has updated the repo. Not sure if it was by mistake or if its a new structure. I am still trying to find the permanent solution *BUT* in the meantime here is the get around that will get you going.

Follow the steps in the setup lecture & if you get the below error then follow the steps below:

* package github.com/hyperledger/fabric/core/chaincode/shim: cannot find package "github.com/hyperledger/fabric/core/chaincode/shim" in any of:

/usr/local/go/src/github.com/hyperledger/fabric/core/chaincode/shim (from $GOROOT) *

Steps:
======
1. Log into the VM
2. Create a temp folder .    mkdir temp
3. Change to the temp folder .   cd temp
4. Check the GOPATH. If it is NOT set then you MUST execute the prior steps for setting the GoLang/GOPATH

echo $GOPATH

5. Clone this repository. 
git clone https://github.com/acloudfan/Fabric-Shim-1.4.git

6. Un tar the file using the command below
tar xvf fabric-shim-1.4.tar -C $GOPATH

If there is no error then you are good to go

Happy Learining !!!!


