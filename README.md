# Captive-Apple
A captive portal designed for the Hak5 WiFi Pineapple Mark V (other variants may work). The end-user will see a login form prompting for Google account credentials. Once credentials have been supplied, the user will be redirected to Google search, giving the impression that the login attempt was "successful"
## Installation
Place all three files within the root directory specified by the Captive Portal infusion.
## Permissions
By default, the end-user will be able to see the contents of auth.txt. A good security measure would be to restrict read access by changing the group ownership and read/write/execute access via chmod. An Apache 2 server running on an Ubuntu host would issue the following commands:
```
$ chown -R www-data:www-data /path/to/file/directory
$ chmod 233 /path/to/file/directory/auth.txt
```

However, to view the contents of auth.txt, you will need to be root or have superuser privileges via command line. The file will be inaccessible via web browser.
## Disclaimer
I provide this content for security testing purposes only. I am not personally liable for any misuse or illegal activities conducted with the information provided.
