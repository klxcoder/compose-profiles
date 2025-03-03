# https://docs.docker.com/compose/how-tos/profiles/

```bash
(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose up -d        
[+] Running 3/3
 ✔ Network compose-profiles_default      Created          0.1s 
 ✔ Container compose-profiles-backend-1  Started          0.4s 
 ✔ Container compose-profiles-db-1       Started          0.4s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose down 
[+] Running 3/3
 ✔ Container compose-profiles-backend-1  Removed          0.0s 
 ✔ Container compose-profiles-db-1       Removed          0.0s 
 ✔ Network compose-profiles_default      Removed          0.4s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose --profile frontend up -d
[+] Running 8/8
 ✔ frontend Pulled                                       17.6s 
   ✔ 7cf63256a31a Already exists                          0.0s 
   ✔ bf9acace214a Pull complete                          12.0s 
   ✔ 513c3649bb14 Pull complete                          12.0s 
   ✔ d014f92d532d Pull complete                          12.0s 
   ✔ 9dd21ad5a4a6 Pull complete                          12.1s 
   ✔ 943ea0f0c2e4 Pull complete                          12.1s 
   ✔ 103f50cb3e9f Pull complete                          12.1s 
[+] Running 4/4
 ✔ Network compose-profiles_default       Created         0.1s 
 ✔ Container compose-profiles-frontend-1  Started         0.4s 
 ✔ Container compose-profiles-backend-1   Started         0.4s 
 ✔ Container compose-profiles-db-1        Started         0.4s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose down                    
[+] Running 3/3
 ✔ Container compose-profiles-db-1       Removed                     0.0s 
 ✔ Container compose-profiles-backend-1  Removed                     0.0s 
 ! Network compose-profiles_default      Resource is still in use    0.0s

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose down
[+] Running 1/1
 ! Network compose-profiles_default  Resource is still in use        0.0s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose --profile frontend down
[+] Running 2/2
 ✔ Container compose-profiles-frontend-1  Removed          0.3s 
 ✔ Network compose-profiles_default       Removed          0.3s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose --profile debug up -d
[+] Running 4/4
 ✔ Network compose-profiles_default         Created                  0.1s 
 ✔ Container compose-profiles-backend-1     Started                  0.3s 
 ✔ Container compose-profiles-db-1          Started                  0.3s 
 ✔ Container compose-profiles-phpmyadmin-1  Started                  0.5s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$ docker compose --profile debug down 
[+] Running 4/4
 ✔ Container compose-profiles-backend-1     Removed                  0.0s 
 ✔ Container compose-profiles-phpmyadmin-1  Removed                  1.2s 
 ✔ Container compose-profiles-db-1          Removed                  0.0s 
 ✔ Network compose-profiles_default         Removed                  0.5s 

(base) ┌──(klx㉿kali)-[~/compose-profiles]
└─$
```
