# Run `rpm -q openssh-server python3 ansible telnet` . Alternatively run `rpm -qa` to list all installations.


# Install ftp with rpm.

We have downloaded rpm file inside /opt/ directory.


## Run `sudo rpm -i /opt/ftp-0.17-67.el7.x86_64.rpm`

The `rpm` command you've provided is used to install an RPM package in a Linux system. In your command, you're attempting to install an RPM package with the file path "/opt/ftp-0.17-67.el7.x86_64.rpm."

Here's the breakdown of the command:

- `sudo`: This is used to run the `rpm` command with superuser (root) privileges. You'll be prompted to enter your password to confirm the installation, as installing software typically requires elevated permissions.

- `rpm -i`: This is the `rpm` command with the `-i` option, which stands for "install." It's used to install RPM packages.

- `/opt/ftp-0.17-67.el7.x86_64.rpm`: This is the full path to the RPM package file that you want to install.

When you run this command with `sudo`, it will attempt to install the specified RPM package on your system. Make sure the RPM package is compatible with your Linux distribution and architecture, and that you have the necessary permissions to install software on your system.

Please be cautious when installing software using the `rpm` command, especially if you are not sure about the source and integrity of the RPM package, as installing software from untrusted or unverified sources can pose security risks.

# Remove ftp with rpm.


You can get exact package name by rpm -qa | grep ftp

Run `sudo rpm -e ftp-0.17-67.el7.x86_64`


`rpm -e`: This is the rpm command with the -e option, which stands for "erase" or "uninstall." It's used to remove RPM packages from the system.

# Install ansible with yum.

Run: `sudo yum install -y ansible`


`-y`: This option is used to automatically answer "yes" to any prompts, which can be useful for unattended installations.


# install specific version
### `sudo yum install -y ansible-2.8.11`


