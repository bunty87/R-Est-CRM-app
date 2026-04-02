# PropConnect CRM - Real Estate Lead Management System

A full-stack web application for real estate businesses to manage leads, projects, staff, and follow-ups efficiently. Built with React, Vite, Node.js, Express, and MongoDB.

## 🎯 Features

### Lead Management
- **Create & Edit Leads** - Add leads with name, mobile, email, budget, location, and notes
- **Lead Assignment** - Assign leads to staff members automatically or manually
- **Lead Status Tracking** - Track lead status (Interested, Callback, Visit Done, Deal Closed, Lost)
- **Lead Sources** - Track where leads come from (Facebook, Walk-in, Google Ads, Referral, MagicBricks, 99acres)
- **Advanced Filtering** - Filter leads by status, project, or assigned staff

### Follow-Up Management
- **Schedule Follow-ups** - Plan callbacks and site visits with date/time
- **Follow-up Types** - Call, WhatsApp, Site Visit, Meeting, Email
- **Missed Follow-up Alerts** - Get notified about overdue follow-ups
- **Follow-up History** - Complete audit trail of all communications
- **Smart Filtering** - View today's, pending, or all follow-ups

### Project Management
- **Project Dashboard** - View projects with lead counts and conversion rates
- **Project Configuration** - Customize project name, location, type, logo, and brand color
- **Project Status** - Mark projects as active or inactive
- **Lead Distribution** - See lead distribution across projects

### Staff Management
- **User Roles** - Admin and Staff roles with appropriate permissions
- **Staff Profiles** - Manage staff members with names, usernames, contact info
- **Project Assignment** - Assign staff to specific projects
- **Performance Metrics** - Track leads, closed deals, and follow-ups per staff member

### Reports & Analytics
- **Performance Dashboard** - View key metrics (Total Leads, Deals Closed, Conversion Rate)
- **Staff Performance** - See individual staff performance and conversion rates
- **Project Performance** - Track leads and closed deals per project
- **CSV Export** - Export reports for further analysis

### Additional Features
- **User Authentication** - Secure login for different user roles
- **Responsive UI** - Works seamlessly on desktop and tablet
- **Real-time Updates** - Instant UI updates without page refresh
- **Settings Panel** - Configure company name, branding, and notifications

## 🏗️ Tech Stack

### Frontend
- **React 19** - UI library
- **Vite 8** - Lightning-fast build tool
- **ESLint** - Code quality and style rules

### Backend
- **Node.js** - Runtime environment
- **Express 5** - Web framework
- **MongoDB 9** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **CORS** - Cross-origin resource sharing
- **Dotenv** - Environment configuration

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB instance (local or cloud - MongoDB Atlas)

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/R-Est.git
cd R-Est
```

### 2. Backend Setup
```bash
# Install dependencies
npm install

# Create .env file in the root directory
echo 'MONGO_URI=mongodb://localhost:27017/r-est' > .env
# Or use MongoDB Atlas
# echo 'MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/r-est' > .env

# Start the backend server
npm start
# Server runs on http://localhost:5000
```

### 3. Frontend Setup
```bash
cd client

# Install dependencies
npm install

# Start the development server
npm run dev
# Client runs on http://localhost:5173
```

## 📦 Project Structure

```
R-Est/
├── client/                 # React frontend (Vite)
│   ├── src/
│   │   ├── App.jsx        # Main app with all components
│   │   ├── App.css        # Styling
│   │   ├── main.jsx       # Entry point
│   │   └── index.css      # Global styles
│   ├── public/            # Static assets
│   ├── vite.config.js     # Vite configuration
│   ├── eslint.config.js   # ESLint rules
│   └── package.json
├── routes/                # Backend API routes
│   ├── auth.js           # Authentication endpoints
│   └── leads.js          # Lead management endpoints
├── server.js             # Express server entry point
├── package.json          # Backend dependencies
└── .env                  # Environment variables (not committed)
```

## 🛣️ API Endpoints

### Authentication
- `POST /api/auth/login` - User login

### Leads
- `GET /api/leads` - Get all leads
- `POST /api/leads` - Create new lead
- `PUT /api/leads/:id` - Update lead
- `DELETE /api/leads/:id` - Delete lead

### Additional endpoints can be added for projects, staff, and follow-ups.

## 🎨 Key UI Components

### Dashboard
Main overview with metrics including total leads, closed deals, and conversion rates.

### Leads Module
Complete CRUD interface for managing leads with filters and search.

### Follow-ups Module
Schedule and track all lead communications with date/time management.

### Projects Module
Configure and monitor real estate projects with branding options.

### Staff Module
Manage team members, assign projects, and view performance metrics.

### Reports
Analytics dashboard with staff and project performance charts.

## 🔐 Default Mock Users

The app comes with pre-loaded mock data:

| Username | Password | Role | Projects |
|----------|----------|------|----------|
| admin | admin123 | Admin | All |
| ravi | ravi123 | Staff | Prestige Sunrise, Green Valley Plots |
| priya | priya123 | Staff | Prestige Sunrise |

**Note:** This is mock data for demo purposes. Connect to a real database and implement proper authentication.

## 📝 Environment Variables

Create a `.env` file in the root directory:

```env
MONGO_URI=mongodb://localhost:27017/r-est
PORT=5000
NODE_ENV=development
```

For production with MongoDB Atlas:
```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/r-est?retryWrites=true&w=majority
PORT=5000
NODE_ENV=production
```

## 🔄 Development Workflow

### Frontend
```bash
cd client
npm run dev        # Start development server with HMR
npm run build      # Create optimized production build
npm run preview    # Preview production build
npm run lint       # Run ESLint
```

### Backend
```bash
npm start          # Start Express server
```

## 📦 Build for Production

### Frontend
```bash
cd client
npm run build
# Creates optimized build in dist/ folder
```

### Backend
Ensure `.env` is configured with production database credentials, then deploy the entire project.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
## images
<img width="1114" height="799" alt="Screenshot 2026-04-02 100345" src="https://github.com/user-attachments/assets/866c5c72-bea4-4f9f-ba7a-ce702fe4c521" />

## 🐛 Known Issues & TODO

- [ ] Replace mock data with real database integration
- [ ] Implement proper authentication and JWT tokens
- [ ] Add email notifications for follow-ups
- [ ] Implement data export to Excel/PDF
- [ ] Add team collaboration features
- [ ] Mobile app version
- [ ] Advanced reporting with charts and graphs

## 📄 License

This project is licensed under the ISC License - see the LICENSE file for details.

## 👥 Authors

- **Your Name** - *Initial work*

## 📞 Support

For support, email support@propconnect.com or create an issue in the repository.

## 🎓 Learning Resources

- [React Documentation](https://react.dev)
- [Vite Guide](https://vitejs.dev)
- [Express.js Guide](https://expressjs.com)
- [MongoDB University](https://university.mongodb.com)

---

**Last Updated:** April 2, 2026  
**Version:** 1.0.0
