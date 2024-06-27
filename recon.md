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

