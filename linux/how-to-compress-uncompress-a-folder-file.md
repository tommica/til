# How to compress/uncompress a folder/file from command-line

Compress
```bash
tar -czf folder_name.tar.gz folder_name/
gzip -c file.txt > filename.ext.gz
```

Uncompress
```
tar -xzf folder_name.tar.gz
gzip -d filename.ext.gz
```

[source](http://superuser.com/questions/161706/command-to-gzip-a-folder)
