Ansible role: Let's Encrypt certificate getter
==============================================

Acquires Let's Encrypt certificate using certbot's webroot method.

Role Variables
--------------

### In `defaults/main.yml`

- `letsencrypt_email: me@example.com`
- `letsencrypt_domains: [example.com, www.example.com]`
- `letsencrypt_dry_run: true`
- `letsencrypt_test_cert: false`
- `letsencrypt_skip_run: false`
- `letsencrypt_webroot_dir: /var/www/html/`

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: username.rolename, x: 42 }
        - role: mr_class.letsencrypt
          vars:
            letsencrypt_email: hello@example.com
            letsencrypt_domains:
              - example.com
              - www.example.com
            # Disables certbot's dry-run mode.
            letsencrypt_dry_run: false
            # Gets a test certifiate. Change to false when you are sure all is ok.
            letsencrypt_test_cert: true
            #letsencrypt_test_cert: false
            # Set to true if you want to completly skip running certbot.
            letsencrypt_skip_run: false
            letsencrypt_webroot_dir: /var/www/html/

License
-------

MIT