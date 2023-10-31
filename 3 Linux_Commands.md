# Run `whoami` command to check current user.

# Run `id` command.to check id

# Which command you will use to switch to ansible user?

su ansible

# Run sudo ls /root/ command to check files under /root directory.


# Which command can't be used to download file over internet?

curl


ping


wget

answer: ping


# Download target file to host01


target file name : dummy.pdf

target file URL: https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf

target directory: /home/thor



Run `cd /home/thor; curl -O https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`

or

`wget https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf -O /home/thor/dummy.pdf` to download file.

The `wget` command you've provided is used to download a file from a remote URL and save it with a specific name and location on your local machine. 

In the command you've provided, you are trying to download a PDF file from a remote URL (https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf) and save it as "dummy.pdf" in the "/home/thor" directory.

Here's the breakdown of the command:

- `wget`: This is the command-line utility for downloading files from the web.
- `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`: This is the URL of the remote PDF file you want to download.
- `-O`: This option is used to specify the output file name.
- `/home/thor/dummy.pdf`: This is the local path where the downloaded PDF file will be saved with the name "dummy.pdf."

When you run this command, it will download the PDF file from the specified URL and save it as "dummy.pdf" in the "/home/thor" directory on your local machine. Make sure you have the necessary permissions to write to the specified directory.




