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
## Modification
It is highly recommended you modify the contents of index.html to suit the needs of your locale. Creating a convincing portal is essential to pulling off the social engineering required to convince end-users to login. You will find two areas in the source code specifically requesting modification:

```
<!-- Rename the Page Title -->
<title>Rename Me</title>
<!-- End Page Title -->
```
Replace the text "Rename Me" to something more suited to your target.

```
<!-- Logo Image -->
<img src="PLACE_LINK_TO_IMAGE_HERE" class="img-responsive center-block">
<!-- End of Logo Image -->
```
Replace "PLACE_LINK_TO_IMAGE_HERE" with the full URL path of a convincing image.

## Disclaimer
I provide this content for security testing purposes only. I am not personally liable for any misuse or illegal activities conducted with the information provided.
