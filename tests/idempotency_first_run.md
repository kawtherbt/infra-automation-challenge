
PLAY [all] *********************************************************************

TASK [Gathering Facts] *********************************************************
ok: [myserver]

TASK [Update apt cache] ********************************************************
ok: [myserver]

TASK [server_setup : Ensure sudo group exists] *********************************
ok: [myserver]

TASK [server_setup : Ensure docker group exists] *******************************
ok: [myserver]

TASK [server_setup : Create dedicated user with home] **************************
ok: [myserver]

TASK [server_setup : Ensure .ssh directory exists] *****************************
ok: [myserver]

TASK [server_setup : Add public key for user] **********************************
ok: [myserver]

TASK [server_setup : Ensure backup of sshd_config exists] **********************
ok: [myserver]

TASK [server_setup : Backup original sshd_config] ******************************
skipping: [myserver]

TASK [server_setup : Deploy hardened sshd_config (template)] *******************
ok: [myserver]

TASK [server_setup : Install apt dependencies for Docker] **********************
ok: [myserver]

TASK [server_setup : Add Docker GPG key] ***************************************
ok: [myserver]

TASK [server_setup : Add Docker apt repository] ********************************
ok: [myserver]

TASK [server_setup : Install docker packages] **********************************
ok: [myserver]

TASK [server_setup : Ensure docker service is running] *************************
ok: [myserver]

TASK [server_setup : Ensure bootstrap user is in docker group] *****************
ok: [myserver]

TASK [server_setup : Deploy docker daemon.json (log opts)] *********************
ok: [myserver]

TASK [server_setup : Install fail2ban] *****************************************
ok: [myserver]

TASK [server_setup : Deploy basic fail2ban ssh jail] ***************************
ok: [myserver]

TASK [server_setup : Ensure fail2ban running] **********************************
ok: [myserver]

TASK [server_setup : Pull app image] *******************************************
ok: [myserver]

TASK [server_setup : Run app container] ****************************************
ok: [myserver]

PLAY RECAP *********************************************************************
myserver                   : ok=21   changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0   

