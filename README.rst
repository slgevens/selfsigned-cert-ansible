Generate a selfsigned certificate
###################################
.. sectnum::


Context
=========

A role to generate a selfsigned certificate x509 usable for stunnel and other applications/services

Playbook example
=================
::

     roles:
     - role: selfsigned-cert-ansible
         cert_path: /etc/stunnel/stunnel.pem

	 cert_owner: root
	 cert_group: root
	 cert_mode: 0600
	
	 cert_days: 3650

	 cert_country: FR
	 cert_state: France
	 cert_city: Paris
	 cert_organisation: Epiconcept
	 cert_common_name: '{{ ohai_fqdn }}'

       
     - include_role: name=selfsigned-cert-ansible

License
==========

MIT_

.. _MIT: LICENSE

Author
=======

Evens SOLIGNAC - evenssolignac@live.fr
