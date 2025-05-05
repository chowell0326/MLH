## Overview

MLH (Multi-Layer Hashing) is a concept that would take a plaintext password and add an additional layer of protection to it using various ciphers. An example of this would be taking the following:

 
### EXAMPLE:

| Plaintext   | Ciphertext (atbash) | Hash (MD5)                       |
| ----------- | ------------------- | -------------------------------- |
| password123 | u9rrnvs6ihg         | b061775d8c3fee412768acb61e24d7bc |

## Benefits 

This layer of obfuscation would enhance the level of security via the following:
- Assuming the hashes are stolen, a higher level of entropy will be needed to crack them opposed to a standard password
- Passwords would no longer have to remain highly complex, as the cipher would significantly increase the level of entropy of the password, as seen with the example above.
- Has little to no overhead when creating/verifying hashes, as ciphers act as a simple one-way encryption.
- Even if password is cracked, another layer of deterrent is added as the password would not be valid as it would still need to be decrypted.

## Additions 

This also can be done with a shared key dependent on what cipher a person would like to use, and it's key. For example, a person would have their password `password123` then their encryption key would be `@A0`, which would indicate an atbash cipher along with the key using capital alphabet and numerals. 

This key would also allow for offset to be added as well, essentially adding an additional salting to the password in question. This would be done by taking some pre-defined information (e.g. username, encryption key, etc.) and using a predetermined algorithm append and prepend additional ASCII characters to the password before encryption using that as an additional layer of entropy.

## Key Takeaway

- Uses additional cipher to act as intermediary for hashing
- Increases Entropy
- Can be implemented with various ciphers and hashes
- Added levels of obfuscation possible via additional salting method

## Addt. Notes

One method I just thought of is using a conjunction of using a diffie-hellman encryption method using a public key of a user's retinal scan/iris color (human unique) to first generate a cipher key, then encrypt the passwords in that manner.

### Simplified Paragraph (for citations)

MLH (Multi-Layer Hashing) is a concept that would take a plaintext password and add an additional layer of protection to it using various ciphers. An example of this would be taking the following: make a password, let it be ‘password123’, then this plaintext would use a known cipher suite like atbash ciphers to put it into a ciphertext ‘u9rrnvs6ihg’, and from there could use any standard implementation encryption standard like MD5 to hash it as usual. Some of the benefits of this include the following: Assuming the hashes are stolen, a higher level of entropy will be needed to crack them opposed to a standard password, passwords would no longer have to remain highly complex, as the cipher would significantly increase the level of entropy of the password, as seen with the example above, has little to no overhead when creating/verifying hashes, as ciphers act as a simple one-way encryption, even if password is cracked, another layer of deterrent is added as the password would not be valid as it would still need to be decrypted, and this system makes the hashes quantum resistant, as standard brute force attacks will not work on this specific form of encryption.
