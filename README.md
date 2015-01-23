Vitadock OAuth dance Python Client Implementation
=============


```python
import vitadock

c = vitadock.VitadockOauthClient("APP_KEY_GOES HERE","APP_SECRET_GOES_HERE")

c.getRequestTokens()

print "access token:", c.request_token
print "access token secret:", c.request_token_secret

print "GOTO: " + c.authorization_url + "?oauth_token=" + c.request_token

verifier = raw_input("What is the verifier? (second line)")

c.getAccessTokens(verifier)

print "access token:", c.access_token
print "access token secret:", c.access_token_secret
```python


Requirements
============

* Python 2.6+