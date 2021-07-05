## Basic work with files

- Create directory test1 
```console
mkdir test1
```  

- Create file test1.txt inside the test1 directory. - cd test1, touch test1.txt

-   Create copy of folder test1 with name test2.  - cp -R test1 test2

-    Delete file test1.txt inside test2 directory. - cd test2, rm test1.txt

-    Rename test2 folder into directory_without_file - mv test2 directory_without_file 

-    Insert 'test1' text into test1/test1.txt file. - echo 'test1' > test1.txt 

-    print the text from the test1/test1.txt file. - cat test1.txt

-    Insert 'test2' into the end of test1/test1.txt file. - echo 'test2' >> test1.txt 

-    print the text from the test1/test1.txt file. - cat test1.txt

- check the size of test1 directory - du -sh test1

## Permissions

-   Create test directory and block access for all to it. - chmod ugo-rwxs

-   Try to remove that directory. - rmdir 


-    Create simple script which prints current date. Try to execute it. - echo 'date' > script.sh, bash script.sh


## Log checking

-  Count lines in the file test.txt. - wc -l test.txt


- Show last 3 lines from the test.txt file. - tail -3 test.txt


-  Hom many uniq IP addresses accessed the website ? - awk {'print $1'} test.txt | sort | uniq -c | wc -l


-  IP address with most requests. - awk {'print $1'} test.txt | uniq -c | sort | tail -1


-  Top 3 IP addresses by amount of POST requests. - grep 'POST' test.txt


-  Which IP addresses received 403 error ? - grep ' 403' test.txt | awk {'print $1'}


- Task with * . Write script to show which pages Google checked from the website - echo 'grep "Google"' test.txt > scriptWith*.sh

## Replace

Replace IP address with most requests on 127.0.0.1 in test.txt file - awk {'print $1'} test.txt | sort | uniq -c | sort -n | tail -1, sed  's/114.119.140.234/127.0.0.1/' test.txt
