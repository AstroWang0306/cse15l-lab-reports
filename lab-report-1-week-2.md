# Lab Report1:

## Installing VsCode: 
    
   Here's where you can downlaod VsCode

   [VsCode](https://code.visualstudio.com/download)
  
  After downloading, you can open the VsCode and you should be able to see your window like this: 

<img width="692" alt="Screen Shot 2022-04-09 at 11 16 14 AM" src="https://user-images.githubusercontent.com/97696773/162586673-0cfdaafd-18bc-487f-b3bc-fe30ffe2255b.png">

    
## Remotely Connecting:

  Open the VsCode and click the terminal:

  The coommand you have to enter: `ssh cs15lsp22zz@ieng6.ucsd.edu`, 
  
  "zz" depends on your account name, each student has his/her own account name:
  
  To look at your account, please go to here: [CSE Account](https://sdacs.ucsd.edu/~icc/index.php)
  
  Below is when you successfully log into the SSH:

  Red frame are refered as account and password, password is not visible, so please carefully enter
  
  <img width="704" alt="Screen Shot 2022-04-09 at 11 29 44 AM" src="https://user-images.githubusercontent.com/97696773/162587506-fb4f8f5e-b09c-49d6-b326-118df92dee80.png">

## Trying Some Commands: 

    a. `ls` : you can see what file you have right now
    
<img width="1113" alt="Screen Shot 2022-04-09 at 12 15 08 PM" src="https://user-images.githubusercontent.com/97696773/162588563-5aed8b2e-06c5-45bf-b257-aba9eaf3f1cd.png">
    
    b. `cd <folder_name>` : you can go to the folder
    
<img width="1138" alt="Screen Shot 2022-04-09 at 12 18 28 PM" src="https://user-images.githubusercontent.com/97696773/162588638-aebd8a02-fb7a-40c7-abd0-b58b7f831432.png">
    
    c. `cd ..` : go back to the previous directory
    
<img width="827" alt="Screen Shot 2022-04-09 at 2 22 37 PM" src="https://user-images.githubusercontent.com/97696773/162592059-7c18f11a-0ec4-4de3-b913-3c3c0058df13.png">

    
    d. `ls -a` : will list all of the files, including hidden files
    
<img width="1057" alt="Screen Shot 2022-04-09 at 2 20 44 PM" src="https://user-images.githubusercontent.com/97696773/162592014-35afd8c9-859a-4511-a70f-f449d4db5c43.png">
    
4. Moving Files with `scp`:

    If you have already logged into SSH, you have to log out in order to copy your file from your PC. 
    
    Reminder: Please go to the directory where you want to copy the file, otherwise, you might get errors since there is no 
    such file in the directoy
    
    As the below picture, I stored my file WhereAmI.java on the Desktop. so I have to `cd Desktop` to find my file
    
    Then, use the coomand to copy the fily to SSH: `scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/`
    
    After entering this command, it will require to enter the password, which is your SSH password. 
    
    When logging into your SSH, enter `ls` and should see your file was copied. 
    
    <img width="1331" alt="Screen Shot 2022-04-09 at 2 41 37 PM" src="https://user-images.githubusercontent.com/97696773/162592524-d9467f0f-0ed0-4dbc-8928-f63ab7068698.png">

## Setting an SSH Key

    a. Get your key on the client:
    
<img width="632" alt="Screen Shot 2022-04-09 at 3 13 04 PM" src="https://user-images.githubusercontent.com/97696773/162593194-d4d0b3ef-1cbb-46ee-9c7e-290dc396e8e3.png">
    
    b. We have to copy the public key to the `.ssh` directory of the user account on the server:
    
<img width="584" alt="Screen Shot 2022-04-09 at 3 16 33 PM" src="https://user-images.githubusercontent.com/97696773/162593253-126226ff-226c-4630-9991-c25842ee61df.png">
<img width="852" alt="Screen Shot 2022-04-09 at 3 18 09 PM" src="https://user-images.githubusercontent.com/97696773/162593308-52d9d024-8bd5-4352-bd8c-4787a42d1861.png">
    
    c. After doing the above steps, you should able to log in without passwords by just entering `ssh cs15lsp22zz@ieng6.ucsd.edu`
    
<img width="571" alt="Screen Shot 2022-04-09 at 3 20 10 PM" src="https://user-images.githubusercontent.com/97696773/162593350-405fd7d2-6512-4aca-b97e-c0bfda53a4e7.png">
  
## Optimizing Remote Running

    a. By adding a command after `ssh cs15lsp22zz@ieng6.ucsd.edu "ls"`, you will be logging in and see the listed files you have. 
    
    Reminder: You can use up-arrow to get the previous command you havr entered and save some time.
    
 <img width="508" alt="Screen Shot 2022-04-09 at 3 25 18 PM" src="https://user-images.githubusercontent.com/97696773/162593466-d5a9fc1a-8d0b-464a-a136-f28e9c5c289b.png">
    
    b. By using semicolons, you can run multilpe coommands in the same line.
    
<img width="588" alt="Screen Shot 2022-04-09 at 3 32 04 PM" src="https://user-images.githubusercontent.com/97696773/162593665-4d0752af-a8f2-4971-b49a-9582e8136bc6.png">





    
    








  


 
 
