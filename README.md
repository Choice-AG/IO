//start server
php -S localhost:8000 -t ./public

//curl
curl -d '{"id":9,"name":"baeldung"}' -H 'Content-Type: application/json' -X PUT http://localhost:8000