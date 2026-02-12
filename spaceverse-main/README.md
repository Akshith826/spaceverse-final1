# Spaceverse Final 🚀

An interactive 3D educational platform for exploring our Solar System with authentication, quizzes, user reviews, and an AI-powered Space Traffic Simulator.

## Features ✨

- **🌍 3D Solar System Explorer**: Interactive 3D models of all planets with realistic textures and orbital mechanics
- **🥽 VR Solar System Explorer**: Immerse yourself in the solar system with WebXR-based virtual reality
- **🔐 User Authentication**: Secure registration and login system with session management
- **🧠 Interactive Quiz System**: Educational quizzes about each planet with score tracking
- **⭐ Review System**: Users can rate and review their experience with the platform
- **🚀 AI-Powered Space Traffic Simulator**: Create hypothetical space scenarios and visualize their impact on orbital congestion, collision risk, and sustainability
- **🔮 Advanced AI Integration**: Real-time predictive analytics and personalized recommendations
- **👥 Social Features**: Community scenario sharing, likes, comments, and user reviews
- **🤖 Space Chatbot**: Ask questions about space in plain English and get informative answers
- **🎨 Modern Interface Design**: Enhanced UI/UX with animations, transitions, and contemporary aesthetics
- **📱 Responsive Design**: Works seamlessly across desktop and mobile devices
- **🎵 Immersive Audio**: Background music for enhanced user experience

## Technologies Used 🛠️

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: Express-session, bcryptjs
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **3D Graphics**: Three.js for 3D planet models and animations
- **VR Technology**: WebXR, @react-three/fiber, @react-three/xr for immersive virtual reality
- **AI Service**: Python, FastAPI, scikit-learn
- **Security**: Rate limiting, input validation, profanity filtering

## Installation & Setup 🔧

1. **Clone the repository**
   ```bash
   git clone https://github.com/karthikguntoju/spaceverse
   cd Spaceverse_final
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Install AI service dependencies**
   ```bash
   cd ai-service
   pip install -r requirements.txt
   cd ..
   ```

4. **Environment Setup**
   - Copy `.env.example` to `.env`
   - Add your MongoDB connection string to `MONGODB_URI` in `.env`

## Quick Start ⚡

For the easiest way to start the complete system, use the single-command approach:

```bash
npm run start-all
```

This will automatically start:
- MongoDB (if not already running)
- The AI Service (on port 8001)
- The main Spaceverse application (on port 5002+)

✅ **AI Services Status: Working**

**Note**: If the AI service fails to start due to missing Python dependencies, you can either:
1. Install the dependencies manually: `cd ai-service && pip install -r requirements.txt`
2. Or continue using the application without AI features (some simulator features will be limited)

5. **Start the application**
   ```bash
   # Option 1: Start all services with one command (recommended)
   npm run start-all
   
   # Option 2: Manual start (traditional method)
   # Terminal 1: Start the main application
   npm start
   
   # Terminal 2: Start the AI service
   cd ai-service
   python ai_service.py
   ```

6. **Access the application**
   - Open your browser and navigate to `http://localhost:5002`
   - The AI service will be running on `http://localhost:8001`
   - When using the single-command startup, both services will be managed automatically

## Project Structure 📁

```
Spaceverse_final/
├── config/
│   └── auth.js              # Authentication middleware
├── models/
│   └── review.js            # Review data model
├── routes/
│   ├── reviews.js           # Review API routes
│   └── simulator.js         # Space Traffic Simulator API routes
├── views/
│   ├── home.html            # Landing page with auth
│   ├── about.html           # About page with reviews
│   ├── solar-system.html    # 3D solar system explorer
│   ├── quiz.html            # Interactive quiz system
│   ├── space-traffic-simulator.html  # Space Traffic Simulator UI
│   ├── space-traffic-visualization.html  # 3D space traffic visualization
│   ├── community-scenarios.html      # Community scenarios browser
│   └── reviews.html         # Community reviews page
├── public/
│   ├── textures/            # Planet textures
│   ├── markers/             # AR markers
│   └── audio/               # Background music
├── images/                  # Planet images
├── models/                  # 3D planet models (.glb files)
├── ai-service/              # AI microservice for space traffic analysis
│   ├── ai_service.py        # AI service implementation
│   ├── requirements.txt     # Python dependencies
│   └── Dockerfile           # Containerization
├── app-enhanced.js          # Main application server
└── package.json             # Project dependencies
```

## Features in Detail 🌟

### 3D Solar System Explorer
- Realistic planet models with accurate textures
- Interactive orbital mechanics
- Click on planets for detailed information
- Smooth camera controls and navigation

### Authentication System
- Secure user registration and login
- Session-based authentication
- Password hashing with bcryptjs
- Protected routes for authenticated users

### Quiz System
- Planet-specific quiz questions
- Score tracking and progress saving
- Multiple choice questions with instant feedback
- Educational content for all age groups

### Review System
- Star rating system (1-5 stars)
- Comment submission with profanity filtering
- User authentication required for reviews
- Real-time review display

### Community Features
- Share space traffic scenarios with the community
- Like and comment on community scenarios
- Browse community-created simulations
- Participate in collaborative learning

### Advanced AI Features
- Real-time predictive analytics for space traffic
- Personalized recommendations based on user history
- Environmental factor integration (space weather, asteroids)
- Skill-level adaptive guidance

## API Endpoints 🔌

- `POST /api/register` - User registration
- `POST /api/login` - User login
- `POST /api/logout` - User logout
- `GET /api/user` - Get current user status
- `GET /api/reviews` - Get all approved reviews
- `POST /api/reviews` - Submit a new review (authenticated)
- `GET /api/planets` - Get planet data
- `GET /api/ephemeris` - Get current planet positions
- `GET /vr-solar-system` - Access the VR solar system explorer
- `POST /api/simulator/run` - Run a space traffic simulation (authenticated)
- `GET /api/simulator/:id` - Get a specific simulation (authenticated)
- `GET /api/simulator/history` - Get user's simulation history (authenticated)
- `GET /api/simulator/scores` - Get user's gamification scores (authenticated)
- `GET /api/simulator/leaderboard` - Get leaderboard (authenticated)
- `POST /api/simulator/real-time-prediction` - Get real-time AI predictions (authenticated)
- `POST /api/simulator/personalized-recommendations` - Get personalized recommendations (authenticated)
- `POST /api/simulator/share-scenario` - Share a scenario with the community (authenticated)
- `GET /api/simulator/community-scenarios` - Get community scenarios (authenticated)
- `POST /api/simulator/like-scenario/:id` - Like/unlike a scenario (authenticated)
- `POST /api/simulator/comment-scenario/:id` - Comment on a scenario (authenticated)
- `POST /api/simulator/chatbot` - Ask questions about space and get informative answers (authenticated)

## Contributing 🤝

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Acknowledgments 🙏

- NASA for planetary data and textures
- Three.js community for 3D graphics support
- MongoDB for database solutions
- Express.js for web framework

---

**🌌 Explore the cosmos with Spaceverse - Where learning meets adventure!**
