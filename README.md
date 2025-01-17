# WAFW00F

WAFW00F identifies and fingerprints Web Application Firewall (WAF) products.

## How does it work?

To do its magic, WAFW00F does the following:

- Sends a _normal_ HTTP request and analyses the response; this identifies a
  number of WAF solutions
- If that is not successful, it sends a number of (potentially malicious) HTTP
  requests and uses simple logic to deduce which WAF it is
- If that is also not successful, it analyses the responses previously
  returned and uses another simple algorithm to guess if a WAF or security
  solution is actively responding to our attacks

For further details, check out the source code on the main site,
[github.com/sandrogauci/wafw00f](https://github.com/sandrogauci/wafw00f).

## What does it detect?

It detects a number of WAFs. To view which WAFs it is able to detect run
WAFW00F with the `-l` option. At the time of writing the output is as follows:

    $ ./wafw00f -l
    
                                     ^     ^
            _   __  _   ____ _   __  _    _   ____
           ///7/ /.' \ / __////7/ /,' \ ,' \ / __/
          | V V // o // _/ | V V // 0 // 0 // _/
          |_n_,'/_n_//_/   |_n_,' \_,' \_,'/_/
                                    <
                                     ...'
                                     
        WAFW00F - Web Application Firewall Detection Tool
        
        By Sandro Gauci && Wendel G. Henrique
        
    Can test for these WAFs:

    Applicure dotDefender
    Art of Defence HyperGuard
    Aqtronix WebKnight
    Barracuda Aplication Firewall
    BinarySec
    Cisco ACE XML Gateway
    Citrix NetScaler
    CloudFlare
    DenyALL WAF
    eEye Digital Security - SecureIIS
    F5 FirePass
    F5 TrafficShield
    F5 BIG-IP (LTM, APM, ASM)
    IBM Web Application Security
    IBM DataPower
    Imperva SecureSphere
    InfoGuard Airlock    
    Incapsula WAF
    Juniper WebApp Secure
    Microsoft ISA Server
    Microsoft UrlScan
    NetContinuum
    Profense
    TrustWave ModSecurity
    Teros WAF
    USP Secure Entry Server

  
## How do I use it?

For help please make use of the `--help` option. The basic usage is to pass it
a URL as an argument. Example:

    $./wafw00f https://www.ibm.com/
    
                                     ^     ^
            _   __  _   ____ _   __  _    _   ____
           ///7/ /.' \ / __////7/ /,' \ ,' \ / __/
          | V V // o // _/ | V V // 0 // 0 // _/
          |_n_,'/_n_//_/   |_n_,' \_,' \_,'/_/
                                    <
                                     ...'
                                     
        WAFW00F - Web Application Firewall Detection Tool
        
        By Sandro Gauci && Wendel G. Henrique
        
    Checking https://www.ibm.com/
    The site https://www.ibm.com/ is behind a Citrix NetScaler
    Number of requests: 6
    

## Need a freelance pentester?

More information about the services that I offer at [Enable Security](http://enablesecurity.com/)

## Questions?

Contact [me](mailto:sandro@enablesecurity.com)

