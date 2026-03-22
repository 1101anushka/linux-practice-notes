LINUX COMMANDS PRACTICED
1. Navigation Commands
   
pwd : Displays current working directory

ls : Lists files and directories

ls -l : Shows detailed file info:
Permissions
Owner
Size
Date


cd : Changes directory
cd /path



2. Directory & File Management
   
mkdir : Creates a new directory
mkdir test


rm : Deletes a file
rm file.txt


rm -r : Deletes directory recursively
rm -r test


rmdir : Deletes empty directory only
rmdir test


cp : Copies file
cp file1 file2


mv : Moves or renames file
mv file1 file2


3. File Viewing & Creation
   
touch : Creates empty file which can't be opened or edited
touch file.txt


cat : Displays file content
cat file.txt


zcat : Reads compressed file content
zcat file.gz


head : Shows first 10 lines
head file.txt


tail : Shows last 10 lines
tail file.txt


tail -f : Real-time file monitoring (logs)
tail -f file.txt


less / more : Scrollable file view
less file.txt


4. Text Processing & Utilities
   
wc : Counts Lines Words Characters
wc file.txt


cut : Extracts specific columns or text
cut -d " " -f1 file.txt


tee : Writes output to file + terminal
echo "hello" | tee file.txt


sort : Sorts file content
sort file.txt


diff : Shows difference between files
diff file1 file2


5. Links
ln (Hard Link) : ln file1-path link1

ln -s (Soft Link) : ln -s file1 link1

6. vi Editor
vi file.txt

Modes:

Insert: i
Save: :w
Exit: :q
Save & Exit: :wq

7. System & Process Commands
   
ssh : Remote login
ssh user@host


df : Disk space usage
df -h


du : Directory size
du -sh *


ps : Shows running processes
ps aux


top : Real-time system monitoring
top



kill : Stops process
kill <PID>



fuser : Shows process using file
fuser file.txt



nohup : Runs command in background and displays output of stored file 
nohup command &


free : Memory usage
free -h


vmstat : System performance stats
vmstat

