# 홈 디렉터리

?> 링크: [https://linuxsurvival.com/linux-home-directories/](https://linuxsurvival.com/linux-home-directories/)

Before we get started on our first exercise, we need to introduce the concept of "home directories".

In a multi-user system, it is convenient for each user to have his or her own private place to store files. Linux calls this private place your "home directory". If your Linux network has been set up in a secure manner, then you are the only regular user who can access the files in your home directory. That is, no one other than yourself and the system administrator can even see the names of your files. However, if you would like to give other people access to your files, you can do so using the "chmod" command.

The location of home directories varies greatly between systems. In the diagram to the right, home directories are located under a directory called "/home", but they could just as easily be located under a directory called "/user". We'll show you how to find out where yours is located.

When you login to your Linux system, you are automatically placed in your home directory. So, if you want to display its pathname, simply login, then type "pwd". In our example, the output would be "/home/keeper".

Because most people need to refer to their home directories on a regular basis, Linux makes them easy to specify. You can use the tilde (~ - it's above the Tab key on your keyboard) everywhere that you would normally use "/home/keeper".

For example, if you wanted to copy a file called "jokes" from your home directory to the "/tmp" directory, you could just type

	         cp ~/jokes /tmp

rather than

               cp /home/keeper/jokes /tmp

You can even use the tilde to specify another user's home directory. If '~' is immediately followed by a User ID, then it no longer refers to your own home directory; it refer's to User ID's home directory. For example, if you wanted to go into bookie's home directory, you could just type

	          cd ~bookie

rather than

	      cd /home/bookie

In fact, '~' by itself is just a short form of "~keeper".

Remember that if you put anything after '~' other than '/', Linux will assume that you are referring to another user's home directory. So, in our "cp ~/jokes /tmp" example above, if we had typed

                        cp ~jokes /tmp

instead, we would have received an error message because there is no User ID called "jokes".

One of the nicest things about using the tilde is that you don't have to know where anyone's home directory is located. Sometimes system administrators will move home directories to new locations to alleviate disk space problems. If you always use the tilde, you might not even notice such moves.

Click the right arrow.

