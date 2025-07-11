# Real-Time Chat Application

A full-stack real-time chat application built with PHP, MySQL, JavaScript, HTML, CSS, and WebSockets using Ratchet PHP.

## ✅ Features

- ✅ User Authentication (Login & Registration)
- ✅ Secure Password Hashing
- ✅ Session-based Authentication
- ✅ Real-Time Messaging (via WebSockets)
- ✅ Public Chat Rooms (Join/Leave)
- ✅ Message History
- ✅ Active User List
- ✅ Typing Indicators (Optional)
- ✅ Message Timestamps
- ✅ XSS Protection
- ✅ Responsive UI

## 🗃️ Project Structure

```
chat-app/
├── backend/
│   ├── db.php                # DB connection config
│   ├── login.php             # Login handler
│   ├── register.php          # Registration handler
│   ├── logout.php            # Logout script
│   └── websocket/
│       ├── Chat.php          # WebSocket logic (Ratchet)
│       └── chat-server.php   # WebSocket server entry
├── public/
│   ├── index.html            # Login/Register UI
│   ├── chat.html             # Chat interface
│   ├── styles.css            # App styling
│   └── script.js             # WebSocket JS logic
├── db/
│   └── database.sql          # SQL file to set up DB
├── composer.json             # PHP dependencies
└── README.md                 # Project documentation
```

## ⚙️ Installation Instructions

### 1. Requirements
- PHP >= 7.4
- Composer
- XAMPP/WAMP for local server (Apache + MySQL)

### 2. Clone or Extract the Project

Place the project folder inside your XAMPP `htdocs/` or WAMP `www/` directory.

### 3. Database Setup

1. Open `phpMyAdmin`
2. Create a database named `chat_app`
3. Import the file `db/database.sql` into it

### 4. Install WebSocket Dependencies

Navigate to the `backend/websocket/` folder and run:

```bash
composer install
```

This installs the required Ratchet library.

### 5. Start WebSocket Server

Run the following in terminal inside `backend/websocket/`:

```bash
php chat-server.php
```

Keep this terminal open while using the app.

### 6. Launch App in Browser

Start Apache & MySQL via XAMPP/WAMP and visit:

```
http://localhost/chat-app/public/index.html
```

## 🧾 Default Tables

### `users`
- `id`, `username`, `email`, `password`, `created_at`

### `chat_rooms`
- `id`, `name`, `description`, `created_at`

### `messages`
- `id`, `room_id`, `user_id`, `message_text`, `timestamp`

## 🔐 Security
- Passwords hashed with `password_hash()`
- Messages sanitized to prevent XSS

## 🚀 Optional Enhancements
- Typing indicators
- Desktop notifications
- Private messaging
- Message reactions

---

## 👨‍💻 Developed With
- PHP & MySQL
- HTML, CSS, JavaScript
- Ratchet WebSocket (PHP)
- XAMPP/WAMP for local hosting

---

Feel free to extend or modify this app for your learning or projects.
