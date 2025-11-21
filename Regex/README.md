
## ✅ **REGEX — Interview Preparation (Short Written Exam Focus)**

---

## 🔹 **1. What is Regex? (Short Written Answer)**  
Regex (Regular Expression) is a pattern-matching syntax used to search, validate, extract, or replace text based on rules (patterns). It is widely used in input validation, parsing, data cleaning, and text processing.

---

## 🔹 **2. Important Regex Concepts (Exam-friendly)**
| Concept | Meaning |
|--------|---------|
| **Literal characters** | Exact match (e.g., `abc`) |
| **Meta characters** | Special meaning symbols (`. ^ $ * + ? | () [] {}`) |
| **Character classes** | Match any one of a set of characters (`[abc]`, `\d`, `\w`) |
| **Quantifiers** | How many times something repeats (`*`, `+`, `?`, `{m,n}`) |
| **Anchors** | Position-based match (`^`, `$`, `\b`) |
| **Groups & Capturing** | Parentheses used to group or capture parts of a match |
| **Alternation** | OR operator (`|`) |

---

## 🔹 **3. Common Meta-characters (Short definitions)**

| Meta | Meaning |
|------|---------|
| `.` | Matches any single character except newline |
| `^` | Start of string |
| `$` | End of string |
| `\d` | Digit `[0-9]` |
| `\w` | Word char `[A-Za-z0-9_]` |
| `\s` | Whitespace |
| `\D` | Not a digit |
| `\W` | Not a word |
| `*` | 0 or more |
| `+` | 1 or more |
| `?` | 0 or 1 (optional) |
| `{m,n}` | Between m and n repetitions |

---

## 🔹 **4. Must-Know Practical Regex Patterns (For Interviews)**

### ✔ Validate Email  
```
^[\w.-]+@[\w.-]+\.\w{2,}$
```

### ✔ Validate Strong Password  
```
^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[@$!%*?&]).{8,}$
```

### ✔ Validate Phone Number  
```
^\+?[0-9]{10,14}$
```

### ✔ Extract only numbers  
```
\d+
```

### ✔ Match only alphabets  
```
^[A-Za-z]+$
```

---

## 🔹 **5. Short Written Questions (with Answers)**

#### **Q1: What is the difference between greedy and lazy quantifiers?**  
**Answer:**  
- **Greedy quantifiers** (`*`, `+`) match **as much as possible**.  
- **Lazy quantifiers** (`*?`, `+?`) match **as little as possible**.

---

#### **Q2: What does `^` and `$` mean in Regex?**  
**Answer:**  
- `^` = Start of string  
- `$` = End of string  

Used to ensure full-string validation.

---

#### **Q3: What is a capturing group?**  
**Answer:**  
A capturing group `( )` stores the matched substring so you can reuse it, extract it, or reference it later.

---

#### **Q4: What is a character class?**  
**Answer:**  
A set of allowed characters inside brackets, e.g. `[abc]` or shorthand like `\d`, `\w`.

---

#### **Q5: What is alternation in Regex?**  
**Answer:**  
Alternation (`|`) defines logical OR.  
Example:  
```
(cat|dog)
```

---

## 🔹 **6. Tricky Interview Questions**

#### **Q1: Write a regex to match a string that starts with “abc” and ends with a digit.**  
```
^abc.*\d$
```

---

#### **Q2: Match an IP address (simplified).**  
```
^(\d{1,3}\.){3}\d{1,3}$
```

---

#### **Q3: Remove all whitespace from a string — which regex would you use?**  
```
\s+
```

---

#### **Q4: Match a date in `YYYY-MM-DD` format.**  
```
^\d{4}-\d{2}-\d{2}$
```

---

#### **Q5: Match a string that contains only hexadecimal values.**  
```
^[0-9A-Fa-f]+$
```

---

## 🔹 **7. Real Exam-Style Written Questions (With Answers)**

#### **Q1: Write a regex to allow only alphanumeric characters and underscore, 5–20 length.**
**Answer:**  
```
^\w{5,20}$
```

---

#### **Q2: Write a regex to validate a URL.**
**Answer (simplified):**
```
^https?:\/\/[\w.-]+\.\w{2,}.*$
```

---

#### **Q3: Which regex would you use to split a sentence by multiple spaces?**
**Answer:**  
```
\s+
```

---

#### **Q4: How to match a string that does *not* contain digits?**
**Answer:**  
```
^[^\d]+$
```

---

#### **Q5: Write a regex to capture first and last name separately.**
**Answer:**  
```
^(\w+)\s+(\w+)$
```

