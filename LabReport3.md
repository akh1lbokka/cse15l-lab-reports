# Lab Report 3 - Copying whole directories with `scp - r`
This week, my lab report will be focused on copying over whole directories from my local computer to my ieng computer. I chose it because it was the easiest option. Let's get started!

## Show copying your whole markdown-parse directory to your ieng6 account
<img width="1203" alt="Screen Shot 2022-02-10 at 11 41 40 AM" src="https://user-images.githubusercontent.com/97696757/153520012-8731930d-489a-4973-9eb2-2be7541c4c6f.png">

In this screenshot, I used the command `scp -r (directory name) (ssh login):~/` to copy over my local markdownparse directory to my ieng account. The `-r` signifies for the terminal to copy over the files recursively, so all files inside the directory will get copied over. After I input my passphrase in the terminal, the files where copied over successfully to the directory. 

## Show logging into your ieng6 account after doing this and compiling and running the tests for your repository
<img width="1182" alt="Screen Shot 2022-02-10 at 4 12 59 PM" src="https://user-images.githubusercontent.com/97696757/153520032-0f33030f-edd0-4c91-805f-b81155999543.png">

In this screenshot, I logged into my ssh by command `ssh (ssh login)` and then inputing my passphrase. After that, I changed my directory to the copied over markdownparse directory, and then ran the javac and java commands to compile and run the tests. As shown in the picture, the tests compiled and ran successfully.

## Show (like in the last step of the first lab) combining scp, ;, and ssh to copy the whole directory and run the tests in one line.
![Screen Shot 2022-02-10 at 4 37 39 PM](https://user-images.githubusercontent.com/97696757/153520795-e5493ef5-d179-4bfe-b5cd-e750edcb7335.png)


In this picture, I logged out of ieng and went back to the markdown parse local directory. Since we can run multiple commands in succession to another in one go, I put all the required commands in the command line, and used `;` to separate them. The terminal asked for my password, and once put in, the tests immediately compiled and ran correctly!


