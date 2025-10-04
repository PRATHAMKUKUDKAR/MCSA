# Install DFS Role 

# step 1 — Install DFS Roles (Server1 and Server2)

**On Server1 (repeat the same steps on Server2):**

1. Log in to **Server1** with an Administrator account.
2. Open **Server Manager**.
3. Click **Add roles and features**.
4. Click **Next** repeatedly until you reach the **Server Roles** page.
5. Expand **File and Storage Services → File and iSCSI Services**.
6. Tick **DFS Namespaces**.
7. Tick **DFS Replication**.
8. (Optionally) Tick **File Server Resource Manager**.
9. Tick **Restart the destination server automatically if required** (if you want automatic reboot).
10. Click **Install** and wait for the installation to complete.

**Screenshot — select roles (example):**  
![Select DFS Roles](https://github.com/user-attachments/assets/140b19f0-a239-4485-949b-a50986c0320f)

**Screenshot — install / reboot option:**  
![Install Complete / Restart Option](https://github.com/user-attachments/assets/0e7c9607-55a2-4170-9360-b266653fda21)

**Repeat same installation on Server2:**  
![Same installation on Server2](https://github.com/user-attachments/assets/113dbf73-42c2-420e-813d-8531ec8a16f4)


## Create Folder And Give sharing Permission And NTFS Permision on Both Server 

### Server1
### Sharing Permision

1. Create folder CompanyData
2. right click on Company Data
3. go to properties
4. click on sharing tab
5. Tick on share this folder
6. click on permision
7. tick on full contol
8. click on apply
9. click on ok
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/77cbc765-d0ae-4309-a6f0-b71c36146928" />

### Security Permission

1. Right click on CompanyData
2. Go to Properties
3. click on security tab
4. click on Edit
5. click on User (MICROSOFT\User)
6. tick on Full Control
7. click on Apply
8. click n ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5850f806-53c3-4235-a441-e156b2203ff4" />

### Server 2
### Sharing Permision

1. Create folder CompanyData
2. right click on Company Data
3. go to properties
4. click on sharing tab
5. Tick on share this folder
6. click on permision
7. tick on full contol
8. click on apply
9. click on ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/82c2e074-50ce-4dc4-be8b-3d354a42b624" />


### Security Permission

1. Right click on CompanyData
2. Go to Properties
3. click on security tab
4. click on Edit
5. click on User (MICROSOFT\User)
6. tick on Full Control
7. click on Apply
8. click n ok

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7f9171fd-ae7d-4847-951d-3f7369b3c75e" />



## Configure DFS Namespace
1. go to server manager
2. click on tools
3. click on DFS Management
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d66732c5-cba4-4784-ae65-1b265819819e" />

4. Right Click On Namespace
5. click on New Namespaces
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/434b3f0e-c71f-4038-bb1f-ff454ced3a26" />

6. Namespace server type `server1`
7. click on next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/64f83386-086e-438c-b1cf-84e7c320026d" />

8. Namespace name type `Company`
9. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c804dd7a-ea45-412c-b1eb-16620d10d990" />

10. Namespace Type
11. Domain Based Namespace
12. click Next
<img width="1902" height="1079" alt="image" src="https://github.com/user-attachments/assets/59421d45-da4d-4f29-bccd-65347a3829e2" />
13. click on crete


## Configure DFS Replication
1. Right click on replication
2. create new replication group
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/42273196-4712-47c1-896c-67199eee1f27" />

3. select Multipurpose Replication Group
4. click Next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/de2743c8-ceb1-4282-9e86-07de87d82b6a" />

5. Name and Domain
6. type name `CompanyDataReplication`
7. click Next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/be0c70f0-4495-462e-8d17-f01dc91d9cff" />

8. Add Member `Server1` And `Server2`
9. click on add
10. type server1
11. click on check name
12. click on ok
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0979ba62-a481-4cdd-9443-a44edb5ac05b" />

13. Now see the servers servr1 and server2
14. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/060d6a22-c860-4534-adea-ac032ad49247" />


15. topology selection
16. select full mash
17. click on next
<img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/caef229a-422e-49e8-9adf-504cf658ef12" />

18. Select Primary Member
19. select Server1
20. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/925a9e36-1b2c-42a1-9b40-8d27e75660b8" />

21. Folder To replace
22. selcet CompanyData Folder
23. click on Next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ad5509db-ac72-4b05-8444-892f7f833dc6" />

24. click on edit
25. click on enable
26. select local path of folder
27. C:\CompanyData
28. click ok
29. click next
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c13f6fd8-23ce-4e28-a49c-519c3543ee8b" />
30. click on create
