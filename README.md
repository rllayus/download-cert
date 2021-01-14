# download-cert

      $ echo | openssl s_client -servername IP -connect IP:PUERTO |\sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p' >certificate.crt
      
