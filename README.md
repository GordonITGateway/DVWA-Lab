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

### Now let's look at some XSS examples, starting with reflected:
### _1. DVWA website which takes an input. Notice how the URL changes again_
![XSS_reflected_1](https://github.com/user-attachments/assets/b77d49b0-99aa-4874-927a-dbde0f4f17cb)

### _2. What if we submitted some scripts into this field?_
![XSS_reflected_2](https://github.com/user-attachments/assets/4810740e-640c-4624-af63-b02f139f3580)

### _3. Looks like the browser executed it! Not only that, it stored the potentially malicious script in the URL. If I sent that URL to another user, it would also run on their machine. That's why this form of XSS is "reflected"_ 😀
![XSS_reflected_3](https://github.com/user-attachments/assets/9e3871de-f47c-4fb6-9e88-606faa8c7d9c)

### Stored XSS:
### _1. DVWA website that simulates a comment section_
![XSS_stored_1](https://github.com/user-attachments/assets/7b7f2d6b-3c96-421b-8177-a0a9dd7d1a7c)

### _2. This time, the script will be stored within the website's database, not just the URL. It is also invisible to regular users in the comment_
![XSS_stored_2](https://github.com/user-attachments/assets/5382f168-97ff-46be-bee3-600fb75bc004)

### _3. We see the same result as before, the lack of input validation means the script will run_
![XSS_stored_3](https://github.com/user-attachments/assets/fa562989-05ce-4c2b-87ee-6e43c6e62e1b)

### _4. But now even if I refresh the page or open a new tab to the same site, it also runs. This means I don't need to send that malicious URL, I simply need to ensure my target visits the site with the comment at some point!_
![XSS_stored_4](https://github.com/user-attachments/assets/6adf492e-fc21-437c-a488-34eb17d9d4e6)


