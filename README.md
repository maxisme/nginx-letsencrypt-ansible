Heavily influenced by:
    
    - https://gist.github.com/mattiaslundberg/ba214a35060d3c8603e9b1ec8627d349
    
    - https://gist.github.com/plentz/6737338 (I will try keep up to date with the `nginx.j2` but please make a PR if you notice a change)


1. create a new hosts section in your /hosts:
    ```
    [nginxletsencrypt]
    example.com letsencrypt_email=me@example.com domain_name=example.com

    [remove-nginxletsencrypt]
    ```
2. Customise the `roles/add/nginx.j2` for your server (if needed):
    - you can also create a new template for different hosts by creating a new template (say `roles/add/nginx2.j2`) and adding a new variable to the host in the hosts file like: `template=nginx2.j2` 

3. run `$ ansible-playbook playbook.yml`