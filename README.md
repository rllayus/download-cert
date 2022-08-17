# download-cert

      $ echo | openssl s_client -servername IP -connect IP:PUERTO |\sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p' >certificate.crt
      
## instalación del certificado en los cacert de java. 
Primero debe dirigirse a la ruta donde está instalado java, en esa ruta debe ingresar a la carpeta bin
      
      cd $JAVA_HOME/bin 
      
Luego debe ejecutar el comando para agregar el certificado      

      keytool -import -alias [ALIAS] -keystore ../../jre/lib/security/cacerts -file /[RUTA_CERTIFICADO]/certificado.crt -storepass changeit
      
