# hook2mail

![GitHub Verified Creator](https://img.shields.io/badge/GitHub-Verified%20Creator-4493F8?logo=github)
[![Release](https://img.shields.io/github/v/release/cloud-native-aixmarseille/hook2mail)](https://github.com/cloud-native-aixmarseille/hook2mail/releases)
[![Downloads](https://img.shields.io/github/downloads/cloud-native-aixmarseille/hook2mail/total)](https://github.com/cloud-native-aixmarseille/hook2mail/releases)
[![GitHub Stars](https://img.shields.io/github/stars/cloud-native-aixmarseille/hook2mail?style=social)](https://github.com/cloud-native-aixmarseille/hook2mail)

A simple webservice that forwards any e-mail message posted on `/webhook` endpoint to a list of recipients.

example :

```shell
MESSAGE="$(echo 'hello word !' | base64 | jq -R '{ "message": . }')"
curl -X POST -H "Content-Type: application/json" localhost:8000/webhook -d "${MESSAGE}"
```
