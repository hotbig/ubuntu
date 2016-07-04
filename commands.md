## file operations 



## Performance
time dd if=/dev/zero of=./test.dbf bs=10k count=300


## Networks
sshfs
sudo sshfs -o allow_other -o kernel_cache -o auto_cache -o reconnect -o compression=no -o cache_timeout=600 -o ServerAliveInterval=15 usrename@xxx.xxx.xxx:/dir/dir /dir/dir