---

## 🔹 **8. Scenario-Based Questions (High-level Interview)**

#### **Q1: You want to validate input in a REST API for username. Which regex do you choose?**  
Rules: letters, numbers, underscore, length 3–15.  
```
^[A-Za-z0-9_]{3,15}$
```

---

#### **Q2: In an LMS system, you want to extract course code “CSE101” from a string.**  
```
CSE\d+
```

---

#### **Q3: Allow only `.pdf` or `.docx` file names.**  
```
^.+\.(pdf|docx)$
```

---

## 🔹 **9. Regex Cheat Sheet (Write this in 30 sec in exam)**

```
\d → digit  
\w → word char  
\s → whitespace  
. → any char  
^ → start  
$ → end  
[a-z] → char set  
[^a-z] → negated set  
* → 0+  
+ → 1+  
? → 0/1  
{m,n} → range  
() → group  
| → OR  
\b → word boundary
```

---

# ✅ **Practical Regex Coding Questions (With Answers)**

---

## 🔹 **1. Extract all numbers from a string**
### **Question**  
Given:  
```
"Order ID: 451, Amount: 1200, Discount: 15%"
```
Write a regex to extract all numbers.

### **Answer**
```
\d+
```

---

## 🔹 **2. Validate a password (8+ chars, upper, lower, digit, special char)**
### **Question**  
Your API requires strong passwords. Write a regex.

### **Answer**
```
^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[@$!%*?&]).{8,}$
```

---

## 🔹 **3. Extract email addresses from a paragraph**
### **Question**  
Given a large text, extract all emails.

### **Answer**
```
[\w.-]+@[\w.-]+\.\w{2,}
```

---

## 🔹 **4. Validate IPv4 address**
### **Question**  
Write a regex to validate any IPv4:

### **Answer**  
(Simplified)
```
^(\d{1,3}\.){3}\d{1,3}$
```

---

## 🔹 **5. Match only Bangladeshi phone numbers (with or without +88)**
Examples that should match:  
`+8801712345678`, `01712345678`

### **Answer**
```
^(\+?88)?01[3-9]\d{8}$
```

---

## 🔹 **6. Extract all hashtags from a text**
### **Question**  
Input:
```
Learning #CSharp and #DotNet is fun!
```

### **Answer**
```
#\w+
```

---

## 🔹 **7. Check if a string contains only alphabets**
### **Answer**
```
^[A-Za-z]+$
```

---

## 🔹 **8. Extract domain names from URLs**
### **Question**  
From:
```
https://www.google.com/search
https://chat.openai.com
```
Extract domain only.

### **Answer**
```
https?:\/\/([^\/]+)
```

Captured group 1 → domain.

---

## 🔹 **9. Split a string on commas or semicolons**
### **Question**  
Split:
```
"apple,banana;orange,mango;grapes"
```

### **Answer**
```
[,;]
```

---

## 🔹 **10. Extract the file extension**
### **Question**  
File names:
```
document.pdf
report.docx
image.jpeg
```

### **Answer**
```
\.(\w+)$
```

Captured group 1 → extension

---

## 🔹 **11. Validate username (3–15 chars, letters/numbers/underscore)**
### **Answer**
```
^\w{3,15}$
```

---

## 🔹 **12. Extract currency values**
Input:
```
$120, €500, BDT 3000
```

### **Answer**
```
([$€]|BDT)\s?\d+
```

---

## 🔹 **13. Remove all whitespace**
### **Answer**
```
\s+
```

---

## 🔹 **14. Validate date YYYY-MM-DD**
### **Answer**
```
^\d{4}-\d{2}-\d{2}$
```

---

## 🔹 **15. Extract HTML tag names**
Input:
```
<div>Hello</div><span>World</span>
```

### **Answer**
```
<(\w+)
```

Captured → `div`, `span`

---

## 🔹 **16. Extract course code like CSE101 from text**
### **Answer**
```
CSE\d+
```

---

## 🔹 **17. Check if string starts with “admin”**
### **Answer**
```
^admin
```

---

# 🔹 **18. Validate BD NID (10 or 17 digits)**
### **Answer**
```
^\d{10}(\d{7})?$
```

---

## 🔹 **19. Extract words starting with capital letter**
Example: "John lives in Dhaka Bangladesh".

### **Answer**
```
\b[A-Z][a-zA-Z]*\b
```

---

## 🔹 **20. Extract everything inside parentheses**
Example: `"User(name)"`

### **Answer**
```
\((.*?)\)
```

---
