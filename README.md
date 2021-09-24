Reset k3s cluster
=========

This role reset changes caused by:

  - https://github.com/lucaslehnen/k3s-install
  - https://github.com/lucaslehnen/k3s-config-master
  - https://github.com/lucaslehnen/k3s-config-worker

Example
----------------

In your `main.yml`:

```yaml
- hosts: servers
  roles:
      - k3s-reset
```

In your `requirements.yml`:

```yaml
- name: k3s-reset
  src: https://github.com/lucaslehnen/k3s-reset
  version: v1.0.0
```

Define target hosts in your inventory file `hosts`:

    [servers]
    192.168.99.11
    192.168.99.12
    192.168.99.13

Install requirements:

```
ansible-galaxy install -r requirements.yml
```

Call the playbook:

    ansible-playbook -i hosts main.yml

License
-------

MIT

Author
------------------

https://github.com/lucaslehnen
