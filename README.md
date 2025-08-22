# docker-mongodb-boilerplate

A Docker MongoDB boilerplate with Docker Compose, including Mongo Express for
database management, and a detailed setup guide for easy configuration and
deployment.

## How to Setup

### 1. MongoDB Setup:

Use the `.env.example` file as a reference to set up the required environment
variables.

After doing that, run the following command to create your MongoDB service:

```bash
docker compose -p mongodb up -d
```

To take down the Docker services, just use:

```bash
docker compose -p mongodb down
```

MongoDB will be accessible on the default port **27017**. Your data is persisted
in the Docker volume `mongo_data`.

### 2. Mongo Express Setup:

Once your containers are up and running, navigate to
[http://localhost:8081](http://localhost:8081) to access your Mongo Express
service. Login with the credentials set in your `.env` file.

Mongo Express will automatically connect to the MongoDB service (`mongodb`)
using the admin credentials provided.

When consuming your MongoDB database in your projects, use the following URL
structure:

`mongodb://USERNAME:PASSWORD@localhost:PORT`

Replace `USERNAME`, `PASSWORD`, and `PORT` with the values from your `.env` file
and Docker Compose setup.

## Licence

This is an open-source project and is available under the
[**MIT License**](LICENSE). You are free to use, modify, and distribute the code
in accordance with the terms of the license.

## Contributors

Contributions are highly appreciated! If you encounter any issues or have
suggestions for improvements, please feel free to open an issue or submit a pull
request.

[feliperdamaceno](https://github.com/feliperdamaceno)

## Contact me

Linkedin: [feliperdamaceno](https://www.linkedin.com/in/feliperdamaceno)
