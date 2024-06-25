# Healthcheck
curl -is -X GET localhost:4000/v1/healthcheck | sed -e "s/\r//g"
