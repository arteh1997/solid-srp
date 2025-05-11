# SOLID Example code
Example code for SOLID.

## Setting up the database
Navigate to the db folder using `cd db`

Spin up database using docker:
```bash
docker-compose up --build -d
```

Run database migration scripts.
```bash
dotnet tool restore
dotnet dbup upgrade local.yml -e local.env --ensure
```

## Run the API
Navigate to the `Store.Api` folder and run `dotnet run`.

You can use the [Swagger UI](http://localhost:5010/swagger/index.html) to use the endpoints.

Use the `/auth` endpoint to get a token. You can use the following credentials:

- Admin User
  - Email: `admin.user@solid.com`
  - Password: `solidrocks`
- Normal User
  - Email: `normal.user@example.com`
  - Password: `solidrocks`