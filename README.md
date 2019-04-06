![img](https://img.shields.io/badge/Python-2.7-green.svg?style=for-the-badge) ![img](https://img.shields.io/badge/Version-0.0.1-orange.svg?style=for-the-badge)

# PAPA
PAPA (Python Automated Proxy Attacker)

This tool is a local proxy like Burp's Intruder.

The difference is that this one will **automatically** start to fuzzing **_all_** parameters found in GET and POST request.
Even in JSON input.
And it will understand if something appens by content-based detections or by DOM differences and more.
At this time no timing attack will be used to be sure to not have much false positives.

## PLEASE NOTE THAT THIS TOOL IS STILL IN BETA AND IT'S PRONE TO FALSE POSITIVES. IT WILL HAVE ALSO MANY BUGS/CODE PROBLEMS

### SETUP

PAPA uses a lot of dependencies that are pre-installed with python **2.7.13+** and rely on [Proxy2](https://github.com/inaz2/proxy2) for his core.

Additional deps:
- Request
- SQLite3

## THE TOOL WILL BE RELEASED WHEN FUZZER WILL WORK ON JSON PARAMETERS;

Fuzzer parses:
- [x] GET parameters;
- [x] POST parameters;
- [ ] JSON parameters;
- [ ] Cookies;
- [ ] Custom X-* Headers;
- [ ] XML inputs;
- [ ] APIs;

Fuzzer works on:
- [ ] GET parameters;
- [ ] POST parameters;
- [ ] JSON parameters;
- [ ] Cookies;
- [ ] Custom X-* Headers;
- [ ] XML inputs;
- [ ] APIs;

##### ROADMAP:
- [x] Core;
- [x] Proxy;
- [x] Interceptor;
- [ ] Fuzzer;
- [ ] Database (Actually will work with in-memory nested dictionaries and list);
- [ ] Active Analyzer;
- [ ] Passive Anlyzer;
