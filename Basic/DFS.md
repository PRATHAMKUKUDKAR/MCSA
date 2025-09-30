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
Same configuration on client
1. create hr2 folder
2. give Full Control permisiion
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/abe55937-cc15-47f5-a171-5cfb0ad0c4af" />


## Configuration
1. Go to Server 1
2. Go to server Manager
3. click on tools
4. click on DFS Manager
