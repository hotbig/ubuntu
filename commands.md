## Processes
  **Get PID of service**  
  $pidof httpd  
  $pidof chrome  
  
  ps -aux|grep httpd  
  ps -aux|grep chrome  
  
  pgrep vim  
  pgrep httd  
  
  **Kill Processes**  
  $kill [SIGNAL] PID  
  $kill -9 PID  # 9 =SIGKILL, same with "kill -SIGKILL PID"  
  $kill -15 PID # 15=SIGTERM, same with "kill -SIGTERM PID"  
  
  $pkill httpd  # kill process by process name  
  $killall -9 httpd # kill process by process name  
  
  $trap -l # list all signal's name and number  
  
  pgrep vim|xargs kill -9 # kill all processes opened by vim  
  
  **threads**  
  ps -eL -o user,pid,psr,comm,args |more ## check the core number for all threads. (PSR!!)  
  ps -T -l [pid] ### ls thread's priority  

## Files
  find -name '.svn' | xargs rm -rf   
  find . -name "*.lib"|xargs -i cp {} ./libs/  
  grep -r "string to be searched"  /path/to/dir #find the files contains string  

## Performance
  time dd if=/dev/zero of=./test.dbf bs=10k count=300


## Networks
  sudo sshfs -o allow_other -o kernel_cache -o auto_cache -o reconnect -o compression=no -o cache_timeout=600 -o ServerAliveInterval=15 usrename@xxx.xxx.xxx:/dir/dir /dir/dir
  
##### list opened ported on linux  
  netstat -lntu 

## Utils
  cloc .  
  ls|gprep xx|xargs cloc
