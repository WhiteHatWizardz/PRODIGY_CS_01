# Caesar Cipher Implementation

def encrypt(text, shift):
    result = ""
    
    # Traverse through the given text
    for i in range(len(text)):
        char = text[i]

        # Encrypt uppercase characters
        if char.isupper():
            result += chr((ord(char) + shift - 65) % 26 + 65)

        # Encrypt lowercase characters
        elif char.islower():
            result += chr((ord(char) + shift - 97) % 26 + 97)
        
        # If it's not a letter, just add it to the result without shifting
        else:
            result += char

    return result


def decrypt(text, shift):
    return encrypt(text, -shift)  # Reversing the shift for decryption


if __name__ == "__main__":
    # User input
    print("Caesar Cipher Program")
    choice = input("Do you want to (e)ncrypt or (d)ecrypt?: ").lower()
    message = input("Enter your message: ")
    shift = int(input("Enter the shift value (number): "))

    if choice == 'e':
        print("Encrypted message: ", encrypt(message, shift))
    elif choice == 'd':
        print("Decrypted message: ", decrypt(message, shift))
    else:
        print("Invalid choice. Please enter 'e' for encryption or 'd' for decryption.")
