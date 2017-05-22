# ansible-role-win_update
Role to Automate Windows Update

# Set Environmental Variable
  export ANSIBLE_VAULT_PASSWORD_FILE=~/.vault_pass

# To Test connection:
  ansible windows -i host -m win_ping --vault-password-file ~/.vault_pass.txt

# Debugging is not enabled by default, you might want to append -vvvvv to enable this if you have issue on first connect.
  If you still have issues you can test connectivity using cURL
    curl -vk -d "" -u "user:pass" https://<windows server ip address>:5986/wsman"

# Run Playbook
  ansible-playbook -i host ./role/main.yml  --vault-password-file ~/.vault_pass.txt
