# notipy
A module for quickly sending email alerts from python code.


This script was created to notify (hence, notipy :) me when a job was completed (and possibly send exit status and results)


Compatible with both python2 and python3


# Instructions
Create file  `sendDetails1.txt` containing the following contents (see template sendDetails.txt as an example)
```
email:nbauto791@gmail.com
password:<redacted>
server:smtp.gmail.com
port:587
```
To run:
```
import notipy
notipy.sendMail("to@address.com", "This is a message")
```

### Notes
`sendDetails1.txt` is include in `.gitignore` so that it doesn't sync.

Use `sendMailAsync(..)` to send mail in the background without blocking the sending process.

Send statuses are logged in `notipy.log`. The file written to can be changed in the `#Constants` section of `notipy.py`