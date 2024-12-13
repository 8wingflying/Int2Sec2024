# openssl_commands
- 檢視指令參數 ==> openssl --help
```
openssl --help
help:

Standard commands
asn1parse         ca                ciphers           cmp               
cms               crl               crl2pkcs7         dgst              
dhparam           dsa               dsaparam          ec                
ecparam           enc               engine            errstr            
fipsinstall       gendsa            genpkey           genrsa            
help              info              kdf               list              
mac               nseq              ocsp              passwd            
pkcs12            pkcs7             pkcs8             pkey              
pkeyparam         pkeyutl           prime             rand              
rehash            req               rsa               rsautl            
s_client          s_server          s_time            sess_id           
smime             speed             spkac             srp               
storeutl          ts                verify            version           
x509              

Message Digest commands (see the `dgst' command for more details)
blake2b512        blake2s256        md4               md5               
rmd160            sha1              sha224            sha256            
sha3-224          sha3-256          sha3-384          sha3-512          
sha384            sha512            sha512-224        sha512-256        
shake128          shake256          sm3               

Cipher commands (see the `enc' command for more details)
aes-128-cbc       aes-128-ecb       aes-192-cbc       aes-192-ecb       
aes-256-cbc       aes-256-ecb       aria-128-cbc      aria-128-cfb      
aria-128-cfb1     aria-128-cfb8     aria-128-ctr      aria-128-ecb      
aria-128-ofb      aria-192-cbc      aria-192-cfb      aria-192-cfb1     
aria-192-cfb8     aria-192-ctr      aria-192-ecb      aria-192-ofb      
aria-256-cbc      aria-256-cfb      aria-256-cfb1     aria-256-cfb8     
aria-256-ctr      aria-256-ecb      aria-256-ofb      base64            
bf                bf-cbc            bf-cfb            bf-ecb            
bf-ofb            camellia-128-cbc  camellia-128-ecb  camellia-192-cbc  
camellia-192-ecb  camellia-256-cbc  camellia-256-ecb  cast              
cast-cbc          cast5-cbc         cast5-cfb         cast5-ecb         
cast5-ofb         des               des-cbc           des-cfb           
des-ecb           des-ede           des-ede-cbc       des-ede-cfb       
des-ede-ofb       des-ede3          des-ede3-cbc      des-ede3-cfb      
des-ede3-ofb      des-ofb           des3              desx              
rc2               rc2-40-cbc        rc2-64-cbc        rc2-cbc           
rc2-cfb           rc2-ecb           rc2-ofb           rc4               
rc4-40            seed              seed-cbc          seed-cfb          
seed-ecb          seed-ofb          sm4-cbc           sm4-cfb           
sm4-ctr           sm4-ecb           sm4-ofb           
```

```
openssl ca --help
Usage: ca [options] [certreq...]

General options:
 -help                   Display this summary
 -verbose                Verbose output during processing
 -outdir dir             Where to put output cert
 -in infile              The input cert request(s)
 -inform PEM|DER         CSR input format (DER or PEM); default PEM
 -infiles                The last argument, requests to process
 -out outfile            Where to put the output file(s)
 -dateopt val            Datetime format used for printing. (rfc_822/iso_8601). Default is rfc_822.
 -notext                 Do not print the generated certificate
 -batch                  Don't ask questions
 -msie_hack              msie modifications to handle all Universal Strings
 -ss_cert infile         File contains a self signed cert to sign
 -spkac infile           File contains DN and signed public key and challenge
 -engine val             Use engine, possibly a hardware device

Configuration options:
 -config val             A config file
 -name val               The particular CA definition to use
 -section val            An alias for -name
 -policy val             The CA 'policy' to support

Certificate options:
 -subj val               Use arg instead of request's subject
 -utf8                   Input characters are UTF8; default ASCII
 -create_serial          If reading serial fails, create a new random serial
 -rand_serial            Always create a random serial; do not store it
 -multivalue-rdn         Deprecated; multi-valued RDNs support is always on.
 -startdate val          Cert notBefore, YYMMDDHHMMSSZ
 -enddate val            YYMMDDHHMMSSZ cert notAfter (overrides -days)
 -days +int              Number of days to certify the cert for
 -extensions val         Extension section (override value in config file)
 -extfile infile         Configuration file with X509v3 extensions to add
 -preserveDN             Don't re-order the DN
 -noemailDN              Don't add the EMAIL field to the DN

Signing options:
 -md val                 Digest to use, such as sha256
 -keyfile val            The CA private key
 -keyform format         Private key file format (ENGINE, other values ignored)
 -passin val             Key and cert input file pass phrase source
 -key val                Key to decrypt the private key or cert files if encrypted. Better use -passin
 -cert infile            The CA cert
 -certform PEM|DER       Certificate input format (DER/PEM/P12); has no effect
 -selfsign               Sign a cert with the key associated with it
 -sigopt val             Signature parameter in n:v form
 -vfyopt val             Verification parameter in n:v form

Revocation options:
 -gencrl                 Generate a new CRL
 -valid val              Add a Valid(not-revoked) DB entry about a cert (given in file)
 -status val             Shows cert status given the serial number
 -updatedb               Updates db for expired cert
 -crlexts val            CRL extension section (override value in config file)
 -crl_reason val         revocation reason
 -crl_hold val           the hold instruction, an OID. Sets revocation reason to certificateHold
 -crl_compromise val     sets compromise time to val and the revocation reason to keyCompromise
 -crl_CA_compromise val  sets compromise time to val and the revocation reason to CACompromise
 -crl_lastupdate val     Sets the CRL lastUpdate time to val (YYMMDDHHMMSSZ or YYYYMMDDHHMMSSZ)
 -crl_nextupdate val     Sets the CRL nextUpdate time to val (YYMMDDHHMMSSZ or YYYYMMDDHHMMSSZ)
 -crldays +int           Days until the next CRL is due
 -crlhours +int          Hours until the next CRL is due
 -crlsec +int            Seconds until the next CRL is due
 -revoke infile          Revoke a cert (given in file)

Random state options:
 -rand val               Load the given file(s) into the random number generator
 -writerand outfile      Write random data to the specified file

Provider options:
 -provider-path val      Provider load path (must be before 'provider' argument if required)
 -provider val           Provider to load (can be specified multiple times)
 -propquery val          Property query used when fetching algorithms

Parameters:
 certreq                 Certificate requests to be signed (optional)
```
