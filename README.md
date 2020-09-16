
# Starting CTFd
The following lists the steps required to get the CTFd platform running with all challanges

## 1. Setup the CTFd platform
Follow the steps listed in the CTFd documentation to deploy CTFd

I recommend following the Docker method for a quick and easy deployment method
> https://docs.ctfd.io/docs/deployment/
>
>**Note:**
>
>`sudo` permissions might be neded to run `docker-compose up`

## 2. Navigate to the CTFd website
This should be located at `localhost:8000` if setup using docker
## 3. Complete the CTFd setup process
The information entered here is not important as it will be replaced when importing the configuration
## 4. Import and restore CTFd configuration
- Extract `[Encrypted] CTFd backup.zip` under `CTFd platform`. (Same password as admin account in CTFd)
- Navigate to `Admin Panel` --> `Config` --> `Backup` --> `Import`
- Upload the backup file `CTFd backup.zip` located inside `[Encrypted] CTFd backup.zip` and import

## 5. CTF platform is now up and running
The login credentials for the admin account can be located in `credentials.zip`

# Extracting zip folders
To prevent this repository from being abused, the challenge folders have been encrypted with its relevant flags. This is to ensure that only users who have successfully completed the challenges can access the writeups.
> The zip files have been ecrypted with AES-256 which is not supported by the default Windows extraction tool. I recommend using 7zip to extract the files.

# Project Structure
```
Cryptography\                                   # Cryptography challenges
    |--Double Trouble\
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup
    
    |--Fight xor Flight\  
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup      
    
    |--Jumping Through Loops\
        |--challenge.txt                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup      
    
    |--Rotting Minds\        
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup  

CTFd platform\                                  # Files for CTFd platform
    |--[docker image] csf_jeopardy_ctfd.tar     # Docker image for ctfd
    |--cover.jpg                                # CTFd cover image
    |--CTFd backup.zip                          # CTFd configuration backup
    |--index.html                               # CTFd cover page

Digital Forensics\                              # Digital Forensics challenges
    |--Too easy\
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup
    
    |--Now you see me\  
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup      
    
    |--Down the rabbit hole\
        |--rabbit.jpg                           # Challenge image
        |--Writeup.md                           # Writeup      
    
    |--Another loss\        
        |--challenge\                           # Challenge folder
            |--.secret\
                |--.password.txt                # Password file
                |--secret.txt                   # Misdirection file
            |--challenge.pdf                    # Challenge file
        |--challenge.zip                        # Compressed challenge folder for distribution
        |--Writeup.md                           # Writeup 

Miscellaneous\
    |--Fish out of water\
        |--challenge.txt                        # Challenge file
        |--Writeup.md                           # Writeup
    
    |--Git Good\
        |--.git\                                # Git folder
        |--challenge.zip                        # Compressed challenge folder for distribution
        |--flag.txt                             # Challenge file
        |--Writeup.md                           # Writeup      
    
    |--Giveaway\
        |--challenge.exe                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--Writeup.md                           # Writeup      
    
    |--Reverse Bit Flip\        
        |--challenge.txt                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup

Programming\
    |--Spot the difference\
        |--challenge1.txt                        # Challenge file 1
        |--challenge2.txt                        # Challenge file 2
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup
    
    |--Numbers numbers numbers\
        |--challenge.txt                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup   
    
    |--Monday blues\
        |--challenge.txt                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup       
    
    |--Don't mess with me\        
        |--challenge.txt                        # Challenge file
        |--create_challenge.py                  # Challenge creation script
        |--solution.py                          # Solution script
        |--Writeup.md                           # Writeup

Web\
    |--Pay the postman\
        |--Writeup.md                           # Writeup
    
    |--Robot takeover\
        |--Writeup.md                           # Writeup

    |--Watch your head\
        |--Writeup.md                           # Writeup     
```