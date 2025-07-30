# Assignment 5: File Creation and Permission

## Create a file and set specific permissions using numbers (751) 


<img width="1919" height="1024" alt="Screenshot 2025-07-30 101211" src="https://github.com/user-attachments/assets/31276cac-cf72-4e4f-b096-a5310229f4a9" />

The file is created and permission is set using numbers (751)



---

## 📝 Notes: Octal Notation in File Permissions

In Linux, file permissions are controlled using **octal notation**, a shorthand based on the **base-8 number system (0–7)**. This notation makes it easier to represent read (`r`), write (`w`), and execute (`x`) permissions for:

* **Owner**
* **Group**
* **Others**

Each permission has a numeric value:

| Permission | Symbol | Value |
| ---------- | ------ | ----- |
| Read       | `r`    | 4     |
| Write      | `w`    | 2     |
| Execute    | `x`    | 1     |

You add the values to get the octal digit:

| Symbolic | Binary | Octal | Meaning              |
| -------- | ------ | ----- | -------------------- |
| `rwx`    | 111    | 7     | Read, write, execute |
| `rw-`    | 110    | 6     | Read, write          |
| `r-x`    | 101    | 5     | Read, execute        |
| `r--`    | 100    | 4     | Read only            |
| `--x`    | 001    | 1     | Execute only         |

---

### 🔧 Example: `chmod 751 myfile.txt`

This sets permissions as:

| Role   | Octal | Symbolic | Description           |
| ------ | ----- | -------- | --------------------- |
| Owner  | 7     | `rwx`    | Read, write, execute  |
| Group  | 5     | `r-x`    | Read and execute only |
| Others | 1     | `--x`    | Execute only          |

When you run:

```bash
ls -l myfile.txt
```

You’ll see:

```
-rwxr-x--x
```

---

This **octal format** helps administrators manage file access clearly and securely.








