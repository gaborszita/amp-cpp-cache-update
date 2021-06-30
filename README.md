# amp c++ cache update

This little program generates you a link to update the amp cache. You don't neeed to manually generate an RSA signature, verify signature.

1. Fetching files
Clone the project using "git clone https://github.com/gaborszita/amp-cpp-cache-update"

2. Installing libraries
If you use the gcc compiler install libraries libssl and libssl-devel.

3. Setting private and public keys in the program
Modify the std::string privateKey and the std::string publicKey in the update.c file. Copy the Private Key and Public Key to the correct location in the file, but be sure to add a " before every line and a \n"\ after every line. Great tutorial for adding symbols to before and after every line for Notepad++ [here](https://stackoverflow.com/questions/11003761/notepad-add-to-every-line).

4. Building the program
Build the program with "g++ update.c -o main -lcrypto"

5. Set the path of update directory
Write the path in the updateurl.txt file

6. Getting the link
Run the main program and you will get a link if the key is Authentic.

7. Update the cache
Update the cache on the CDNs you want to support

References:
https://gist.github.com/irbull/08339ddcd5686f509e9826964b17bb59
https://developers.google.com/amp/cache/update-cache

Troubleshooting:
If timestamp is bad check your computers time.
