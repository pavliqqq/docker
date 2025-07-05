# Wizard Form (Laravel Project)

## 🧰 Requirements

- Node.js 22.13 and npm 10.9 //check
- Git (optional)


## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/pavliqqq/docker.git
```

### 2. Install Dependencies

```bash
composer install
```

### 3. Environment Setup

```bash
cp .env.example .env
```
Edit the .env file to configure your environment variables (database, app key, etc.):

```bash
php artisan key:generate
```
### 4. Install JS dependencies

```bash
npm install
npm run dev
```

### 5. Database Setup

1) Run migrations

```bash
php artisan migrate
```

2) Run admin seeder

```bash
php artisan db:seed --class=AdminSeeder
```

### 6. Create the storage symbolic link

```bash
php artisan storage:link
```

### 7. Docker compose up

```bash
docker-compose up -d
```

Project will be accessible at:
http://localhost:8080


The database contains a default admin user seeded 
with email: admin@gmail.com and password: 12345.

You can access the admin login page at:
http://localhost:8000/admin/login
