# PublicScripts
#### Prepare Ubuntu 18.04 Template
`# curl -sL https://github.com/gonhvvjvo/PublicScripts/raw/master/Files/prepare-ubuntu-18.04-template-latest.sh | sudo -E bash -`
#### Prepare Ubuntu 18.04 Template with Ansible config
1. Import ssh by CMD `ssh-copy-id username@s.e.r.v` on client
2. Run CMD script below  
`# curl -sL https://github.com/gonhvvjvo/PublicScripts/raw/master/Files/prepare-ubuntu-18.04-template-ansible.sh | sudo -E bash -`
#### CentOS 7 Script crontab yum update monthly
```
mkdir -p /opt/scripts/

cat <<EOF | sudo tee /opt/scripts/monthly-yum-update.sh
#!/bin/bash

########## Update all ##########
yum update -y && yum upgrade -y && reboot
EOF

chmod +x /opt/scripts/monthly-yum-update.sh
```

`0 1 17 * * sh /opt/scripts/monthly-yum-update.sh >/dev/null 2>&1`

#### CentOS 7 Script crontab update DirectAdmin weekly
```
cat <<EOF | sudo tee /opt/scripts/weekly-da-update.sh
#!/bin/bash

########## Update all ##########
#cd /usr/local/directadmin/custombuild
#./build update
#./build all d


########## Update only new version ##########
cd /usr/local/directadmin/custombuild
./build update_versions
EOF

chmod +x /opt/scripts/weekly-da-update.sh
```

`0 3 * * 0 sh /opt/scripts/weekly-da-update.sh >/dev/null 2>&1`