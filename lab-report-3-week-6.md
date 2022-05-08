# Lab Report3:

## Streamlining ssh Configuration:

I edited my `config` in mac terminal:

<img width="641." alt="Screen Shot 2022-05-08 at 11 44 05 AM" src="https://user-images.githubusercontent.com/97696773/167310818-edb60229-43b0-4b2b-b7e2-781b8fa0fba5.png">

To edit `config` file, I use `vim config`. 

<img width="641" alt="Screen Shot 2022-05-08 at 11 48 20 AM" src="https://user-images.githubusercontent.com/97696773/167310980-739d80a6-0018-4fd5-9a08-723885205a5e.png">


<img width="641" alt="Screen Shot 2022-05-08 at 11 46 21 AM" src="https://user-images.githubusercontent.com/97696773/167310897-507102b3-b9bf-4552-94b0-45c98cab1f2d.png">

Using only `ssh ieng6` to log into school account:

<img width="641" alt="Screen Shot 2022-05-08 at 11 50 04 AM" src="https://user-images.githubusercontent.com/97696773/167311069-cd14f145-43e2-47c3-a750-632c133abe66.png">


Then in the terminal, use `scp file_name ieng6:~/` to copy my file from my PC to my account:
<img width="641" alt="Screen Shot 2022-05-08 at 12 01 29 PM" src="https://user-images.githubusercontent.com/97696773/167311525-f90e6b9a-9624-4f84-8b10-520c619e0f95.png">


## Setup Github Access from ieng6:

To store the public key, you can go to `settings` -> `SSH and GPG keys` (in the `Access`), by clicking `New SSH key`, you can add your github key. 

<img width="1287" alt="Screen Shot 2022-05-08 at 2 44 24 PM" src="https://user-images.githubusercontent.com/97696773/167317052-af40ad23-4baa-4b6b-8eef-9a8b668cec3f.png">

On my user acount, I stored my github key in `.ssh`, as you can see the below screenshot and there is a file called `id_rsa_github`:


<img width="632" alt="Screen Shot 2022-05-08 at 2 52 19 PM" src="https://user-images.githubusercontent.com/97696773/167317294-0dab3525-4e32-4ddd-b376-e0a271dabf91.png">


Running `git push origin main` on my user account, the result please see the below screenshot:

<img width="719" alt="Screen Shot 2022-05-08 at 2 54 09 PM" src="https://user-images.githubusercontent.com/97696773/167317341-debd030c-9c6e-4e8c-92cd-8a9fba306ef0.png">

The link to the resulting commit:
[Resulting Commit]()


