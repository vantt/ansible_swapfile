How to install
--------------

    ansible-galaxy install -r requirements.yml

with the content of requirements.yml
    
    
    # requirements.yml
    
    - src: https://github.com/vantt/ansible_swapfile.git
      version: master
      name: swapfile

How to use
----------

    # playbook.yml
    
    - hosts:  all 
      sudo: yes
      gather_facts: true
      roles:
        - { role: swapfile, swap_filepath: "/swapfile", swap_size:4096 }
