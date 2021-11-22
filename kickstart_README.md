# launch container

docker run -it \
-v $(pwd):/root/ansible_collections/cisco/ftdansible/ \
python:3.6 bash

# run commands

pip install -r requirements.txt

cd /root/ansible_collections/cisco/ftdansible/

pip install -r requirements.txt

ansible-playbook -i inventory/sample_hosts samples/ftd_install/install_ftd_on_2110.yml

ansible-playbook -i inventory/sample_hosts samples/ftd_configuration/download_upload.yml

