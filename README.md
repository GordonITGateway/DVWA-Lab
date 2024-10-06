# DVWA Lab for CySA+

## Goal:
Deepening my understanding of web vulnerabilities and common attack vectors by seeing these attacks in action. This should allow me to better defend against them in the future and help me on the CySA+ exam.
## Skills:
### Testing and observing a variety of simplified attacks such as:
- SQL Injections
- File Inclusion
## Tools Used:
- Kali Linux
- DVWA (Damn Vulnerable Web Application)
## Screenshots:
### Starting off with a quick demo of improper error handling on a website:
### _1. DVWA example of a website that takes an input_
![Error_handling_1](https://github.com/user-attachments/assets/953612f5-a519-4f4f-902d-6b5c67721294)

### _2. What if I attempt a simple SQL injection?_
![Error_handling_2](https://github.com/user-attachments/assets/a0d60658-03fb-461c-8b68-79e5d1236c38)

### _3. An error! But wait, why are you showing this to the user? Now I know where I went wrong or at least the fact that this runs MariaDB_ 🤔
![Error_handling_3](https://github.com/user-attachments/assets/059a5502-5999-4a58-829e-6b7c2ffddb00)

### Next let's see what happens when we don't sanitize inputs in the URL:
### _1. DVWA website which serves a webpage based on a file_
![File_inclusion_1](https://github.com/user-attachments/assets/8ea64ae1-4ba8-4156-b721-705e786f9988)

### _2. I can modify that URL to attempt to point it towards an internal file, like /etc/passwd for example_
![File_inclusion_2](https://github.com/user-attachments/assets/991d826a-1f36-4aad-97e5-b4a8f7b20ce6)
