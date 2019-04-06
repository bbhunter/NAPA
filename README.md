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

- SQLite3

##### ROADMAP:
- [x] Core;
- [x] Proxy;
- [x] Interceptor;
- [ ] Fuzzer;
- [ ] Database;
- [ ] Active Scanner;
- [ ] Passive Anlyzer

