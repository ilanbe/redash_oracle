# redash_oracle
Build docker file for redash with Orcale support 
1. Get the oracle drivers manuly from oracle, copy Oracle driver *.zip to ```./oracle/```
2. Build the custom docker image , force refresh of redash image
  ```docker build --pull -t custom/redash:latest -t custom/redash:<actual redash version>```
3. Follow redash upgrade guideline : https://redash.io/help/open-source/admin-guide/how-to-upgrade
 
