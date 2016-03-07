Installfest2016 (http://installfest.cz/if16/uvod) ansible playbooks and roles
=============================================================================

Local configuration
-------------------

If you want to run it, you must have ansible (really!) and boto library installed (python-boto package). Then, you must set env variables #export AWS_ACCESS_KEY_ID and  AWS_SECRET_ACCESS_KEY. You will obtain keys in step below.

Amazon configuration
--------------------

Sign up into your Amazon console and create an Ansible user, that will have privileges to create ec2 and rds instances. Create an keypair for the user and set env for your local computer. If you want to be extra safe (recommended) create an server trhu Amazon console and instal land configure ansible there.

Deployment
----------

First run create_app_server_ami.yml, that will create an deployable AMI image, than add it`s id to site.yml and it will create full app stack (ELB, RDS, EC2, autoscaling, cloudformation). It will create several machines (it WILL cost you money!), create load balancer, setup RDS Mysql instance, setup networking and security zones.

I`m open to pull requests, or bug reports if you get stuck somwhere, thanks!

David Karban

