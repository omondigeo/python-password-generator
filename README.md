import random
import string
length=8 #number of characters in a single password
count=5 #number of passwords to generate

#function to generate password based on length and count

def generate_password(length, count):
    passwords = []
    for i in range(count):
        password = ''.join(random.choice(string.ascii_letters + string.digits + string.punctuation) for _ in range(length))
        passwords.append(password)
    return passwords

passwords = generate_password(8, 5)
print(passwords)
