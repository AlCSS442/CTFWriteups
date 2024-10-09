# Verify
#### Category:
Forensics
#### Challenge file:
challenge.zip

### Description
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.
### Notes:
The challenge provides the checksum of the file, as well as a decrypt script. <br>
Checksum: 3ad37ed6c5ab81d31e4c94ae611e0adf2e9e3e6bee55804ebc7f386283e366a4
### Steps
1. **Accessing Pico's server through SSH**
   <br>
   I found Pico's webshell terminal to be a bit unstable, so I opted to use VisualStudioCode's terminal to connect via SSH.
   ![image](https://github.com/user-attachments/assets/71c58186-2632-4b7a-874d-749d98d2ba63)
   <br>
   
   I use the **ls command** to see what is included in the challenge:
   <br>
   
   ![image](https://github.com/user-attachments/assets/382c1671-0004-4a26-a22b-b356d537bd8b)

3. The challenge already gave us the checksum of the file, but just to verify I open the **checksum.txt**.
   <br>
   ![image](https://github.com/user-attachments/assets/5fc35f3d-c899-4261-a511-a2ce5c2ddb31)
   <br>
   This is the sha256 hash of the targeted file.
   <br>
   
4. Now that I have the sha256 hash of the target file, I just have to check the files in **files** directory to see which file has the correspondng hash. For this, I will need to use the command:
   <br>
   ![image](https://github.com/user-attachments/assets/a50c5b54-e14b-424d-82f5-dae9935d1bcf)
   <br>
   You will get this output:
   <br>
   ![image](https://github.com/user-attachments/assets/d985d610-dc06-4e5d-9206-2c365c3e7c35)
   <br>
5. Now to parse through this information and see which file matches the given checksum, I used the **grep** command:
   <br>
   ![image](https://github.com/user-attachments/assets/01561950-5314-4449-81a4-2664451a27d9)
   <br>
6. I now have the correct file. I run this command to see some information about the targeted file:
   <br> 
   ![image](https://github.com/user-attachments/assets/656cd45a-acab-4a9a-8950-02a3a8cf6a86)
   <br>
7. The challenge provides me with a decrypt script. I run it on the file:
   <br>
   ![image](https://github.com/user-attachments/assets/d47c8812-25f2-4ac8-9f39-321d8410d05a)
   <br>
   **Flag secured!**


   



   
