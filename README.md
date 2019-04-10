![img](https://img.shields.io/badge/Python-2.7-green.svg?style=for-the-badge) ![img](https://img.shields.io/badge/Version-0.1-orange.svg?style=for-the-badge) ![img](https://img.shields.io/github/last-commit/h0nus/PAPA.svg?style=for-the-badge)

# PAPA
PAPA (Python Automated Proxy Attacker)

This tool is a local proxy like Burp's Intruder.

The difference is that this one will **automatically** start to fuzzing **_all_** parameters found in GET and POST request.
Even in JSON input.
And it will understand if something appens by content-based detections or by DOM differences and more.
At this time no timing attack will be used to be sure to not have much false positives.

## PLEASE NOTE THAT THIS TOOL IS STILL IN BETA AND IT'S PRONE TO FALSE POSITIVES. IT WILL HAVE ALSO MANY BUGS/CODE PROBLEMS

### TOOL WORKFLOW
This tool will work like that (not in depth):

```
Request > Proxy > Server > Log base response
            |  
           Fuzzer > Change values with  >  Server >  Analyze responses   >  Get warnings  >  Profit!
                     bytes and payloads               for abnormalities      with infos
```
### Video PoC [Just little demo, no attack]
![](demo.gif)

### Use of the tool:
python2.7 paa.py PORT TARGET_DOMAIN

### SETUP
PAPA uses a lot of dependencies that are pre-installed with python **2.7.15+** and rely on [Proxy2](https://github.com/inaz2/proxy2) for his core.

Additional deps:
- Request
- MariaDB
- pyMysql

After this, open Mozilla Firefox and in preferences set the proxy address to 127.0.0.1 and the port to the one chosen.
After that go to certificates and in Authorities just import the .crt file, check the two boxes and finish.
Now you're ready to rock!

## THE TOOL WILL BE RELEASED WHEN FUZZER WILL WORK ON JSON PARAMETERS;

Fuzzer parses:
- [x] GET parameters;
- [x] POST parameters;
- [X] JSON parameters;
- [ ] Cookies;
- [ ] Custom X-* Headers;
- [ ] XML inputs;
- [ ] APIs;

Fuzzer attacks on:
- [ ] GET parameters;
- [ ] POST parameters;
- [ ] JSON parameters; (once here, I'll release the tool)
- [ ] Cookies;
- [ ] Custom X-* Headers;
- [ ] XML inputs;
- [ ] APIs;

##### ROADMAP:
- [x] Core;
- [x] Proxy;
- [x] Interceptor;
- [ ] Fuzzer;
- [x] Database Interaction;
- [ ] Active Analyzer;
- [ ] Passive Anlyzer;
- [ ] Porting to python3;
- [ ] Graphical Interface (maybe);
