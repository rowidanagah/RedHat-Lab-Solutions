1- List the user commands and redirect the output to /tmp/commands.list
```sh
cat /etc/passwd > /tmp/commands.list
```
![image](https://user-images.githubusercontent.com/52299389/213921516-2f6cbcaf-9d6e-4d35-8fe6-5b23e2fc5f3d.png)

<hr>

2- Count the number of user commands

![image](https://user-images.githubusercontent.com/52299389/213921674-dd4973d3-f926-4f97-886d-a190632301a9.png)


<hr>

3- Get all the users names whose first character in their login is ‘g’.
  - The following command could only hightlight line that starts with g and print the whole line
```sh
grep '^g* /etc/passwd
``` 
  - To extract user name, use `:` as a delemeter and cut ,to extract,username as a first pattern or index. `cut -d ":" -f 1`
```sh
cat /etc/passwd | cut -d ":" -f 1 | egrep "^g"
```
![image](https://user-images.githubusercontent.com/52299389/213922165-41d1ceb5-526a-4f6c-97ff-1ac914efe5ac.png)


<hr>

4- Get the logins name and full names (comment) of logins starts with “g”
  - _using `who` commands_
  
  ```sh
  $ who | cut -d' ' -f1 | sort | uniq

  ```
![image](https://user-images.githubusercontent.com/52299389/213922756-aef062a7-5cef-42a6-b7e6-6b4745811c3d.png)

<hr>

5- Save the output of the last command sorted by their full names in a file.

![image](https://user-images.githubusercontent.com/52299389/213923177-9524ed2b-3ad8-48c8-b47b-cb898b0e5d9b.png)

6- Write two commands: 
  - first: to search for all files on the system that named
.bash_profile. 

![image](https://user-images.githubusercontent.com/52299389/213924371-09ddcfbd-6bb6-4591-937e-2582fe0fb405.png)

  - Second: sorts the output of ls command on / recursively, Saving
their output and error in 2 different files and sending them to the background.

![image](https://user-images.githubusercontent.com/52299389/213924299-dcde1138-ffaa-45eb-935e-6780fc3d7569.png)



<hr>

7- Display the number of users who is logged now to the system
![image](https://user-images.githubusercontent.com/52299389/213924591-4649d577-4ae4-41a0-9001-e86cddf34602.png)

<HR>
 
8 - Display lines 7 to line 10 of /etc/passwd file
  
  ```sh
  sed -n '7,10p' /etc/passwd 
  ```
  _OR_
  ```sh
  head -10 /etc/passwd | tail +7
  ```
![image](https://user-images.githubusercontent.com/52299389/213925225-6b560c7f-cec6-4f78-9515-820f13d620d6.png)

9. What happens if you execute:
  - cat filename1 | cat filename2
  - ls | rm
  - ls /etc/passwd | wc –l
 
![image](https://user-images.githubusercontent.com/52299389/213925418-08080140-bce0-4fb0-abbf-bdc9fde6137d.png)

 <HR>
  
10 - Stop the last command
  
  ![image](https://user-images.githubusercontent.com/52299389/213925737-84c7fa56-9584-4f52-90df-fbefb5b6dcf3.png)
  
<HR>
  
11- Resume the last command in the background , 12- Issue the jobs command and see its output.
![image](https://user-images.githubusercontent.com/52299389/213925798-dddd932b-d73e-4ea6-a663-8f29e46bc211.png)
  
 
  <HR>
 12- Send the sleep command to the foreground and send it again to the background
    
    ![image](https://user-images.githubusercontent.com/52299389/213925883-0ed86922-a9e3-48fd-9b37-dbeac0a42ef4.png)
    
<HR>
  
  
<HR>

 15- Kll the sleep command.
  ![image](https://user-images.githubusercontent.com/52299389/213925983-2c0d2609-b9b5-4ab9-8aba-03c438044ee4.png)

  
  <hr>
  
  16- display your processes only
![image](https://user-images.githubusercontent.com/52299389/213926023-403061e5-1a20-4989-874f-df468271cd6b.png)

