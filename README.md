# ansible-role-kibana

Tested on Ansible 2.4.2 and Ubuntu 16.04

This role depends on a
[docker](https://github.com/blurblah/ansible-role-docker) role and installs elasticsearch running on a docker container.

Referenced by a
[Configuring Kibana on Docker](https://www.elastic.co/guide/en/kibana/6.2/_configuring_kibana_on_docker.html) document.

## Playbook sample
This sample playbook installs kibana.

* **server_name (optional)** : default is kibana
* **http_port (optional)** : default is 5601
* **es.host (optional)** : Host ip of the Elasticsearch which will be queries by Kibana. Default value is the host ip which Kibana will be installed.
* **es.port (optional)** : Host port of the Elasticsearch. Default port is 9200
* **version (optional)** : default is 6.2.3

```yaml
- hosts: kibana_host
  become: yes
  roles:
    - role: kibana
      server_name: test-kibana
```
