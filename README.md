# Challenges Solved By Ariel Rahamim

Hack The Bank Wep Application PT Challenge - https://cywar.hackeru.com/challenges/webpt/hack-the-bank

in this challenge you are given a site that you are supposed to scan for any vulnerabilities and find the flag.

i started in checking any xss weakness as well as SQL injection by both manually checking and using automatic tools like SQLMap and xss scanners from github but didn't find anything
then i added in the URL of the site /admin (http://18.216.168.212:50102/admin) and found that the admin panel login is not restricted and is using a service called Feng Office (https://www.fengoffice.com/web/) 
after that with the help of my teacher iv'e used an existing exploit to upload a shell to the site using the existing upload files feature of the site - https://www.exploit-db.com/exploits/35041 
then i excuted the exploit the shell in pycharm while changing the parameters to the site in question and was able to navigate to the /home directory and read flag.txt
