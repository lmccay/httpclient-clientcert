# httpclient-clientcert

Use keytool to export a PKCS#12 file form the gateway.jks keystore:

keytool -importkeystore -srckeystore /usr/hdp/current/knox-server/data/security/keystores/gateway.jks -destkeystore /usr/hdp/current/knox-server/data/security/keystores/gateway.p12 -srcstoretype JKS -deststoretype PKCS12 -deststorepass knoxsecret -destkeypass knoxsecret -srcalias gateway-identity -destalias gateway-identity

1. clone this project into the {GATEWAY_HOME} directory
2. change the URL, the keystore password and keystore location (if necessary)
3. mvn clean install
