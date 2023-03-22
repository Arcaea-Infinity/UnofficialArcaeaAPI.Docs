# How to deploy AUA

### Get Started

* Install ASP.NET Core Runtime 6.0
* Download the latest release
* Start service
* Follow the prompts to proceed after filling in the `challenge_token`, saving and restarting the service

### Configuration fields

* config.json

  | field           | description                                                   | example                                   |
  |:----------------|:--------------------------------------------------------------|-------------------------------------------|
  | api_entry       | latest Arcaea API entry                                       | "join/21"                                 |
  | app_version     | latest Arcaea version                                         | "4.3.2c"                                  |  
  | host            | latest Arcaea API Host                                        | "arcapi-v2.lowiro.com"                    |
  | cert_name       | certificate file name in the data folder                      | "cert-4.3.2c.p12"                         |
  | cert_password   | certificate file password                                     | "HelloWorld"                              |
  | data_path       | path to save files and databases                              | "/etc/arcaeaunlimitedapi/data"            |
  | open_register   | whether to enable the automatic registration task             | true                                      |
  | quota           | Allow the number of requests without token per ip per day     | 10                                         |
  | challenge_type  | the type of the challenge API                                 | "aua" <br/> "taikari"                     |  
  | challenge_api   | the url of the challenge API                                  | "https://example.com/botarcapi/challenge" |
  | challenge_token | the token of the challenge API (Taikari API will ignore this) | "yourtokenhere"                           |
  | nodes           | TCP port forwarding server                                    |                                           |

> Note: most of fields in `config.json` is not need to fill in manually after the first-start

* tokens.json
  *  whitelist array of token(string) in json format

* appsettings.json

  | field | description                  | example                                       |
  |:------|:-----------------------------|-----------------------------------------------|
  | urls  | port to provide your service | "https://*:616" <br/> "https://localhost:616" |

### How a node works

* Bypass rate limiting for a single IP with tcp port forwarding
  * When it is needed to send a large number of requests to arcapi in a short period of time (e.g. Best30 query)
  * AUA will evenly distribute requests to each node

### How to set up a node

* Linux server
  * install socat, and just run
    ```bash
    socat -d TCP4-LISTEN:6161,reuseaddr,fork TCP4:arcapi-v2.lowiro.com:443
    ```
  * It is highly recommended that set it as a background task


* Windows server
  * run cmd as administrator, then run
    
    ```bash
    netsh interface portproxy add v4tov4 listenport=6161 connectaddress=arcapi-v2.lowiro.com connectport=443
    ```

* Other avaliable solutions could be adapted such as stream of nginx


* Don't forget to open the port in the firewall


* Add the node in config.nodes like
    ```json
    {
        "url": "192.3.xxx.xxx",
        "port": 6161, 
        "active": true
    }
    ```

* How to test node
  * Access `https://${nodeip}:${port}/${api_entry}/` with a browser or curl and check if the certificate is from *.lowiro.com 
