## Install DFS 

1. go to server manager
2. click on add role and feature
3. CLICK ON NEXT UNTIL SERVER ROLE
4. click on file and Storage services (2 of 12 installed )
5. click on file and iscsi (1 of 11 Installed )
6. tick on DFS Namespeace
7. Tick on DFS Replication
8. tick on file server resoure managment
9. click on next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/140b19f0-a239-4485-949b-a50986c0320f" />
10. tick on restart the destination server atomaticalli if requied
11. click install
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0e7c9607-55a2-4170-9360-b266653fda21" />
### Same instalation on Server2
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/113dbf73-42c2-420e-813d-8531ec8a16f4" />

### Create Folder In Serve2 And Client 
#### Server2
1. Go to server2
2. click on file explore
3. go to this pc
4. click on local disk c
5. create folder hr1
6. hr1 under create file hr1
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/24e7ce83-3c80-4d64-b435-1cb02c30cfb6" />
7. Right click on hr1 folder
8. click on properties
9. click on Sharing
10. click on Advance sharing
11. Tick on share this folder
12. click on permision
13. evaryone tick on full access
14. click apply
15. click ok

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/515875b3-c87f-4b3b-902b-d3ef85092dc7" />
#### Client
Same configuration on client1
1. create hr2 folder
2. give Full Control permisiion
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/abe55937-cc15-47f5-a171-5cfb0ad0c4af" />


## Configuration
1. Go to Server 1
2. Go to server Manager
3. click on tools
4. click on DFS Manager
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b9d62c65-e41f-47ec-86e0-915ebd964b09" />

5. Right click on Namespaces
6. click on New Namespace
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/45af4d91-f22e-4230-836b-1596b8e04523" />
7. Enter the name of the server that will host the namespace. The server you specify will be known as the namespace server.
8. Type Server : server1
9. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/533f8571-18aa-4ec2-936d-512899dc0b51" />
10. Enter a name for the namespace. This name will appear after the server or domain name in the namespace path, such as \\Server\Name or \\Domain Name
11. Type Name : HR
12. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/adbac635-f151-4927-937a-b3abcce5673b" />
13. choice Domain based namespace
14. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ace27f39-931d-48ee-a8e6-d16e9db054df" />
15. click on create
16. now you see created namespace success
<img width="1919" height="1079" alt="Screenshot 2025-09-30 234047" src="https://github.com/user-attachments/assets/86c6288d-30e0-4337-8c1e-fcada16496a0" />

### Create folder under domain
1. right click on \\microsoft.com\HR
2. click on New Folder
<img width="1919" height="1079" alt="Screenshot 2025-09-30 235728" src="https://github.com/user-attachments/assets/2303091a-079b-45dd-b522-4ac825b127a8" />
3. type name : hr1
4. click on add
5. Add Target Folder
6. path to folder target : \\server2\hr1
7. click ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b2161584-73bb-4ceb-be55-3abfcf0b1af8" />

same for client1
1. right click on \\microsoft.com\HR
2. click on New Folder
<img width="1919" height="1079" alt="Screenshot 2025-09-30 235728" src="https://github.com/user-attachments/assets/2303091a-079b-45dd-b522-4ac825b127a8" />
3. type name : hr2
4. click on add
5. Add Target Folder
6. path to folder target : \\client1\hr2
7. click ok
<img width="1919" height="1079" alt="Screenshot 2025-10-01 001155" src="https://github.com/user-attachments/assets/899ad7e3-65d8-487e-9ad3-a487d2e3d278" />

## Verification
verify server1 , server2 , and client1

1. press window key + r
2. type : \\microsoft.com
3. click ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0389f2fb-f808-45cb-b84a-7a1f6e7e2405" />
4. now you see HR Folder Under hr1 and hr2 folder
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4bb12368-d63a-4b16-8c85-2706104f71a7" />

same verification on server2 and clinet1
