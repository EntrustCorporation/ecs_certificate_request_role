galaxy-edc-roles
=====================

Additional references
---------------------
- Leveraging Deployment Automation Ansible Role to Set Up and Refresh Your Web Infrastructure (article)
https://www.entrustdatacard.com/blog/2019/august/leveraging-deployment-automation-tools 
- Entrust Datacard SSL certificates information/purchase pages
https://www.entrustdatacard.com/products/categories/ssl-certificates

Purpose of role
---------------
This role creates a publicly-signed Entrust Datacard certificate.

 - Create a private key.
 - Create a certificate signing request (CSR).
   - Note: Before you can request a certificate, the domain and organization in the CSR must be 
     validated by Entrust Certificate Services. An organization and domain undergo a validation process when signing
     up for an ECS Enterprise account. Additional domain and organization validations are beyond the scope of this example,
     but the process can easily be extended via the cloud portal.
 - Create, reissue, or renew your certificates using the Entrust Certificate Services (ECS) API.
    - Note: You must have Entrust Certificate Services(ECS) API credentials.
      
	  
Requirements
------------ 
 - Ansible version 2.9
 - PyYAML version 3.11 or higher
 - cryptography version 1.6 or higher
 - PyOpenSSL version 0.15 or higher

Role Variables
--------------

See variables in vars/main.yml


Dependencies
------------

None

Example Playbook
----------------

The command below is an example of how to use the role.

Before running the example you will need to: 

	1- Update the contents of api-files with your ECS API certificate and key information.
	2- Update the variables in vars/ as appropriate for the certificate you wish to request and the location you want it.

Navigate to the top level of this role: 
	   
Run command "ansible-playbook sample_playbook.yml"
		
		
License
-------

MIT/BSD

Author Information
------------------

This role was created by Taha Hadreez (ECS testing)
Copyright (c), Entrust Datacard Corporation, 2019
