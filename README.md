# RaspberryPi Setup with Ansible

1. Add the vault password into a file:

```sh
echo "<password>" > .vault_pass.txt
```

2. Adjust the `hosts` file.

3. Installing the desktop can be disabled by setting the variable `common_desktop` to `false`. When it's on the installation takes a long time.

4. Then run the playbook:

```sh
ansible-playbook -i hosts --vault-password-file=.vault_pass.txt --diff site.yml
# or just
./run
```
