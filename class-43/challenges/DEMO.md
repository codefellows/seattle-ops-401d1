# Ops Challenge - Attack Tools Part 3 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

This example script scans for the FTP vulnerability described in https://www.scanforsecurity.com/penetration-testing/automating-actions-attacker-using-metasploit-and-python.html


```bash
from metasploit.msfrpc import MsfRpcClient
from metasploit.msfconsole import MsfRpcConsole
client = MsfRpcClient('password')
console = MsfRpcConsole(client, cb=read_console)

global global_positive_out
global_positive_out = list()
global global_console_status
global_console_status = False

def read_console(console_data):
    global global_console_status
    global_console_status = console_data['busy']
    print global_console_status
    if '[+]' in console_data['data']:
	sigdata = console_data['data'].rstrip().split('\n')
	for line in sigdata:
	    if '[+]' in line:
		global_positive_out.append(line)
    print console_data['data']

console.execute('use auxiliary/scanner/ftp/ftp_version')
console.execute('set RHOSTS 192.168.0.0/24')
console.execute('set THREADS 20')
console.execute('run')
time.sleep(5)

while global_console_status:
    time.sleep(5)

targets = list()
for line in global_positive_out:
    if 'FreeFloat' in line:
    	ip = re.findall(r'[0-9]+(?:\.[0-9]+){3}', line)[0]
	targets.append(ip)
```
"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top


