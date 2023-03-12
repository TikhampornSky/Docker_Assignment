# You don't need to modify the following 
FROM __________

WORKDIR /var/dmongo
COPY __________ /var/dmongo
CMD mongoimport --host asset_mapping -d user -c userProfile --drop --type json --file /var/dmongo/profile_asset.json --jsonArray
