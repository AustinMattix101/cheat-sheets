# POST 

curl -X POST http://localhost:5000/api/auth/login 
	-H "Content-Type: application/json" 
	-d '{"email": "songchimchek23712@gmail.com", "password": "ShunShenZe@23712"}'

# Get Method with HEADER

curl -i -H "Content-Language: en" http://localhost:5000/api/default

# Get Method with HEADER Authorization

curl -i -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYzN2E0YTViNTQ5MDA5NDdjOWNiYWQ5MyIsImlhdCI6MTY2OTE4NzMzNSwiZXhwIjoxNjY5MjczNzM1fQ.hUFod0DZvZxF4X4rnvWDJ-4CwKr2ZPjVw4xqau4Z1I4" http://localhost:5000/api/hello
