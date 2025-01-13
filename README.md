> # simple_dns_server
This is the role for simple dns server

example usage:

inventory

    dns_master:
    hosts:
      ns1.local:
        ansible_host: 192.168.1.10
    dns_slave:
      hosts:
        ns2.local:
          ansible_host: 192.168.1.11
        

Vars:
Example:

    dns_zones:
      - name: test.com
        inaddr: 0.168.192
        serial: 1
        type: master
        ttl: 2d
        email_notify: admin
        a_records:
          - suffix: ns1
            ip: 192.168.0.1
          - suffix: www
            ip: 192.168.0.100

Vars override:

    simple_dns_server_bind_log_directory: /var/log/bind
    simple_dns_server_bind_zones_directory: /etc/bind/zones
    simple_dns_server_bind_packages:
      - bind9
      - bind9utils
      - bind9-doc

    simple_dns_server_bind_delete_zones: true
    simple_dns_server_bind_backup_zones: true
    simple_dns_server_bind_forwarders:
      - 8.8.8.8
      - 1.1.1.1
    simple_dns_server_trusted_bind_servers:
      - localhost
      - localnets





