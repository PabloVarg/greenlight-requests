# Options
curl -is -X OPTIONS localhost:4000/v1/movies/1 | sed -e "s/\r//g"

---
# Get a movie
curl -is -X GET localhost:4000/v1/movies/3 | sed -e "s/\r//g"

---
# Get an invalid movie
curl -is -X GET localhost:4000/v1/movies/-1 | sed -e "s/\r//g"

---
# Create a movie
curl -is -X POST -d '{"title":"The Breakfast Club","year":1986, "runtime":"96 mins","genres":["drama"]}' localhost:4000/v1/movies | sed -e "s/\r//g"

---
# Create an invalid movie
curl -is -X POST -d '{"title":"","year":1000,"runtime":"-123 mins","genres":["sci-fi","sci-fi"]}' localhost:4000/v1/movies | sed -e "s/\r//g"

---
# Error
curl -is -X DELETE localhost:4000/v1/movies/1 | sed -e "s/\r//g"

---
# Update a movie
curl -is -X PUT -d '{"title":"Black Panther","year":2018,"runtime":"134 mins","genres":["sci-fi","action","adventure"]}' localhost:4000/v1/movies/3 | sed -e "s/\r//g"

---
# Partial update a movie
curl -is -X PATCH -d '{"year": 1985, "title": ""}' localhost:4000/v1/movies/3 | sed -e "s/\r//g"

---
# Delete a movie
curl -is -X DELETE localhost:4000/v1/movies/2 | sed -e "s/\r//g"
