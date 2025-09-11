# general_computing_reminders
Just a reminder for myself on how to do certain things

## Pytest
Printout all outputs (-s is important)
`pytest -s -k TestName`

## Vim Stuff
https://github.com/jstout211/vim_cmds

## TMUX hints:
https://gist.github.com/michaellihs/b6d46fa460fa5e429ea7ee5ff8794b96

## Docker / Podman
https://github.com/jstout211/podman_commands  <br>
Docker w/ github actions: <br>
https://linuxhit.com/how-to-create-docker-images-with-github-actions/

## Datalad
https://github.com/jstout211/datalad_examples

## Used for nested looping and getting the x,y index in a matrix
np.unravel_index(tile_idxs, [row_num, col_num])

## find all files and replace a specific word (deprecated function) with an alternative.  Use git clean / checkout / restore to fix if erroneous changes happen
```
find /MYGITPROJECT/ -type f | xargs sed -i 's/word1/word2/g'
```


## Checking connectivity issues to a computer
```
ping IPADDRESS --- if this works and the below says filtered, then there is a network block
sudo nmap -p 22 -Pn --traceroute IPADDRESS
```
also nslookup is helpful to return the ip address of a named computer <br>
On the local computer --- sudo ufw status -- this may show any local firewall filtering that is occuring <br>

## Twine upload to pypi
To fix the following issue with setuputils uploade, download twine to 6.0.1 (from 6.1.0): https://stackoverflow.com/questions/79408101/what-is-the-correct-way-of-specifying-the-license-in-pyproject-toml-file-for-a-n


### Sphinx setup (still learning this)
`pip install sphinx` <br>
`pip install sphinxcontrib-napoleon` <br>
```
mkdir docs
cd docs
sphinx-quickstart
```

Add the following to the conf.py file :
```
import os, sys
sys.path.insert(0, os.path.abspath('..'))

extensions = ["sphinx.ext.todo", "sphinx.ext.viewcode", "sphinx.ext.autodoc", "sphinx.ext.napoleon"]  
```

Run 
```
cd ..
sphinx-apidoc -o docs .
sphinx-build -b html ./ ./html
``` 

## RAID Config Help
```
sudo smartcl -a /dev/sd#
openSeaChest_*      #This is the seagate utility that can be installed through apt
```
### Old Server
```
  cd /opt/MegaRAID/storcli
  sudo storcli show
  sudo strocli /c#/eall/sall show
```
### New Server
```
cd /opt/MegaRAID/perccli/
sudo ./perccli64 show
```

Additional info on Seagate drives in Dell server: https://toughtechsite.wordpress.com/2017/12/03/the-case-of-non-certified-physical-drives-causing-warnings-in-dell-openmanage-omsa/ <br>
PWDIS  fix: https://forums.servethehome.com/index.php?threads/powering-sas-drives.42019/ <br>
Kapton Insulating Tape: https://www.mcmaster.com/products/polyimide-tape/masking-tape-for-electronics-8/?s=polyimide-tape <br>








