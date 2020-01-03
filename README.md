DHCP
====

Example Run command
-------------------

    ansible-playbook --private-key <key> -i <inventory> <playbook> -u <user> -K

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Required:
- dhcp_network:
- dhcp_netmask:
- dhcp_broadcast:
- dhcp_gateway:
- dhcp_dns_ns:
- dhcp_ntp_ts:
- dhcp_dns_zone:
- dhcp_dns_search:
- dhcp_range_start:
- dhcp_range_end:

Optional:
- dhcp_leasetime_default: (default: "600")
- dhcp_leasetime_max:     (default: "7200")
- dhcp_failover:          (default: False)
- dhcp_denyunknown:       (default: False)
- dhcp_pxe_server:
- dhcp_pxe_file:


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: dhcp_server
      roles:
         - { role: username.rolename, x: 42 }

      vars:
        dhcp_failover:          True
        dhcp_denyunknown:       True
        dhcp_network:           "192.168.1.0"
        dhcp_netmask:           "255.255.255.0"
        dhcp_broadcast:         "192.168.1.255"
        dhcp_gateway:           "192.168.1.1"
        dhcp_dns_ns:
        - "192.168.1.2"
        - "192.168.1.3"
        dhcp_ntp_ts:
        - "192.168.1.4"
        - "192.168.1.5"
        dhcp_dns_zone:          "anslab"
        dhcp_dns_search:
        - "anslab"
        - "devlab"
        dhcp_range_start:       "10.0.0.100"
        dhcp_range_end:         "10.0.0.150"
        dhcp_leasetime_default: "600"
        dhcp_leasetime_max:     "7200"
        dhcp_pxe_server:        "10.0.0.20"
        dhcp_pxe_file:          "pxelinux.0"

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
