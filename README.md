<p align="center">
    <a href="https://laravel.com" target="_blank">
        <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
    </a>
</p>

<p align="center">
    <a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
    <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
    <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
    <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Laravel Chat Application (Laravel + Reverb )

Welcome to the Laravel Chat Application! This application allows you to create real-time chat conversations between users using the Laravel framework. It includes features such as user authentication, chat rooms, and real-time messaging.

## Laravel Reverb Server Settings

This repository contains essential server configuration settings for deploying and managing Laravel applications. It includes configurations for:

- Nginx setup
- Pusher integration
- Supervisor process management
- And other key server settings
These configurations aim to streamline the deployment and management of Laravel applications, ensuring a smooth and efficient production environment.

The repository is designed for a simple chat app, Laravel Reverb, and serves as a guide for developers who want to set up this application locally. Often, when deploying Laravel Reverb to a production server, developers encounter issues. This repository helps solve those problems by providing detailed instructions and configurations for a seamless server setup, ensuring a smooth deployment process.





## Features

- **Real-time messaging:** Chat messages are sent and received instantly using WebSocket technology.
- **User authentication:** Register, login, and logout functionality for users.
- **Chat rooms:** Users can create or join chat rooms to communicate with other users.
- **User profiles:** View and edit user profile information.
- **Secure communication:** Messages are transmitted securely over the network.

## Installation and Setup

Follow the instructions below to install and run the project on your local machine:

### Step 1: Clone the Repository

Clone the repository from GitHub:

```bash
git clone https://github.com/AjayYadavAi/laravel-reverb-chat-app.git
```

### Step 2: Navigate to the Project Directory

Change to the project directory:

```bash
cd laravel-chat-app
```

### Step 3: Install Dependencies

Install the required PHP and JavaScript dependencies:

```bash
composer install
npm install
```

### Step 4: Create an Environment File

Copy the `.env.example` file to a new file named `.env`:

```bash
cp .env.example .env
```

Configure the `.env` file with your database and other settings.

### Step 5: Generate an Application Key

Generate a new application key:

```bash
php artisan key:generate
```

### Step 6: Run Migrations and Seed the Database

Run the migrations to set up the database schema:

```bash
php artisan migrate
```

Seed the database with default data (if available):

```bash
php artisan db:seed
```

### Step 7: Start the WebSocket Server

To enable real-time messaging, you need to start the Reverb server:

```bash
php artisan reverb:start
```

### Step 8: Start the Application

Start the Laravel application:

```bash
php artisan serve
```

The application will run on `http://127.0.0.1:8000`.

## Nginx File
Paste Socket.conf file to nginx 
and Add your Domain 
and remove my certbot configuration addrees and genrate new ssl

## Supervioser Setting
- install supervioser
- past reverb.conf file in to /etc/supervioser/conf.d/
- then read or update supervioser 
- then start supervioser

## Pusher
Create and Account on https://pusher.com/

Then Create an app choose laravel or vue and Enter then go ```APP KEY  Copy
- app_id =   , 
- key =      ,
- secret =   ,
- cluster =  ,

Then paste the keys in .env file 

## Add you Cluster Pusher Region in you config/Broadcasting.php file

- for example go pusher area      'host' => env('PUSHER_HOST') ?: 'api-'.env('PUSHER_APP_CLUSTER', 'ap2').'.pusher.com',
- only change ap2 to your Pusher Region


## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests for any improvements or bug fixes.
