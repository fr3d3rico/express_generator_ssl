# Expressjs Generator + OpenSSL ;)

Example how configure Express Generator app with OpenSSL.

This example use Express site (https://expressjs.com/en/starter/generator.html) and this openssl distribution for windows (https://blog.didierstevens.com/2015/03/30/howto-make-your-own-cert-with-openssl-on-windows/)

## Prerequisites

1 - Install Node.js and update npm (https://docs.npmjs.com/getting-started/installing-node)

2 - Install OpenSSL(https://blog.didierstevens.com/2015/03/30/howto-make-your-own-cert-with-openssl-on-windows/)

3 - Install express-generator (https://expressjs.com/en/starter/generator.html)

4 - Create private.key and certificate.pem with OpenSSL... how?

After configured OpenSSL and created environment variables, execute openssl.exe and then:

$ genrsa -out private.key 4096

$ req -new -x509 -days 1826 -key private.key -out private.crt

and done with(windows command)...

$ type private.crt private.key > certificate.pem

5 - All files generated on step 4 above must be addressed to bin/ directory.

6 - Please, open /bin/www file to learn how config private.key and pem file, and how create https server to respond on 3443 https port.

## Run

Go to root directory and run: npm start

This command will execute www file. If you want change it, please go to package.json and change "scripts" ;)
