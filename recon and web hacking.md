Nmap, short for "Network Mapper," is a powerful open-source tool used for network recon and security auditing.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/ff0bd218-6a4f-4b1e-bab3-dea3f15d69dd)


Let's try to make a scan on a win11 machine for open ports.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/e2846daa-bdda-44fa-b667-2622e38b16ba)

What we found:

Port 135
Port 139
Port 445
Port 3389

We also found SSL Certificate Information, and some System Information.

Let's try now for windows server 2016.
We got now an open 80 port for an IIS server.
![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/e55e5a77-b56d-4d19-b8eb-2c07270b7096)

We can also use tools like netcat (nc) to check if the port is open
![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/af7bda9e-8cc7-48f5-a23a-b5e8b57e5046)


In this example:

    -z tells nc to scan without sending any data.
    -v enables verbose mode to get detailed output.
    172.31.47.223 is the target IP address.
    80 is the port to check.

Let's try to get more information with telnet
I typed in : telnet 172.31.47.223 80
then GET / HTTP/1.0 and i pressed enter twice.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/3d275db0-f0a7-4cd9-90fb-e94476df0e2f)


How to search for load balancers:
We found a couple.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/fe040327-60ff-422a-b68d-d8b8b249fcd3)


Going back to our IIS windows machine i'll try a dirb on it to find directories inside the website.

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/6e39ffae-7471-4cf9-a2a2-a6ef40b97093)

And found one called secret.
So this is an example of directory scanning.
![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/ce4b9d03-b7bf-4780-b1d1-0da95d36137e)

Now i'll attempt a Denial of Service on the port 80 using hping3. (the ip of the attacking machine is 172.31.43.83)

I used this command:
hping3 -S 172.31.47.223 -p 80 --flood

![imagem](https://github.com/DanielP33/ethical-hacking/assets/145346859/81602ae0-14d7-4add-af60-541e41ca268a)




