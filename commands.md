## Files
find -name '.svn' | xargs rm -rf
find . -name "*.lib"|xargs -i cp {} ./libs/
grep -r "string to be searched"  /path/to/dir #find the files contains string

## Performance
time dd if=/dev/zero of=./test.dbf bs=10k count=300


## Networks
sshfs
sudo sshfs -o allow_other -o kernel_cache -o auto_cache -o reconnect -o compression=no -o cache_timeout=600 -o ServerAliveInterval=15 usrename@xxx.xxx.xxx:/dir/dir /dir/dir
