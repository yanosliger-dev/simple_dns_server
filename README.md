# simple_dns_server
This is the role for simple dns server

example usage:

inventory

dns_servers:
  dns_master:
    hosts:
      ns1.local:
        ansible_host: 192.168.1.10
  dns_slave:
    hosts:  
      ns2.local:
        ansible_host: 192.168.1.11


