
step1:
git clone https://github.com/Slothiiii/multi-mn-script.git $$ cd multi-mn-script.git

step2:
chmod +x install.sh

step3:
./install.sh -p peps -n 6 -c 4 #(-n6 = ipv6 )
 
 ./install.sh -p peps -n 4 -c 4 #(-n 4 = ipv4
 
 step4:
 wait for done (30min) of the 4 nodes / 1 node par min.
 
 
 step5:
  /etc/masternodes
  and edit genkey ,rpuser,rpcpassword 

  step6:

/usr/local/bin/pepsd -daemon -pid=/var/lib/masternodes/peps1/peps.pid -conf=/etc/masternodes/peps_n1.conf -datadir=/var/lib/masternodes/peps1
...
...
...

ste7:
look at blocks

/usr/local/bin/peps-cli -conf=/etc/masternodes/peps_n1.conf getinfo

step8:
go into your wallet as soon as you have loaded all blocks in the VPS / and start the node in the wallet 
#status on VPS Succesfull
/usr/local/bin/peps-cli -conf=/etc/masternodes/peps_n1.conf masternode status
----------------------------------------------------------------------------------
#stop the node !
/usr/local/bin/peps-cli -conf=/etc/masternodes/peps_n1.conf stop
#start the node
/usr/local/bin/peps-cli -conf=/etc/masternodes/peps_n1.conf start
#start all nodes
/usr/local/bin/activate_masternodes_peps
#all kommands
Long Option    Short Option    Values    description
--project    -p    project, e.g. "abet"    shortname for the project
--net    -n    "4" / "6"    ip type for masternode. (ipv)6 is default
--release    -r    e.g. "tags/v3.4.0.0"    a specific git tag/branch, defaults to latest tested
--count    -c    number    amount of masternodes to be configured
--update    -u    --    update specified masternode daemon, combine with -p flag
--sentinel    -s    --    install and configure sentinel for node monitoring
--wipe    -w    --    uninstall & wipe all related master node data, combine with -p flag
--help    -h    --    print help info
--startnodes    -x    --    starts masternode(s) after installation