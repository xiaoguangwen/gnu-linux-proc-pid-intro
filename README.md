[/proc/[pid]/cmdline](#cmdline)
[/proc/[pid]/environ](#environ)


## cmdline
`/proc/[pid]/cmdline`是一个只读文件，包含进程的完整命令行信息。如果这个进程是`zombie`进程，则这个文件没有任何内容。举例如下：    

    # ps -ef | grep 2948
    root       2948      1  0 Nov05 ?        00:00:04 /usr/sbin/libvirtd --listen

    # cat /proc/2948/cmdline
    /usr/sbin/libvirtd--listen

## environ  
`/proc/[pid]/environ`显示进程的环境变量。举例如下：  

    # strings /proc/2948/environ
    LANG=POSIX
    LC_CTYPE=en_US.UTF-8
    PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
    NOTIFY_SOCKET=@/org/freedesktop/systemd1/notify
    LIBVIRTD_CONFIG=/etc/libvirt/libvirtd.conf
    LIBVIRTD_ARGS=--listen
    LIBVIRTD_NOFILES_LIMIT=2048
