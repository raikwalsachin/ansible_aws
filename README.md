Hi Dynamic inventory ansible configuration for AWS cloud   
# ansible dynamic inventory setup    
After installation of ansible     
Step1: ansible-galaxy collection install amazon.aws    
Step2: cat aws_ec2.(yaml|yml) name should be strictly same aws_ec2    
Step3: make changes to ansible.cfg file at /etc/ansible/ansible.cfg    
        >> In [inventory] block add a line     
        >> enable_plugins = aws_ec2       
Step4: Give a AWS role to the localhost instance so that you dont have to store access keys in a file.     
Step5: ansible-inventory -i "location of aws_ec2.yaml" --list      
Step6: ansible all --list-hosts     
