# redash_oracle
Build docker file for redash with Orcale support 
1. Get the oracle drivers manuly from oracle, copy Oracle driver *.zip to ```./oracle/```
2. Build the custom docker image , force refresh of redash image
  ```docker build --pull -t custom/redash:latest -t custom/redash:<actual redash version>```
3. Follow redash upgrade guideline : https://redash.io/help/open-source/admin-guide/how-to-upgrade (assuming this is upgrade process)
    3.1 Change directory to /opt/redash.
    3.2 copy docker-compose.yml  to /opt/redash/docker-compose.yml 
    3.3 Stop Redash services: 
    ``` docker-compose stop server scheduler scheduled_worker adhoc_worker ``` (you might need to list additional services if you updated your configuration)
    3.4 Apply migration (if necessary): ``` docker-compose run --rm server manage db upgrade ```
    3.5 ``` Start services: docker-compose up -d ```

 
