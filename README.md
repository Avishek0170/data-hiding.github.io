# data-hiding.github.io
import cv2
import os
import string

 

img = cv2.imread("naruto.jpg") # Replace with the correct image path

 

msg = input("Enter secret message:")
password = input("Enter a passcode:")

 

d = {}
c = {}

 

for i in range(255):
    d[chr(i)] = i
    c[i] = chr(i)

 

m = 0
n = 0
z = 0

 

for i in range(len(msg)):
    img[n, m, z] = d[msg[i]]
    n = n + 1
    m = m + 1
    z = (z + 1) % 3

 

cv2.imwrite("encryptedImage.jpg", img)
os.system("start encryptedImage.jpg")  # Use 'start' to open the image on Windows

 

message = ""
n = 0
m = 0
z = 0

 

pas = input("Enter passcode for Decryption")
if password == pas:
    for i in range(len(msg)):
        message = message + c[img[n, m, z]]
        n = n + 1
        m = m + 1
        z = (z + 1) % 3
    print("Decryption message:", message)
else:
    print("YOU ARE NOT auth")





    Steganography is the practice of concealing one piece of information within another to hide the existence of the embedded content. Unlike cryptography, which focuses on keeping the content secret, steganography is concerned with keeping the existence of the message or data secret. The term is derived from the Greek words "steganos," meaning covered or hidden, and "graphie," meaning writing. Steganography has various applications, including covert communication, digital watermarking, copyright protection, and tamper detection. However, it can also be misused for malicious purposes, such as hiding malware or unauthorized data transmission. The detection of steganography often involves sophisticated analysis and statistical methods to identify deviations from the expected patterns in digital files.


Modelling of a steganography project uses many steps for making it a success. Steganography is done using python programming language, image encryption and decryption is done in this process. Get a image and write a secret message inside a text with the help of a password so than only 1:1 end users can have the message. There is a change done in the less dominating key so the Blackhat hackers don’t recognize a huge change. There are so many libraries used for this project but we used CV2(pip install cv2). Functions like config(), showinfo(), lable() are used and instantly destroying a message after one wrong password uses destroy() function. This code has no hiding capacity and is highly secured, it can be used now a days as a data hiding process.
![image](https://github.com/Avishek0170/data-hiding.github.io/assets/142254745/13a44868-344b-4974-bc98-1970d07c6acf)

![image](https://github.com/Avishek0170/data-hiding.github.io/assets/142254745/6a578e3e-020c-4791-8d0f-5abac76fefd5)


