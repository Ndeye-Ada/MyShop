# MyShop Backend

Backend for the **MyShop** project developed with **FastAPI**.  
Main features:
- User authentication and registration
- CRUD management for products

## Technologies Used

- **FastAPI** (Python)
- **PostgreSQL** (containerized)
- **pgAdmin** (containerized)
- **Docker** & **Docker Compose**

## Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Installation

1. **Clone the repository**
    ```bash
    git@github.com:ndeyetou/my-shop-backend.git
    ```

2. **Start the services**
    ```bash
    docker-compose up --build
    ```

3. **Create a virtual environment (optional)**  
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```

4. **Run FastAPI manually (optional)**  
    Start FastAPI:
    ```bash
    uvicorn app.main:app --reload
    ```

5. **Access the API**
    - Interactive documentation: [http://localhost:8000/docs](http://localhost:8000/docs)

6. **Access pgAdmin**
    - [http://localhost:5050](http://localhost:5050)
    - Use the credentials defined in `.env`

## Main Endpoints

- `POST /auth/register`: User registration
- `POST /auth/login`: User authentication
- `GET /api/v1/products/products/`: List all products
- `GET /api/v1/products/products/{product_id}`: Get a product by ID
- `POST /api/v1/products/products/`: Create a product
- `PUT /api/v1/products/products/{product_id}`: Update a product
- `DELETE /api/v1/products/products/{product_id}`: Delete a product

## Configuration
To generate a random secret key (for example, for JWT), you can use the following command:

```bash
python3 -c "import secrets; print(secrets.token_urlsafe(32))"
```

Environment variables (JWT_SECRET, etc.) should be set in a `.env` file.









# MyShopFrontend

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.0.6.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
