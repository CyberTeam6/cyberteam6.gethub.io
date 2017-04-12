# Cryptography
Collection of websites and scripts that pertain to Cryptography

* Wytshadows RSA Script

```py
#!/usr/bin/pyton

#p:   937
#q:   641
#e:   65537
#d:   489473
#phi: 599040
#cipher1: BAD
#cipher2: FADE

p = raw_input("p: ")
q = raw_input("q: ")
e = raw_input("e: ")
phi = (int(p)-1) * (int(q)-1)
print phi
for d in range(0, 10000000):
    one = (int(e) * d) % phi
    if one == 1:
        print str(d) + "GOT IT!"
	break
```

### Links
  * [Crypto Pals](http://cryptopals.com/) - A website with crypto challenges
  * [featherduster](https://github.com/nccgroup/featherduster) - An automated, modular cryptanalysis tool
  * [id0-rsa](https://id0-rsa.pub/) - Another website with crypto challenges
  * [RSA Worksheet](https://www.cs.drexel.edu/~jpopyack/IntroCS/HW/RSAWorksheet.html) - RSA Calculator
