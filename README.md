# Single SCRAM secured MongoDB istalation on Debian

All in one playbook.

Set variables before use:
    mongodb_version: "6.0"  # MongoDB version to install
    mongodb_user: "mongoadmin"  # MongoDB admin user
    mongodb_password: "mongoadmin_password"  # MongoDB admin password
    mongodb_database: "admin"  # MongoDB admin database
    mongodb_port: 27017  # MongoDB port
    mongodb_bind_ip: "0.0.0.0" # MongoDB bind IP (0.0.0.0 to allow remote connections)
    non_root_user: "new_linux_user"  # New non-root user
    non_root_password: "linux_user_password"  # Password for the new non-root user
    user_public_key: "/path/to/ssh_key.pub"  # Replace with the path to your SSH public key

Non root Linux user will pe used for SSH connection to Debian. 

ansible-playbook -i your_inventory_file.yaml install-mongo-debian.yaml

