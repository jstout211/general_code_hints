# general_computing_reminders
Just a reminder for myself on how to do certain things

## Pytest
Printout all outputs (-s is important)
`pytest -s -k TestName`

## Vim Stuff
https://github.com/jstout211/vim_cmds

## Docker / Podman
https://github.com/jstout211/podman_commands  <br>
Docker w/ github actions: <br>
https://linuxhit.com/how-to-create-docker-images-with-github-actions/

## Datalad
https://github.com/jstout211/datalad_examples

## Used for nested looping and getting the x,y index in a matrix
np.unravel_index(tile_idxs, [row_num, col_num])

## Checking connectivity issues to a computer
ping IPADDRESS --- if this works and the below says filtered, then there is a network block
sudo nmap -p 22 -Pn --traceroute IPADDRESS

also nslookup is helpful to return the ip address of a named computer
On the local computer --- sudo ufw status -- this may show any local firewall filtering that is occuring

## RAID CLI
# Old Server
cd /opt/MegaRAID/storcli
sudo storcli show
sudo strocli /c#/eall/sall show 
# New Server
cd /opt/MegaRAID/perccli/
sudo ./perccli64 show

Additional info on Seagate drives in Dell server: https://toughtechsite.wordpress.com/2017/12/03/the-case-of-non-certified-physical-drives-causing-warnings-in-dell-openmanage-omsa/







