# Non existing route
curl -is -X GET localhost:4000/v2/movies/1 | sed -e "s/\r//g"

# Invalid method
curl -is -X PUT localhost:4000/v1/movies/1 | sed -e "s/\r//g"
