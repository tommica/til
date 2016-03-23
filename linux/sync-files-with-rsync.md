# Sync files with rsync

Local to remote

```bash
rsync --progress --partial --rsh=ssh file.zip user@remote:/path/goes/here
```
