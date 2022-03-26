SONARQUBE_URL=$(aws cloudformation list-exports | jq '.Exports[] | select(.Name=="SonarQubeURL").Value' | tr -d '[\"\n]')

ZAP_URL=$(aws cloudformation list-exports | jq '.Exports[] | select(.Name=="OWASPZapURL").Value' | tr -d '[\"\n]')

export ZAPAPIKEY="workshopzapkey"
