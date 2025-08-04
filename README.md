# Wizard Form (Laravel Project)

## 🧰 Requirements

- Node.js 18.19+ and npm 9.2+


## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/pavliqqq/docker.git
```

### 2. Environment Setup

```bash
cp .env.example .env
```
Edit the .env file to configure your environment variables (database, app key, etc.):

### 3. Launch Containers and Access app

```bash
docker-compose up -d --build
```

```bash
docker exec -it wizardForm_app bash
```

### 4. Install Dependencies

```bash
composer install
```

### 5. Generate key

```bash
php artisan key:generate
```

### 6. Database Setup

1) Run migrations

```bash
php artisan migrate
```

2) Run admin seeder

```bash
php artisan db:seed --class=AdminSeeder
```

### 7. Create the storage symbolic link

```bash
php artisan storage:link
```

### 8. Install JS dependencies

```bash
npm install
npm run dev
```


Project will be accessible at:
http://localhost:8080


The database contains a default admin user seeded 
with email: admin@gmail.com and password: 12345.

You can access the admin login page at:
http://localhost:8000/admin/login
