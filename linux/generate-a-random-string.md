# Generate a random string

Should not be used for passwords!

```bash
cat /dev/urandom | base64 | head -c 11; echo;
```
