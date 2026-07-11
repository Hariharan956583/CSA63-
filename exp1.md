def encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():  
        
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char  
    return result

def decrypt(text, shift):
    return encrypt(text, -shift)

plaintext = "ATTACKATDWAN"
shift = 3  

ciphertext = encrypt(plaintext, shift)
decrypted_text = decrypt(ciphertext, shift)

print("Plaintext:", plaintext)
print("Ciphertext:", ciphertext)
print("Decrypted:", decrypted_text)
<img width="887" height="837" alt="WhatsApp Image 2026-07-11 at 2 08 51 PM" src="https://github.com/user-attachments/assets/15c7bf3b-a3fc-4520-824b-1cc4d0407739" />
