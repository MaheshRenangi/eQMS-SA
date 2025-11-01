# 🔐 QMS Application - Login Credentials Guide

## 📍 Application URL
**Access your QMS Application at:** http://localhost:3000

---

## 👥 Available Test Accounts

### 🔐 Super Admin
- **Name:** Super Admin
- **Email:** `admin@qms.com`
- **Password:** `admin123`
- **Role:** System Administrator
- **Company:** QMS System
- **Access Level:** Full system access and company management
- **Features:**
  - Create and manage companies
  - View system-wide statistics
  - Manage client administrators
  - System configuration

---

### 👨‍💼 Client Admin
- **Name:** Client Admin
- **Email:** `client@example.com`
- **Password:** `client123`
- **Role:** Company Administrator
- **Company:** Example Company
- **Access Level:** Company-level administration
- **Features:**
  - Manage company users
  - Define roles and permissions
  - Configure workflows
  - View company analytics

---

### 👤 Regular User 1
- **Name:** John Doe
- **Email:** `user1@example.com`
- **Password:** `user123`
- **Role:** User
- **Company:** Example Company
- **Access Level:** Basic user access
- **Features:**
  - Task management
  - View assigned workflows
  - Submit reports
  - Basic dashboard

---

### 👩‍💻 Regular User 2
- **Name:** Jane Smith
- **Email:** `user2@example.com`
- **Password:** `user456`
- **Role:** Administrator (within company)
- **Company:** Example Company
- **Access Level:** Advanced user with administrative privileges
- **Features:**
  - Advanced user management
  - Workflow administration
  - Enhanced reporting
  - Administrative dashboard

---

## 🚀 How to Use

### Method 1: Enhanced Login Form
1. Visit http://localhost:3000
2. Click "Show Credentials" on the login form
3. Browse all available accounts with detailed information
4. Click "Use These Credentials" to auto-fill the form
5. Or copy individual email/password using the copy buttons

### Method 2: Quick Access
1. Visit http://localhost:3000
2. Use the quick access buttons for Super Admin or Client Admin
3. Manual entry for regular users

### Method 3: Manual Entry
1. Select account type (Super Admin or Client Admin)
2. Enter email and password manually
3. Click "Sign In"

---

## 🎯 Account Features Comparison

| Feature | Super Admin | Client Admin | Regular User |
|---------|-------------|--------------|--------------|
| Company Management | ✅ | ❌ | ❌ |
| User Management | ✅ | ✅ | ❌ |
| Role Definition | ✅ | ✅ | ❌ |
| Workflow Configuration | ✅ | ✅ | ❌ |
| Task Management | ✅ | ✅ | ✅ |
| Reports & Analytics | ✅ | ✅ | ✅ |
| System Settings | ✅ | ❌ | ❌ |

---

## 🛠️ Technical Details

- **Database:** SQLite with seeded test data
- **Authentication:** NextAuth.js with credentials provider
- **Session Management:** Automatic role-based redirects
- **Security:** Bcrypt password hashing
- **UI:** Enhanced with professional design and gradients

---

## 🆘 Troubleshooting

### If login fails:
1. Ensure you've selected the correct account type (Super Admin vs Client Admin)
2. Check email and password spelling
3. Try using the "Use These Credentials" buttons for auto-fill
4. Refresh the page and try again

### If page doesn't load:
1. Ensure the development server is running: `npm run dev`
2. Check the URL: http://localhost:3000
3. Clear browser cache and reload

---

## 🎨 Enhanced Features

- **Password Visibility Toggle:** Click the eye icon to show/hide passwords
- **Auto-fill Credentials:** One-click credential filling
- **Copy to Clipboard:** Copy email/password individually
- **Account Details:** Comprehensive user information display
- **Professional Design:** Modern UI with gradient backgrounds and animations

---

*Last Updated: October 30, 2025*
*QMS Application v1.0*