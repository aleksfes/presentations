# My notes

## Error 'Error: ENOSPC: System limit for number of file watchers reached'

Run to fix it. [Source](https://github.com/facebook/jest/issues/3254)
```bash
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```
