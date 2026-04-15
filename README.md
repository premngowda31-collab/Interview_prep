# Interview Prep - MERN Stack Application

An AI-powered interview preparation platform built with the MERN (MongoDB, Express, React, Node.js) stack. This application helps users practice DSA problems, conduct mock interviews, and track their progress.

## 🚀 Features

- **User Authentication**: Secure login and registration system with JWT
- **DSA Practice**: Extensive collection of Data Structures and Algorithms problems
- **Mock Interviews**: AI-powered mock interview sessions with real-time feedback
- **Progress Tracking**: Track your progress across different topics and subjects
- **Admin Dashboard**: Manage problems, subjects, and topics
- **Subject Management**: Organize DSA problems by subjects and topics
- **Performance Analytics**: Visual charts and statistics of your progress

## 🛠️ Tech Stack

### Frontend
- **React** (v19.2.0) - UI library
- **Vite** (v7.3.1) - Build tool and dev server
- **TailwindCSS** (v4.2.1) - Utility-first CSS framework
- **React Router** (v7.13.1) - Client-side routing
- **Axios** - HTTP client for API calls
- **React Hook Form** - Form state management
- **Recharts** - Data visualization library
- **React Hot Toast** - Notification system

### Backend
- **Node.js** - Runtime environment
- **Express** (v5.2.1) - Web framework
- **MongoDB** (with Mongoose) - Database
- **JWT** - Authentication
- **Groq SDK** - AI integration for interview feedback
- **ElevenLabs** - Text-to-speech API
- **OpenAI** - Additional AI capabilities

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB (local or MongoDB Atlas)
- Git

## 🔧 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/premngowda31-collab/Interview_prep.git
cd Interview_prep
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend folder with the following variables:
```env
MONGO_URI=mongodb://127.0.0.1:27017/interview_prep
GROQ_API_KEY=your_groq_api_key
JWT_SECRET=your_secret_key
JWT_EXPIRES_IN=7d
PORT=5000
CLIENT_URL=http://localhost:5173
ELEVENLABS_API_KEY=your_elevenlabs_api_key
OPENAI_API_KEY=your_openai_api_key
```

### 3. Frontend Setup
```bash
cd frontend
npm install
```

## 🚀 Running the Application

### Start Backend Server
```bash
cd backend
npm run dev
```
Backend will run on `http://localhost:5000`

### Start Frontend Server
In a new terminal:
```bash
cd frontend
npm run dev
```
Frontend will run on `http://localhost:5173`

## 📁 Project Structure

```
Interview_Mern/
├── backend/
│   ├── config/          # Database configuration
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/          # Database schemas
│   ├── routes/          # API routes
│   ├── services/        # Business logic
│   ├── Server.js        # Main server file
│   └── .env             # Environment variables
│
├── frontend/
│   ├── src/
│   │   ├── components/  # Reusable components
│   │   ├── pages/       # Page components
│   │   ├── services/    # API service calls
│   │   ├── context/     # React context for state
│   │   ├── App.jsx      # Main app component
│   │   └── main.jsx     # Entry point
│   └── vite.config.js   # Vite configuration
│
└── README.md
```

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update user profile

### DSA Problems
- `GET /api/dsa/problems` - Get all problems
- `GET /api/dsa/problems/:id` - Get problem details
- `POST /api/dsa/problems/:id/solve` - Mark problem as solved
- `DELETE /api/dsa/problems/:id/solve` - Unmark problem
- `GET /api/dsa/companies` - Get companies list
- `GET /api/dsa/topics` - Get topics list

### Mock Interviews
- `POST /api/interview/start` - Start interview session
- `GET /api/interview` - Get all interviews
- `GET /api/interview/:id` - Get interview details
- `PUT /api/interview/:id/answer/:qIdx` - Submit answer
- `PUT /api/interview/:id/complete` - Complete interview
- `GET /api/interview/:id/phase` - Get current phase

### Progress
- `GET /api/progress` - Get user progress

### Admin (Protected)
- `POST /api/admin/subjects` - Create subject
- `POST /api/admin/problems` - Create problem
- `PUT /api/admin/problems/:id` - Update problem
- `DELETE /api/admin/problems/:id` - Delete problem

## 🔐 Authentication

The application uses JWT (JSON Web Tokens) for authentication. Tokens are stored in localStorage and sent with each request via the Authorization header.

## 🤖 AI Integration

The application uses:
- **Groq API** for fast AI responses in interviews
- **OpenAI API** for additional AI capabilities
- **ElevenLabs** for text-to-speech functionality

## 📊 Database Schema

### User Model
- Email, password (hashed), name
- Role (user/admin)
- Profile information

### Problem Model
- Title, description, difficulty
- Company tags, topics
- Solutions and examples

### Interview Model
- Questions, answers
- Feedback from AI
- Performance metrics

### Progress Model
- Solved problems count
- Topics covered
- Performance stats

## 🐛 Troubleshooting

### MongoDB Connection Error
Ensure MongoDB is running locally or update `MONGO_URI` in `.env` to use MongoDB Atlas.

### Port Already in Use
If ports 5000 or 5173 are in use, update the PORT in `.env` for backend or use `npm run dev -- --port 3000` for frontend.

### CORS Issues
Ensure `CLIENT_URL` in backend `.env` matches your frontend URL.

## 📝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Authors

- **Prem Ngowda** - Initial work

## 🙏 Acknowledgments

- MongoDB for database solutions
- Groq for fast AI inference
- ElevenLabs for text-to-speech
- OpenAI for AI capabilities
- React ecosystem contributors

## 📞 Support

For support, email your-email@example.com or open an issue on GitHub.

---

**Happy Learning! 🎉**
