# README #
# xtream-ui-install

This is an installation mirror for xtream ui software.

### How do I install? ###

update your ubuntu first, then install panel  

- sudo su
- apt-get upgrade
- apt-get update
- apt install net-tools
- cd /usr/src
- nano /etc/apt/sources.list (nota: anadir esta linea : deb http://mirrors.us.kernel.org/ubuntu/ xenial main 
- sudo apt-get update
- sudo apt-get install libpng12-0
- sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get install libxslt1-dev libcurl3 libgeoip-dev python -y;
- wget https://raw.githubusercontent.com/PlusmasTV/XtreamUI-Ubuntu18.04-V22-CK7/main/install.py; 
- sudo python install.py  

  
If you want to install main server with admin panel, choose MAIN.  
If you want to install load balance on additional servers, add a server to panel in manage servers page, then run script and proceed with LB option.  
If you want to update admin panel, select UPDATE, then paste download link of release_xyz.zip file.  

### tutorials are here; ###

[Xtream-UI Tutorials](https://www.youtube.com/playlist?list=PLJB51brdC_w7dTDxi1MPqiuk3JH5U2ekn "Xtream-UI Tutorials")


### Files Hashes ###
* main_xtreamcodes_reborn.tar
* sha1: "532B63EA0FEA4E6433FC47C3B8E65D8A90D5A4E9"

* sub_xtreamcodes_reborn.tar
* sha1: "5F8A7643A9E7692108E8B40D0297A7A5E4423870"

* release_22f.zip
* sha-1: "95471A7EFEB49D7A1F52BAB683EA2BF849F79983"

### note,
i forked this install.py is from https://xtream-ui.com/install/install.py  
you can compare my install.py with original one.

### note2,
edit pytools/balancer.py to use "auto lb installer" from this mirror. auto lb installer added to panel with update    
`sed -i 's|"https://xtream-ui.com/install/balancer.py"|"https://github.com/xtream-ui-org/xtream-ui-install/raw/master/balancer.py"|g' /home/xtreamcodes/iptv_xtream_codes/pytools/balancer.py`  

### note3,  
developer made update releases open to public after r22c release, you can download them from https://xtream-ui.com.  
i added an "UPDATE" part to install.py, it will ask link of update zip file.
