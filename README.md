# Linux-Command-Cheat-Sheet
#Linux Cheat Sheet

##File Commands:

ls – directory listing <br>
ls -al – formatted listing with hidden files<br>
cd dir - change directory to dir<br>
cd – change to home<br>
pwd – show current directory<br>
mkdir dir – create a directory dir<br>
rm file – delete file<br>
rm -r dir – delete directory dir<br>
rm -f file – force remove file<br>
rm -rf dir – force remove directory dir *<br>
cp file1 file2 – copy file1 to file2<br>
cp -r dir1 dir2 – copy dir1 to dir2; create dir2 if it doesn't exist<br>
mv file1 file2 – rename or move file1 to file2 if file2 is an existing directory, moves file1 into directory file2<br>
ln -s file link – create symbolic link link to file<br>
touch file – create or update file<br>
cat > file – places standard input into file<br>
more file – output the contents of file<br>
head file – output the first 10 lines of file<br>
tail file – output the last 10 lines of file<br>
tail -f file – output the contents of file as it grows, starting with the last 10 lines<br><br>
##Process Management:

ps – display your currently active processes<br>
top – display all running processes<br>
kill pid – kill process id pid<br>
killall proc – kill all processes named proc *<br>
bg – lists stopped or background jobs; resume a stopped job in the background<br>
fg – brings the most recent job to foreground<br>
fg n – brings job n to the foreground<br><br>
##File Permissions:

chmod octal file – change the permissions of file to octal, which can be found separately for user, group, and world by adding:<br>
4 – read (r)<br>
2 – write (w)<br>
1 – execute (x)<br><br>
###Examples:

chmod 777 – read, write, execute for all<br>
chmod 755 – rwx for owner, rx for group and world<br><br>
##SSH:

ssh user@host – connect to host as user<br>
ssh -p port user@host – connect to host on port port as user<br>
ssh-copy-id user@host – add your key to host for user to enable a keyed or passwordless login<br><br>
##Searching:

grep pattern files – search for pattern in files<br>
grep -r pattern dir – search recursively for pattern in dir<br>
command | grep pattern – search for pattern in the output of command<br>
locate file – find all instances of file<br><br>
##System Info:

date – show the current date and time<br>
cal – show this month's calendar<br>
uptime – show current uptime<br>
w – display who is online<br>
whoami – who you are logged in as<br>
finger user – display information about user<br>
uname -a – show kernel information<br>
cat /proc/cpuinfo – cpu information<br>
cat /proc/meminfo – memory information<br>
man command – show the manual for command<br>
df – show disk usage<br>
du – show directory space usage<br>
free – show memory and swap usage<br>
whereis app – show possible locations of app<br>
which app – show which app will be run by default<br><br>
##Compression:

tar cf file.tar files – create a tar named file.tar containing files<br>
tar xf file.tar – extract the files from file.tar<br>
tar czf file.tar.gz files – create a tar with Gzip compression<br>
tar xzf file.tar.gz – extract a tar using Gzip<br>
tar cjf file.tar.bz2 – create a tar with Bzip2 compression<br>
tar xjf file.tar.bz2 – extract a tar using Bzip2<br>
gzip file – compresses file and renames it to file.gz<br>
gzip -d file.gz – decompresses file.gz back to file<br><br>
##Network:

ping host – ping host and output results<br>
whois domain – get whois information for domain<br>
dig domain – get DNS information for domain<br>
dig -x host – reverse lookup host<br>
wget file – download file<br>
wget -c file – continue a stopped download<br><br>
##Installation:

dpkg -i pkg.deb – install a package (Debian)<br>
rpm -Uvh pkg.rpm – install a package (RPM)<br><br>
##Install from source:

./configure<br>
make<br>
make install<br><br>
##Shortcuts:

Ctrl+C – halts the current command<br>
Ctrl+Z – stops the current command, resume with<br>
fg in the foreground or bg in the background<br>
Ctrl+D – log out of current session, similar to exit<br>
Ctrl+W – erases one word in the current line<br>
Ctrl+U – erases the whole line<br>
Ctrl+R – type to bring up a recent command<br>
!! - repeats the last command<br>
exit – log out of current session<br>
