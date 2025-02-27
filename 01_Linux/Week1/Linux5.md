                                                                                       #  TEXT EDITORS  #

                                                                                       
# Vim [Vi IMproved]:
 it is powerfull text editor commonly used in Linux for coding, configuration editing and Scripting .it is an Enhanced Version of the Vi editor and is highly efficient Once Mastered.

# How to use Vim in Linux via MobaXterm in windows :

** Steps to be followed :

* 1. Open MObaxterm and Connect to LINUX.
* 2. Install Vim (if not installed)
          -> " sudo su - "  # switch to root user.
          -> "yum install vim -yum
          -> exit   #Once done

* 3. Create a New File or open an Existing One 
        -> vim vimtest.text

* 4. Enter Insert Mode ( To Write in the File )

    Once inside vim
    -> press i - this enables Insert Mode, allowing you to type text.

* 5. write your Content 
    -> Hello This is Vim file ;

* 6. Save and exit vim :
     -After writing , press Esc button to exit insert mode then
         * Save & exit    =  :wq + Enter button
         * Save without exiting = :w + Enter button
         * exit without saving = :q! + Enter button

* 7. Verify Your file 
      -> After exiting , you can check the file using  " cat vintest.txt "

# Summary of Vim Commands :

1. open vim                      -      vim filename.txt
2. Insert Mode                   -      press  i
3. Save & exit                   -      press Esc , type :wq , click  Enter
4. Save without exiting          -      press Esc , type :w . click Enter
5. Exit without saving           -      press Esc , type :q! , click Enter
6. Delete a Line                 -      press dd
7. Copy a Line                   -      press yy 
8. paste a Line                  -      press p 
9. undo last change              -      press u 
10. Redo last change             -      press ctrl + r               
