  
https://rafter.bi.vt.edu/usersvc/register  
https://rafter.bi.vt.edu/usersvc/  
https://rafter.bi.vt.edu/  
  
[Register an Application]
https://rafter.bi.vt.edu/usersvc/application 

Save application name  , suppose Application_ngs2_1.  

UUID : 4a21bea0-72fc-11e7-8613-717499928918  
Save uuid : 
https://rafter.bi.vt.edu/usersvc/application/4a21bea0-72fc-11e7-8613-717499928918  

Get New Token, using generate token button :  
TOKEN. Save it.
  
=====================  

## For ubuntu
sudo apt-get install npm  
sudo npm install -g  
sudo ln -s  /usr/bin/nodejs  /usr/local/bin/node  

Should not throw an error  
which rafter  
which node  
which nodejs  

Download rafter-cli.tar
Untar [ tat -xf rafter-cli.tar]  
./bin/rafter init <uuid> <token>
./bin/rafter volume init
./bin/rafter volume ls /home/ddatta

=====================

There is a sample data file.Extract it.  
./bin/rafter volume create -n <target file path/name>  -f < local file path/name>   /home/ddatta  
For eaxample :  
./bin/rafter volume create -n n.1000.k.10.v.01.int.node.traits  -f nim.11.1.data/n.1000.k.10.v.01.int.node.traits  /home/ddatta

Use the job config json file : 
./bin/rafter job submit -d intersim-im-11-1 -o /home/ddatta -n nim.output.1 -o @/absolute/path/to/input/params.json

For Example: 
./bin/rafter job submit -d intersim-im-11-1 -o /home/ddatta -n nim.output.1 -o @/home/debanjan/params_for_job.json

See this file:
$ cat ./rafter/config.json
