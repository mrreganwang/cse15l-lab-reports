## Lab Report 3

## Streamlining SSH Configuration
Having to type a long command to log onto the remote server can be cumbersome. We can make the process a bit easier. 

First open up the config file under .ssh/ directory. 
Then, add these lines to the file. 
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22zzz (use your username)
    IdentityFile ~/.ssh/id_rsa

```
Here's an example of it being ran in TextEdit on mac. 

![image](config.png)

Note that in this example, the name after "host" is just an alias, you can change it to whatever name you want. I've decided to use the name "Alias" for my examples. 

Then, you can log onto your remote server using 
```
ssh ieng6
```
Again, the "ieng6" here can be replaced by your own alias. Here's an example of me logging onto my remote account using the above command. 
![image](sshAlias.png)

Now, the scp command from lab report 1 can be ran using the alias for easier transfer of file. Check section 4 from [lab report 1](https://mrreganwang.github.io/cse15l-lab-reports/lab-report-1-week-2) for info on scp command. 

Here's an example of the file transfer. (The file I moved is called "Lab3.java")
![image](scpLab3.png)

## Setup Github Access from ieng6
This is where the public key is stored on my GitHub account
![image](githubKey.png)

On my account, both the private and public key are stored in the .ssh directory. 
![image](ssh.png)

Once the public key has be stored on GitHub, we can now commit and push changes to GitHub while logged onto the remote server. Here's an example of how it's done:
![image](addFile.png)

and here is a screenshot of the commit history on my GitHub account: 
![image](commit.png)

## Copy whole directories with scp -r
To copy a directory takes a bit more than just the `scp` command. We have to copy the files recursively. Here's an example of me copying my MarkdownParse directory to my remote server. 
![image](copyDirectory1.png)
![image](copyDirectory2.png)
![image](copyDirectory3.png)

Here's me running the tests remotely
![image](compile&run.png)

Using what we've learned from lab report 1, the process of copying the directory, compiling the test, and running test can be done in a single step. Here's an example

![image](copy+runTest1.png)
![image](copy+runTest2.png)



