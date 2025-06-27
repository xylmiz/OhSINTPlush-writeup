# 📝 TryHackMe Room Write-Up: **TrackDown**

Welcome to the OhSINT++ OSINT Challenge!

This room was designed to teach you how to combine image analysis, metadata extraction, steganography, Morse code decoding, and simple data conversions to trace a suspect’s online footprint.

Below is the full step-by-step solution for each task.

---

## 🌟 Task 1: **What is this person’s Twitter username?**

✅ **Solution:**

- **Step 1:** Download the provided image.
- **Step 2:** Extract the metadata. Use Notepad.
- **Step 3:** Look at the last line at the bottom for needed information.
- **Step 4:** You find an encrypted text in last called base64 encryption.
- **Step 5:** Decrypt the base64 encryption in https://v2.cryptii.com/base64/text
- ✅ **Answer:**
    
    ```
    https://x.com/@xylmiz
    
    ```
    

---

## 🌍 Task 2: **What city does this person live in?**

✅ **Solution:**

- **Step 1:** Inspect the same image in `exiftool` metadata or any other images provided.
- **Step 2:** Look for GPS Latitude and Longitude coordinates.
    
    ```
    51.500897, -0.123027
    ```
    
- **Step 3:** Plug them into Google Maps.
- **Step 4:** The coordinates point to central London.
- ✅ **Answer:**
    
    ```
    London
    
    ```
    

---

## 📶 Task 3: **What is the SSID of the WAP he connected to?**

✅ **Solution:**

- **Step 1:** Visit the suspect’s Twitter profile.
- **Step 2:** Find the tweet with the Morse code:
    
    ```
    .... --- -- . .-- .. ..-. ..
    ```
    
- **Step 3:** Use a Morse translator:
- ✅ **Answer:**
    
    ```
    HOMEWIFI
    ```
    

---

## 📧 Task 4: **What is his personal email address?**

✅ **Solution:**

- **Step 1:** Go to the Twitter and get the GitHub repository URL.
- **Step 2:** Look for a README.md or any text file.
- **Step 3:** The email is included in the contact information.
- ✅ **Answer:**
    
    ```
    xylmiz.challenge@gmail.com
    ```
    

---

## 🌐 Task 5: **What is the login URL of the bank?**

✅ **Solution:**

- **Step 1:** On Twitter, locate the post with a long decimal string:
    
    ```
    104 116 116 112 115 58 47 47 120 121 108 109 105 122 46 103 105 116 104 117 98 46 105 111 47 98 97 110 107 111 102 108 111 110 100 111 110 47
    ```
    
- **Step 2:** Convert each number to ASCII:
- ✅ **Answer:**
    
    ```
    https://xylmiz.github.io/bankoflondon
    ```
    

---

## 🔑 Task 7: **What is the login password?**

✅ **Solution:**

- **Step 1:** Use `file` or `exiftool` to find the image dimensions:
    
    ```
    Image Width: 721
    Image Height: 752
    ```
    
- **Step 2:** Multiply width × height:
    
    ```
    721 × 752 = 542192
    ```
    
- ✅ **Answer:**
    
    ```
    542192
    ```
    

---

## 💰 Task 8: **How much money will I receive back?**

✅ **Solution:**

- **Step 1:** Use the email (`xylmiz.challenge@gmail.com`) and password (`542192`) to log in at:
    
    ```
    https://xylmiz.github.io/bankoflondon/
    ```
    
- **Step 2:** The dashboard displays the recovered funds.
- ✅ **Answer:**
    
    ```
    1,450,670.75
    ```
    

---

## 🏁 Completion

🎉 **Congratulations!**

You successfully tracked down **xylmiz**, uncovered his digital trail, and reclaimed your stolen money.

This challenge shows the power of OSINT: using freely available tools and publicly visible data to reconstruct someone’s activities.
