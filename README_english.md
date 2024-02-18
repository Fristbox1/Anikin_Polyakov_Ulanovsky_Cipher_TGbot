README.md Overview

This Python script is a versatile encryption and decryption Telegram bot that utilizes various cryptographic techniques. It employs libraries such as cryptography and telebot to provide functionalities like Fernet-based encryption, Vigenere cipher, cryptography.hazmat encryption, RSA encryption, and text hashing.
Requirements

    Python 3.x
    Telebot library: To interact with the Telegram Bot API.
    Cryptography library: For implementing cryptographic algorithms.
    datetime library: To manage and display timestamps.
    base64 library: For encoding and decoding data in base64.
    hashlib library: For hashing text using the SHA-256 algorithm.

Bot Commands
1. /encode_fernet

This command initiates the Fernet encryption process. The bot prompts the user to enter the text to be encrypted, generates a Fernet key, encrypts the text, and provides both the encrypted text and the encryption key.
2. /decode_fernet

To decrypt Fernet-encrypted text, the user inputs the Fernet key received during encryption. The bot then decrypts the text using the provided key and displays the original text.
3. /encode_vigenere

This command initiates Vigenere cipher encryption. Users input the text to be encrypted, and then provide a keyword that determines the encryption pattern. The bot displays the encrypted text along with the used keyword.
4. /decode_vigenere

To decrypt Vigenere-encrypted text, users input the encrypted text and the keyword used for encryption. The bot then reveals the original text.
5. /rsa_encrypt

This command employs RSA encryption. Users input the text, and the bot generates RSA key pairs. The encrypted text, along with the public key, is displayed.
6. /rsa_decrypt

To decrypt RSA-encrypted text, users input the ciphertext and the private key. The bot then reveals the original text.
7. /cryptography_hazmat_encode

This command uses the cryptography.hazmat library for encryption. Users input the text, and the bot displays the encrypted text.
8. /cryptography_hazmat_decode

To decrypt text encrypted using cryptography.hazmat, users input the encrypted text, and the bot reveals the original text.
9. /hash_text

Users input the text they want to hash, and the bot displays the SHA-256 hash of the text.
10. /compare_hashes

This command initiates the process of comparing two hashed texts. Users input the first hash, then the text to compare. The bot informs whether the hashes match or not.
11. /help

This command provides a list of available commands along with a brief description of each.
Functions
1. send_welcome(message)

This function sends a welcome message to users, introducing the bot and listing available commands.
2. handle_text(message)

This function handles incoming messages and directs them to the appropriate command functions based on user input.
3. generate_private_key()

This function generates an RSA private key if not already generated and returns it.
4. vigenere_encrypt(plaintext, key)

Encrypts the given plaintext using the Vigenere cipher and the provided key.
5. vigenere_decrypt(ciphertext, key)

Decrypts the given ciphertext using the Vigenere cipher and the provided key.
6. encode_vigenere(message)

Initiates the Vigenere encryption process by prompting the user for input.
7. perform_vigenere_encryption(message, chat_id)

Processes the user input for Vigenere encryption, then prompts for the encryption key.
8. send_vigenere_encrypted_text(message, chat_id, original_text)

Displays the Vigenere-encrypted text along with the used key.
9. decode_vigenere(message)

Initiates the Vigenere decryption process by prompting the user for input.
10. ask_for_vigenere_key(message, chat_id)

Prompts the user for the Vigenere decryption key.
11. perform_vigenere_decryption(message, vigenere_encoded_text, chat_id)

Processes the user input for Vigenere decryption and displays the decrypted text.
12. hash_text(text)

Hashes the given text using the SHA-256 algorithm and returns the hashed value.
13. encrypt_text_cryptography_hazmat(original_text)

Encrypts the given text using the cryptography.hazmat library.
14. decrypt_text_cryptography_hazmat(ciphertext)

Decrypts the given ciphertext using the cryptography.hazmat library.
15. encrypt_message_cryptography_hazmat(message)

Initiates the cryptography.hazmat encryption process by prompting the user for input.
16. perform_encryption_cryptography_hazmat(message, chat_id)

Processes the user input for cryptography.hazmat encryption and displays the encrypted text.
17. decrypt_message_cryptography_hazmat(message)

Initiates the cryptography.hazmat decryption process by prompting the user for input.
18. ask_for_cipher_text_cryptography_hazmat(message, chat_id)

Prompts the user for the cryptography.hazmat decryption key.
19. perform_decryption_cryptography_hazmat(message, ciphertext_text)

Processes the user input for cryptography.hazmat decryption and displays the decrypted text.
20. encrypt_message_fernet(message)

Initiates the Fernet encryption process by prompting the user for input.
21. perform_encryption_fernet(message, chat_id)

Processes the user input for Fernet encryption and displays the encrypted text and key.
22. decrypt_message_fernet(message)

Initiates the Fernet decryption process by prompting the user for the decryption key.
23. generate_rsa_key_pair()

Generates an RSA key pair and returns the private and public keys.
24. rsa_encrypt(plaintext, public_key)

Encrypts the given plaintext using RSA and the provided public key.
25. rsa_decrypt(ciphertext, private_key, encryption_key)

Decrypts the given ciphertext using RSA and the provided private key and encryption key.
26. encrypt_message_rsa(message)

Generates an RSA key pair and initiates the encryption process by prompting the user for input.
27. perform_encryption_rsa(message, public_key)

Processes the user input for RSA encryption and displays the encrypted text and public key.
28. decrypt_message_rsa(message)

Initiates the RSA decryption process by prompting the user for the ciphertext.
29. ask_for_decryption_key_rsa(message, ciphertext)

Prompts the user for the decryption key in RSA decryption.
30. perform_decryption_rsa(message, ciphertext, encryption_key)

Processes the user input for RSA decryption and displays the decrypted text.
31. ask_for_cipher_text_fernet(message, chat_id)

Prompts the user for the Fernet decryption key.
32. perform_decryption_fernet(message, key_text)

Processes the user input for Fernet decryption and displays the decrypted text.
33. hash_text_command(message)

Initiates the text hashing process by prompting the user for input.
34. send_hashed_text(message, chat_id)

Displays the hashed text to the user.
35. compare_hashes_command(message)

Initiates the process of comparing two hashed texts by prompting the user for the first hash.
36. ask_for_comparison_text(message, chat_id)

Prompts the user for the text to compare with the first hash.
37. perform_hash_comparison(message, first_hash_text)

Compares two hashed texts and informs the user whether the hashes match or not.
38. log_error(message)

Logs errors with timestamps to the console.
39. bot.polling()

Starts the bot's polling loop to listen for incoming messages and execute commands.
Usage

    # Install the required libraries:
    bash
    pip install telebot 
    pip install cryptography 
    pip install base64 
    pip install datetime 
    pip installhashlib


Replace the TOKEN variable with your Telegram bot token.

Run the script:

    python your_script_name.py

Interact with the Telegram bot using the provided commands.