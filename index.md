# Installing VScode
<img width="1036" alt="Screen Shot 2022-01-06 at 10 39 59 AM" src="https://user-images.githubusercontent.com/97696757/149589274-742c863d-3cad-463b-b75e-2c3466d66db3.png">
First thing I did here to get started was head over to the Visual Studio Code Website to download VSCode. VSCode is an Itegrated Coding Environment that is very helpful because it has a lot of features. The website is pretty easy to navigate, so download the VSCode software that is for your current operating system. Then, go through the steps to install the software and open it up. Your screen should look like the picture above. Here is a link for the VScode download!: [Link](https://code.visualstudio.com/).
# Remotely Connecting
<img width="1179" alt="Screen Shot 2022-01-14 at 1 53 35 PM" src="https://user-images.githubusercontent.com/97696757/149590245-1a99bee9-7713-4579-bfb8-d14e20d0afa7.png">
Next, open up a new terminal by going to the menu bar > terminal > new terminal. Type in `ssh <insert your @ieng username here>`. For example, I typed in `ssh cs15lwi22ajt@ieng6.ucsd.edu` (You can look up your email with UCSD's account lookup tool. If you are connecting for the first time, the terminal will ask you if you are sure you want to connect, type yes. Then, type in your password. Your screen should now look like the image above. Here is a link to look up your SSH account!: [Link](https://sdacs.ucsd.edu/~icc/index.php). 
# Trying Some Commands
<img width="1027" alt="Screen Shot 2022-01-14 at 1 56 47 PM" src="https://user-images.githubusercontent.com/97696757/149590652-5ca4f976-1086-4742-8686-3141e86f4e34.png">
Now that you are connected, you can run some commands to test out the remote server. The image above provides some examples. `ls` lists all files in the current Directory. `pwd` means "print working directory", so it shows which directory you are in and how to get to that directory. `cd` means change directory, so using that followed up by another directory's name changes the director you are currently working with to the desired one. Type `exit` to disconnect from the server. 
# Moving Files with scp
<img width="909" alt="Screen Shot 2022-01-14 at 2 10 40 PM" src="https://user-images.githubusercontent.com/97696757/149591982-a68d527b-b4c0-4ac3-bf3d-bd5941a4154c.png">
Moving files from your computer to the remote server is quite simple as well. While you are in the directory of the desired file in the terminal, type `scp <desired file> <ssh login>:~/`. You will get prompted for a passsword, but after entering the password, the file should successfully send over. Look at the image above for an example of what i did. 
# Setting an SSH Key
<img width="960" alt="Screen Shot 2022-01-14 at 2 25 11 PM" src="https://user-images.githubusercontent.com/97696757/149593187-de86c1ee-0c8c-4e8e-a8c5-96b104d34909.png">
<img width="1009" alt="Screen Shot 2022-01-14 at 2 25 23 PM" src="https://user-images.githubusercontent.com/97696757/149593195-2bc4a3a8-5b4e-4b11-bb8c-5ce059465882.png">
To make remote running more efficient, we can create an SSH key to not have to type in our password every time we ssh or scp from our client. I Did this by generating an SSH key, and placing the id in the remote server. Look at the images for the specific commands. Now I can ssh and scp much faster. 
# Optimizing Remote Running
<img width="1004" alt="Screen Shot 2022-01-14 at 2 45 48 PM" src="https://user-images.githubusercontent.com/97696757/149595003-0af462e3-10e2-4a28-a376-3b702d843359.png">
In order to make the remote work process more efficient, you can type in commands directly after an ssh command to run it faaster. This way you do not have to wait 
until you are connected to run the code. Also, you can run multiple commands in one line by separating them in by semicolons. These tips can help you be a more efficient remote worker- see the image above for examples. 
