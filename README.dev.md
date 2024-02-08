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



File `schema.json` contains the JSONschema schema for the metadata used when making uploads to Zenodo or Zenodo Sandbox. It was derived by hand using the following resources:

1. https://github.com/zenodo/zenodo/blob/f091af8f2d0bfac2fdaf53222160f8e037d5a0e6/zenodo/modules/deposit/static/json/zenodo_deposit/deposit_form.json
2. https://github.com/zenodo/zenodo/blob/594bad1d2c3c12c2d44a8f35950662677d51414b/tests/unit/conftest.py#L1376-L1430
