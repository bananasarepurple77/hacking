## Hashcat
```hashcat sha512-practice.txt wordlist.txt```
will give options for -m, may need to try multiple.

Alternatively, use:
https://hashes.com/en/tools/hash_identifier

```hashcat sha512-practice.txt wordlist.txt -m 1700```

Once tested check the "status" and may need to run command again with "--show" option included.


## John
```
john wordlist=wordlist.txt hash.txt format=HMAC-SHA256
john --format=raw-md5 --wordlist=wordlist.txt hash.txt
john --list=formats
john --help
```

FAQ:
https://github.com/pmittaldev/john-the-ripper/blob/master/doc/FAQ
Github:
https://github.com/pmittaldev/john-the-ripper/tree/master/doc
