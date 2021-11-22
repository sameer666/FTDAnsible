# launch container

docker run -it \
-v $(pwd):/root/ansible_collections/cisco/ftdansible/ \
python:3.6 bash

# run commands

pip install -r requirements.txt

cd /root/ansible_collections/cisco/ftdansible/

pip install -r requirements.txt

# this will pass with the correct inventory hosts file
ansible-playbook -i inventory/sample_hosts samples/ftd_configuration/download_upload.yml

# this will not pass with kickstart error
ansible-playbook -i inventory/sample_hosts samples/ftd_install/install_ftd_on_2110.yml


