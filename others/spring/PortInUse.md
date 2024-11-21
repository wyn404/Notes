
找到占用8080端口的应用进程
netstat -ano | findstr 8080

杀死该进程
taskkill -PID XXX -F

