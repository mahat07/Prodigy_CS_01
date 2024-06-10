1. **Encryption Function (`encrypt`)**:
   - The `encrypt` function takes two parameters: `text` (the message to be encrypted) and `shift` (the number of positions to shift each character).
   - It initializes an empty string `encrypted_text` to store the encrypted message.
   - It iterates over each character in the input `text`.
   - For each character, it checks if it is an alphabet character using `isalpha()`.
   - If the character is an alphabet:
     - It calculates the shifted value of the character's ASCII code based on the provided `shift`.
     - It handles wrapping around the alphabet boundary (e.g., from 'z' to 'a' or vice versa) by adjusting the shifted value accordingly.
     - It appends the encrypted character (determined by the shifted ASCII value) to the `encrypted_text`.
   - If the character is not an alphabet (e.g., punctuation or space), it appends the character as is to the `encrypted_text`.
   - Finally, it returns the `encrypted_text`.

2. **Decryption Function (`decrypt`)**:
   - The `decrypt` function simply calls the `encrypt` function with the negative value of the `shift`. This is because decryption in the Caesar Cipher is essentially encryption with the inverse shift.

3. **Main Function (`main`)**:
   - The `main` function provides the user interface for interacting with the program.
   - It prompts the user to enter whether they want to encrypt or decrypt (`choice`).
   - Depending on the user's choice ('e' for encryption or 'd' for decryption), it prompts for the message and shift value accordingly.
   - It then calls the appropriate function (`encrypt` or `decrypt`) with the user-provided inputs and prints the result.

4. **Execution**:
   - The `if __name__ == "__main__":` block ensures that the `main` function is only executed if the script is run directly, not if it's imported as a module into another script.
   - When the script is run, it starts by executing the `main` function, which guides the user through the encryption or decryption process.

Overall, this program encapsulates the logic for Caesar Cipher encryption and decryption and provides a simple interface for users to interact with it.
