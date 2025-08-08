# MedSwift - Digital Healthcare Platform

A modern, intelligent healthcare web application built with the MERN stack that helps users manage their health records, check symptoms with AI, and consult doctors online — all in one place.

## 🚀 Features

### Core Features
- **AI Symptom Checker**: Input symptoms and get AI-powered condition suggestions with urgency scoring
- **Telemedicine Consultations**: Video, audio, and chat consultations with instant doctor matching
- **Smart Health Dashboard**: Digital storage for medical records and health analytics
- **Emergency Assist**: Quick access to emergency contacts and nearby hospitals with SOS functionality

### Key Capabilities
- 🔐 **Secure Authentication**: JWT-based authentication with role-based access (Patient, Doctor, Admin)
- 📱 **Real-time Communication**: WebRTC video calls and real-time messaging
- 📊 **Health Analytics**: Track health trends over time with interactive charts

- 📁 **File Management**: Upload and manage medical documents securely
- 🔔 **Notifications**: Real-time alerts and reminders

## 🛠 Tech Stack

### Frontend
- **React 18** - UI library
- **Vite** - Build tool and dev server
- **Redux Toolkit** - State management
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animations
- **React Query** - Data fetching and caching
- **Chart.js** - Data visualization
- **Axios** - HTTP client

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Socket.io** - Real-time communication
- **Multer** - File uploads
- **Helmet** - Security middleware

### External Services
- **Cloudinary** - File storage
- **Twilio** - Video calls and SMS

- **Nodemailer** - Email notifications

## 📁 Project Structure

```
medswift/
├── frontend/                 # React frontend application
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/           # Page components
│   │   ├── store/           # Redux store and slices
│   │   ├── utils/           # Utility functions
│   │   └── main.jsx         # Application entry point
│   ├── public/              # Static assets
│   ├── package.json         # Frontend dependencies
│   └── vite.config.js       # Vite configuration
├── backend/                  # Node.js backend application
│   ├── models/              # Mongoose models
│   ├── routes/              # API routes
│   ├── middleware/          # Custom middleware
│   ├── server.js            # Express server
│   ├── package.json         # Backend dependencies
│   └── .env.example         # Environment variables template
└── README.md               # Project documentation
```

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd medswift
   ```

2. **Quick Setup (Recommended)**
   ```bash
   # Run the automated setup script
   node start.js
   ```
   This will automatically:
   - Install all dependencies for both frontend and backend
   - Create the backend .env file from template
   - Provide setup instructions

3. **Manual Setup (Alternative)**
   ```bash
   # Install backend dependencies
   cd backend
   npm install
   
   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

4. **Environment Setup**
   ```bash
   # Backend environment (if not created by start.js)
   cd backend
   cp .env.example .env
   # Edit .env with your configuration
   ```

5. **Database Setup**
   - Install MongoDB locally or use MongoDB Atlas
   - Update the `MONGODB_URI` in your `.env` file

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   ```
   The API will be available at `http://localhost:5000`

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm run dev
   ```
   The application will be available at `http://localhost:3000`

### Production Build

1. **Build the frontend**
   ```bash
   cd frontend
   npm run build
   ```

2. **Start production server**
   ```bash
   cd backend
   npm start
   ```

## ⚙️ Environment Variables

### Backend (.env)
```env
# Server Configuration
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000

# Database
MONGODB_URI=mongodb://localhost:27017/medswift

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key
JWT_EXPIRE=7d

# Email Service (Nodemailer)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password

# File Upload (Cloudinary)
CLOUDINARY_CLOUD_NAME=your-cloud-name
CLOUDINARY_API_KEY=your-api-key
CLOUDINARY_API_SECRET=your-api-secret

# Video Calls (Twilio)
TWILIO_ACCOUNT_SID=your-account-sid
TWILIO_AUTH_TOKEN=your-auth-token



# AI Service (for symptom checker)
AI_SERVICE_URL=https://api.example.com/symptoms
AI_SERVICE_API_KEY=your-ai-service-key

# Security
BCRYPT_ROUNDS=12
RATE_LIMIT_WINDOW_MS=900000
RATE_LIMIT_MAX_REQUESTS=100
```

## 📚 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update user profile
- `PUT /api/auth/password` - Change password

### User Management
- `GET /api/users` - Get all users (admin)
- `GET /api/users/:id` - Get user by ID
- `DELETE /api/users/:id` - Delete user

### Doctor Management
- `GET /api/doctors` - Get all doctors
- `GET /api/doctors/:id` - Get doctor by ID



### Consultations
- `GET /api/consultations` - Get consultations
- `POST /api/consultations` - Create consultation
- `PUT /api/consultations/:id` - Update consultation

### Health Records
- `GET /api/health-records` - Get health records
- `POST /api/health-records` - Create health record
- `PUT /api/health-records/:id` - Update health record
- `DELETE /api/health-records/:id` - Delete health record

### Symptom Checker
- `POST /api/symptom-checker/analyze` - Analyze symptoms with AI

### Emergency Services
- `GET /api/emergency/contacts` - Get emergency contacts
- `POST /api/emergency/contacts` - Add emergency contact
- `PUT /api/emergency/contacts/:id` - Update emergency contact
- `DELETE /api/emergency/contacts/:id` - Delete emergency contact
- `POST /api/emergency/sos` - Trigger SOS alert
- `GET /api/emergency/hospitals` - Get nearby hospitals

## 🔧 Development

### Available Scripts

**Backend:**
```bash
npm run dev      # Start development server with nodemon
npm start        # Start production server
npm test         # Run tests
```

**Frontend:**
```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

### Code Style
- Use ESLint for code linting
- Follow consistent naming conventions
- Write meaningful commit messages
- Add comments for complex logic

## 🚀 Deployment

### Backend Deployment
1. Set up environment variables on your hosting platform
2. Build the application: `npm run build`
3. Start the server: `npm start`

### Frontend Deployment
1. Build the application: `npm run build`
2. Deploy the `dist` folder to your hosting platform
3. Update API endpoints in production

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 🔮 Future Enhancements

- [ ] Mobile app development
- [ ] AI-powered health recommendations
- [ ] Integration with wearable devices
- [ ] Advanced analytics dashboard
- [ ] Multi-language support
- [ ] Telemedicine regulations compliance
- [ ] Blockchain for medical records
- [ ] Voice-enabled consultations

---

**MedSwift** - Revolutionizing healthcare through technology 🏥✨ 