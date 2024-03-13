# LSB-Steganography
My Project in C Language is to Encrypt and Decrypt a Secret Message File into a Bitmap Image File.

# What is Steganography?
Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information. Many different carrier file formats can be used, but digital images are the most popular because of their frequency on the internet. For hiding secret information in images, there exists a large variety of steganography techniques some are more complex than others and all of them have respective strong and weak points.

Steganography is the practice of hiding private or sensitive information within something that appears to be nothing out to the usual. Steganography is often confused with cryptography, because the two are similar in the way that they both are used to protect important information. The difference between two is that steganography involves hiding information so it appears that no information is hidden at all. If a person or persons views the object that the information is hidden inside of he or she will have no idea that there is any hidden information, therefore the person will not attempt to decrypt the information.

# Requirements for Project
• The application accept an image file say .bmp along with the a text file which contains the message to be steged

• Analyze the size of the message file and the data part of the .bmp file to check whether the message could fit in the provided .bmp image

• Provide a option to steg a magic string which could be useful to identify whether the image is steged or not

• The application should provide a option to decrypt the file

• This has to be an command line application and all the options has to be passed as an command line argument

# Compilation & Run the Project
Before going to compilation we have to know some essential part of the project. In this project using files are beautiful.bmp, common.h, decode.c, encode.c, encode.h, main_test_encode_decode.c, secret.txt, types.h, '.bmp' is the image file, '.txt' is the text file which is contained a secret message, '.h' are the header file and '.c' are the source file. Header files are used for function and variable declarations and Source files are used for function and variable definitions. Here we are using multiple files for the project so, we are compiling all C files at a time. For this reason, only all necessary files have to keep in the same directory.

For compile-> gcc *.c

For Encrypting Step1-> ./a.out -e beautiful.bmp secret.txt

The above encoding process will generate an additional image file in the same project directory namely "stego_img.bmp" which is the default output filename. We can provide our own output filename by giving the 4th argument as shown below: (Note that, this filename must be having ".bmp" format, otherwise an error message will be shown)

For Encrypting Step2-> ./a.out -e beautiful.bmp secret.txt my_stegged_img.bmp

If we want to provide more security, we can use a passcode for encrypting operations using -p followed by the passcode.

For Encrypting Step3-> ./a.out -e beautiful.bmp secret.txt my_stegged_img.bmp -p 1234

*Note: The passcode can contain a maximum of 4 "digits". We can't use a passcode like 1$3p

For Decrypting Step1-> ./a.out -d stego_img.bmp

It will decrypt the secret message from the image and store it in a newly created file called "decoded.txt" which is the default decoded filename. This file has the same format as that of the input secret file format.

For Decrypting Step2-> ./a.out -d stego_img.bmp my_decoded_file.txt

If we want to provide our own decoded filename, then we can do so by using 3rd argument as shown above.

*Note: The file format must match with the input secret file format. Otherwise, an error message will show.

For Decrypting Step3-> ./a.out -d stego_img.bmp my_decoded_file.txt -p 1234

If a passcode is used while encrypting, then we have to provide the correct passcode as shown above.

After successfully decrypting the process we can check the decoded text file content. Here the secret file complete messages will be available inside the decoded text file.
