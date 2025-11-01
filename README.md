# QMS - Quality Management System

A comprehensive Quality Management System built with Next.js, React.js, and SQL. This application provides two main modules: Super Admin for managing companies and Client Admins, and Client Admin for managing users, roles, and workflows within companies.

## Features

### Super Admin Module
- **Company Management**: Add new companies with unique domains
- **Client Admin Creation**: Create Client Admin accounts for each company
- **Company Overview**: View all companies with user counts and creation dates

### Client Admin Module
- **User Management**: Create and manage users within the company
- **Role Definition**: Define custom roles with specific permissions
- **Workflow Configuration**: Configure workflows and assign them to users

## Technology Stack

- **Frontend**: Next.js 16 with React.js
- **Backend**: Next.js API routes
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js with credentials provider
- **Styling**: Tailwind CSS
- **TypeScript**: Full type safety throughout the application

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- PostgreSQL database (or use Prisma Postgres for development)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd qms-application
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Copy the `.env` file and update the values:
   ```bash
   # Database
   DATABASE_URL="your-postgresql-connection-string"
   
   # NextAuth
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=your-secret-key-here
   
   # Application
   NODE_ENV=development
   ```

4. **Set up the database**
   ```bash
   # Generate Prisma client
   npx prisma generate
   
   # Run database migrations
   npx prisma migrate dev --name init
   ```

5. **Create a Super Admin account**
   
   You can create a Super Admin account directly in the database or use the Prisma Studio:
   ```bash
   npx prisma studio
   ```

6. **Start the development server**
   ```bash
   npm run dev
   ```

   The application will be available at `http://localhost:3000`

## Usage

### Super Admin Login

1. Go to the application homepage
2. Select "Super Admin" from the account type dropdown
3. Enter your Super Admin credentials
4. Access the Super Admin dashboard to:
   - View all companies
   - Add new companies
   - Create Client Admin accounts

### Client Admin Login

1. Go to the application homepage
2. Select "Client Admin / User" from the account type dropdown
3. Enter your Client Admin credentials
4. Access the Client Admin dashboard to:
   - Manage users in your company
   - Define roles and permissions
   - Configure workflows

## Database Schema

The application uses the following main entities:

- **SuperAdmin**: Super administrator accounts
- **Company**: Companies managed by the system
- **User**: Users (including Client Admins) within companies
- **Role**: Roles with specific permissions
- **Workflow**: Configurable workflows
- **WorkflowAssignment**: User workflow assignments

## API Endpoints

### Super Admin APIs
- `GET /api/super-admin/companies` - Get all companies
- `POST /api/super-admin/companies` - Create a new company with Client Admin

### Client Admin APIs
- `GET /api/client-admin/users` - Get users in the company
- `GET /api/client-admin/roles` - Get roles in the company
- `GET /api/client-admin/workflows` - Get workflows in the company

### Authentication
- `POST /api/auth/[...nextauth]` - NextAuth.js authentication endpoints

## Development

### Project Structure

```
src/
├── app/                 # Next.js App Router pages
│   ├── api/            # API routes
│   ├── super-admin/    # Super Admin dashboard
│   ├── client-admin/   # Client Admin dashboard
│   └── auth/           # Authentication pages
├── components/         # Reusable React components
├── lib/               # Utility libraries
├── types/             # TypeScript type definitions
└── prisma/            # Database schema and migrations
```

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npx prisma studio` - Open Prisma Studio database browser
- `npx prisma migrate dev` - Run database migrations

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `DATABASE_URL` | PostgreSQL connection string | Yes |
| `NEXTAUTH_URL` | Application URL for NextAuth | Yes |
| `NEXTAUTH_SECRET` | Secret key for NextAuth | Yes |
| `NODE_ENV` | Environment (development/production) | No |

## Security Features

- **Password Hashing**: All passwords are hashed using bcryptjs
- **Session Management**: Secure JWT-based sessions with NextAuth.js
- **Role-based Access Control**: Different access levels for Super Admins and Client Admins
- **Company Isolation**: Client Admins can only access their company's data

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
