# SnippetBox
SnippetBox is a simple web application for storing and sharing text snippets on the web.


# Installation
1. Clone the repository:
```bash
git clone https://github.com/ashvwinn/snippetbox.git
cd snippetbox
```

2. Set environment variables (look at .env.example for reference)

3. Setup database with Docker Compose:
```bash
docker compose up -d
```

4. Run database migrations with the [migrate](https://github.com/golang-migrate/migrate/tree/master/cmd/migrate) tool:
```bash
migrate -path=./migrations -database=$SNIPPETBOX_DB_DSN_MIGRATE up
```

5. Start the application:
With go:
```bash
go run ./cmd/web
# or
go build -o tmp/main ./cmd/web
./tmp/main
```

Or with [air](https://github.com/air-verse/air)
```bash
air
```
