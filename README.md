#Advance Bash Notes

#Linux is extension less
  .txt means nothing

#Everything is a file

#Linux permission
Things a user can do:
  Read(r)
  Write(w)
  Execute(x)

Users that exist:
  -Owner
      Typically the person/user who creates the file, however it can be changed
  -Group
      Every file belongs to a single group. Groups have many users in it and give access to multiple people
  -Others
      Everyone else not in a group or the owner

##Changing permission
chmood <permissions> <path/file>

##Streams, Redirects and Piping

##Streams
  - STDIN
      Standard input
      STDIN code is 0
  - STDOUT
      Standard output
      STDOUT output 1
  - STDERR
      Standard error
      STDERR output 2

#Piping and Redirects
Means that we can join all these commands together

#Redirecting:
###This is redirecting of STDOUT
ls > list_of_ls.text
wc words.txt >word_count.txt        - redirecting

cat words.txt >> word_count.txt     - appending

###This is redirecting of STDIN

wc < words.txt

###Redirecting STDERR
ls non_file_existing 2> log.txt

###Piping |
We sent STDOUT and STDERR into files, but what we want is to be able to send outputs into other programs
This is very powerful and is called Piping.

sort words.txt | head -4

Piping concatenate programs

##Process management
Top
ps - for your processes
ps aux - for all the processes

ps aux | grep vagrant > ps_vagrant_logs.txt

### To kill use kill and the process id (pid)
