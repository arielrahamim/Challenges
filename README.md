# Challenges Solved By Ariel Rahamim

Hack The Bank Wep Application PT Challenge - https://cywar.hackeru.com/challenges/webpt/hack-the-bank

in this challenge you are given a site that you are supposed to scan for any vulnerabilities and find the flag.

i started in checking any xss weakness as well as SQL injection by both manually checking and using automatic tools like SQLMap and xss scanners from github but didn't find anything
then i added in the URL of the site /admin (http://18.216.168.212:50102/admin) and found that the admin panel login is not restricted and is using a service called Feng Office (https://www.fengoffice.com/web/) 
after that with the help of my teacher iv'e used an existing exploit to upload a shell to the site using the existing upload files feature of the site - https://www.exploit-db.com/exploits/35041 
then i excuted the exploit the shell in pycharm while changing the parameters to the site in question and was able to navigate to the /home directory and read flag.txt



Reverse Enginnering Challenge Stage0.exe

in this challenge we were given a file named Stage0.exe and were briefly explained that some companies want that in-house applications will only run in their domain pc's and they are doing so by making thier applications look up a specific value in the registery and if that value doesn't exist , the application will not run.


at first we executed the file with CMD , returned 'Not Ok' and exited - https://prnt.sc/r0quta
then we used ida to try and understand how to make the file run correctly
and we figured out that the file is looking up a specific registery value
then we created that value in our pcs and the file worked! https://prnt.sc/r0qznd
