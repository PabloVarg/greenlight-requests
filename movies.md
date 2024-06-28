# Options
curl -is -X OPTIONS localhost:4000/v1/movies/1 | sed -e "s/\r//g"

---
# Get a movie
curl -is -X GET localhost:4000/v1/movies/1 | sed -e "s/\r//g"

---
# Get an invalid movie
curl -is -X GET localhost:4000/v1/movies/-1 | sed -e "s/\r//g"

---
# Create a movie
curl -is -X POST -d '{"title":"Moana","year":2016,"runtime":107, "genres":["animation","adventure"]}' localhost:4000/v1/movies | sed -e "s/\r//g"

---
# Error
curl -is -X DELETE localhost:4000/v1/movies/1 | sed -e "s/\r//g"
