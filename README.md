- 👋 Hi, I’m @naY9yjoS6ZqhOd35sIFH
- 👀 I’m interested in keepass
- 🌱 I’m currently learning k8s
```sh
solusbw(){
local soluskey=$1
local solushash=$2
local solusurl=https://$3/api/client/command.php

curl -s -L --data "key=$soluskey&hash=$solushash&action=info&bw=true" $solusurl|grep -oP '(?<=bw>).*(?=</bw>)'
}
kiwivmbw(){
local veid=$1
local apikey=$2
local apiurl=https://$3/v1/getServiceInfo

curl -s -L "$apiurl?veid=$veid&api_key=$apikey"|jq ".data_counter"
}
```
