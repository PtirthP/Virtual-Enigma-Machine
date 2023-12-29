# Personalized Enigma Machine and Encryption/Decryption in Go

## Enigma Machine (`enigma.py`)

### Introduction

This GoLang code implements a simplified version of the famous Enigma machine, a historical encryption device used during World War II. The Enigma machine consists of rotors, reflectors, and a set of rules for enciphering and deciphering messages.

### How it works

1. **Rotor Class:**
   - The `Rotor` class represents a rotor in the Enigma machine. Each rotor has a set of mappings that define how each letter is enciphered.
   - You can create a rotor by providing a set of mappings and an optional starting position offset.

2. **Reflector Class:**
   - The `Reflector` class models the reflector component in the Enigma machine. It defines a bijective map representing the reflection of a character.

3. **Machine Class:**
   - The `Machine` class brings together rotors and a reflector to form the complete Enigma machine.
   - Initialize the machine with a list of rotors and a reflector.

4. **Example Usage:**
   - Example rotors and reflector configurations are provided at the end of the code. You can customize these configurations based on your requirements.

```python
# Example Usage
r1 = Rotor("VEADTQRWUFZNLHYPXOGKJIMCSB", 1)
r2 = Rotor("WNYPVJXTOAMQIZKSRFUHGCEDBL", 2)
r3 = Rotor("DJYPKQNOZLMGIHFETRVCBXSWAU", 3)
reflector = Reflector("EJMZALYXVBWFCRQUONTSPIKHGD")
machine = Machine([r1, r2, r3], reflector)
plaintext = "ATTACK AT DAWN"
ciphertext = machine.encipher(plaintext)
decrypted_text = machine.decipher(ciphertext)
```

## Notes

- The code includes detailed comments to help you understand each component and its functionality.
- Feel free to customize rotor and reflector configurations for your specific use case.

## Encryption/Decryption in Go (`PersonalizedEnigmaMachine.go`)

### Introduction

This GoLang code demonstrates various encryption and decryption methods using different ciphers, including AES-ECB, AES-OFB, and ChaCha20. It also includes padding and unpadding functions for secure data transmission.

### How to Use

**User Input:**
- The program prompts the user to enter plaintext.

**Key Generation:**
- Keys and initialization vectors (IVs) are generated for AES-ECB, AES-OFB, and ChaCha20.

**Encryption:**
- The plaintext is encrypted using AES-ECB, AES-OFB, and ChaCha20 sequentially.

**Decryption:**
- The ciphertext is decrypted using ChaCha20, AES-OFB, AES-ECB, and AES-ECB (2nd time) sequentially.

**Output:**
- The program displays the encrypted messages, decrypted messages, and the final unpadded decrypted message.

### Example Usage

```bash
# Example Usage
go run PersonalizedEnigmaMachine.go
```

## Notes

- The code showcases the use of different encryption algorithms in Go.
- Experiment with different plaintext inputs and observe the effects of multiple encryption and decryption steps.
- 🔒 **Note:** This code is for educational purposes. Always use secure and established cryptographic libraries for real-world applications.
