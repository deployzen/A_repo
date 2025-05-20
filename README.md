===================== ssh keygen in server/master  ==========

generate ssh key copy the public key and paste in client authorized_keys 


======= install anisible package ============

      sudo apt install ansible 

====make directory========
	
      make directory -->>> create ansible related files 
      cd Demo
==== inventory.ini ===================

      nano inventory.ini  -- paste intentory.ini file
        
==== installa2.yml ======================[webservers]
          
         nano installa2.yml  -- past
         managed_node ansible_host=192.168.100.101 ansible_user=star           ======>>>> client ip and username 

===== /etc/default/locale ===============

         LANG="     .UTF-8"
         LC_ALL="      .UTF-8"

         sudo locale-gen en_In.UTF-8
         sudo update-locale
====== reboot =========================

         reboot

	
===== type thiscommand===========

     ansible-playbook -i inventory.ini installa2.yml
     ansible -m ping all


============ check in client   ==========


    sudo systemctl status apache2


