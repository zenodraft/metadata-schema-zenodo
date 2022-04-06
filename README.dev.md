# Developer notes


```shell
# get the list of licenses from opendefinition
LIST0=`curl https://licenses.opendefinition.org/licenses/groups/all.json | jq '.[].id'`

#get the list of licenses from spdx
LIST1=`curl https://raw.githubusercontent.com/spdx/license-list-data/master/json/licenses.json | jq '.licenses[].licenseId'`

# combine, unique, add trailing comma
echo -e "$LIST0\n$LIST1" | sort | uniq | sed s/$/,/g

# then, copy paste into schema.json
```
