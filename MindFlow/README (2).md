# MindFlow - AI-Powered Mental Wellness Platform

![MindFlow Banner](https://images.unsplash.com/photo-1559757148-5c350d0d3c56?w=1200&h=400&fit=crop&auto=format)

## 🧠 About MindFlow

MindFlow is an innovative AI-powered mood journal and emotion tracker that helps users understand and improve their mental wellness through intelligent analysis of daily journal entries. Using advanced Natural Language Processing, MindFlow provides real-time emotional insights and beautiful visualizations to help users track their mental health journey.

## 🚀 Live Demo

**🌐 Deployment Link:** [https://xutmvobehyo2w.mocha.app](https://xutmvobehyo2w.mocha.app)

**📊 Pitch Deck:** Available at `/pitch` route or as standalone HTML file

## ✨ Features

### Core Functionality
- **🤖 AI-Powered Analysis**: Advanced sentiment analysis using Hugging Face's RoBERTa model
- **📝 Smart Journaling**: Intuitive writing experience with real-time mood detection
- **📊 Mood Analytics**: Beautiful charts and visualizations of emotional trends
- **🔒 Privacy First**: Secure data handling with user authentication
- **📱 Responsive Design**: Works seamlessly on desktop and mobile devices

### User Experience
- **⚡ Instant Feedback**: Real-time AI analysis of journal entries
- **🎯 Personalized Insights**: Tailored recommendations for mental wellness
- **📈 Progress Tracking**: Long-term mood pattern recognition
- **🔐 Secure Authentication**: Google OAuth integration
- **🌈 Beautiful UI**: Modern design with gradients and smooth animations

## 🛠 Technology Stack

### Frontend
- **React 19** with TypeScript
- **Tailwind CSS** for styling
- **Lucide React** for icons
- **Recharts** for data visualization
- **React Router** for navigation

### Backend
- **Cloudflare Workers** (Hono.js framework)
- **Cloudflare D1** (SQLite database)
- **Zod** for validation
- **Hugging Face API** for sentiment analysis

### Authentication
- **Mocha Users Service** for OAuth
- **Google OAuth** integration

## 🏗 Architecture

```
├── Frontend (React SPA)
│   ├── Landing Page
│   ├── Dashboard
│   ├── Journal Entry Form
│   ├── Mood Visualizations
│   └── Pitch Deck
├── Backend (Cloudflare Worker)
│   ├── API Routes
│   ├── Authentication Middleware
│   ├── AI Sentiment Analysis
│   └── Database Operations
└── Database (Cloudflare D1)
    └── Journal Entries Table
```

## 📊 AI Analysis Features

### Sentiment Analysis
- **Model**: Twitter RoBERTa Base Sentiment (Hugging Face)
- **Outputs**: 
  - Mood score (0-100 scale)
  - Primary emotion detection
  - Confidence levels
  - Personalized insights

### Data Processing
- Real-time text analysis
- Emotion mapping and categorization
- Trend identification over time
- Privacy-preserving processing

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm
- Cloudflare account (for deployment)
- Hugging Face API key

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/mindflow.git
cd mindflow
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up environment variables**
```bash
# Add these secrets to your Cloudflare Worker
HUGGING_FACE_API_KEY=your_hugging_face_api_key
MOCHA_USERS_SERVICE_API_URL=your_mocha_api_url
MOCHA_USERS_SERVICE_API_KEY=your_mocha_api_key
```

4. **Run development server**
```bash
npm run dev
```

5. **Build for production**
```bash
npm run build
```

## 📝 Database Schema

```sql
CREATE TABLE journal_entries (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  user_id TEXT NOT NULL,
  entry_text TEXT NOT NULL,
  mood_score INTEGER,
  primary_emotion TEXT,
  ai_analysis TEXT,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

## 🔄 API Endpoints

### Authentication
- `GET /api/oauth/google/redirect_url` - Get OAuth redirect URL
- `POST /api/sessions` - Create user session
- `GET /api/users/me` - Get current user
- `GET /api/logout` - Logout user

### Journal Entries
- `GET /api/journal-entries` - Get user's journal entries
- `POST /api/journal-entries` - Create new journal entry
- `GET /api/journal-entries/:id` - Get specific journal entry

## 💼 Business Model

### Pricing Tiers
- **Free**: 5 entries/month, basic mood tracking, 7-day history
- **Premium ($4.99/mo)**: Unlimited entries, advanced AI insights, full analytics
- **Enterprise ($50/employee)**: Team analytics, corporate wellness features

### Market Opportunity
- **Market Size**: $5.6B mental health app market
- **Growth Rate**: 23% CAGR
- **Target Users**: 75M adults seeking wellness tools in the US

## 🎯 Key Metrics & Goals

### Phase 1 (Months 1-3): Launch & Validation
- **Target**: 1,000 users
- **Focus**: User feedback and product-market fit

### Phase 2 (Months 4-8): Premium Features
- **Target**: 10,000 users
- **Focus**: Monetization and advanced features

### Phase 3 (Months 9-18): Enterprise Sales
- **Target**: 50,000 users
- **Focus**: B2B partnerships and corporate wellness

### Phase 4 (Months 19-36): Scale & Exit
- **Target**: 100,000+ users
- **Focus**: Market expansion and potential acquisition

## 🔮 Future Enhancements

- **Mobile Apps**: iOS and Android native applications
- **Advanced Analytics**: Detailed mood pattern analysis
- **Integration**: Calendar, fitness trackers, and other wellness apps
- **Community Features**: Anonymous mood sharing and support groups
- **Professional Tools**: Integration with therapists and healthcare providers

## 🤝 Contributing

We welcome contributions! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

- **Email**: hello@mindflow.app
- **Demo**: [https://xutmvobehyo2w.mocha.app](https://xutmvobehyo2w.mocha.app)
- **Pitch Deck**: Available in the app at `/pitch`

## 🙏 Acknowledgments

- **Hugging Face** for sentiment analysis models
- **Cloudflare** for hosting and database services
- **Mocha Platform** for authentication services
- **Unsplash** for beautiful stock photography

---

**Made with ❤️ for better mental wellness**
