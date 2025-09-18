# 🚀 SmartTeam Coach - AI Sports Analysis Platform

A modern, AI-powered web application for comprehensive sports team analysis and player performance evaluation, built with cutting-edge technologies for real-time insights and intelligent recommendations.

## ✨ Features

### 🏃‍♂️ Player Management
- **Complete Player Profiles**: Detailed player information including performance metrics, physical condition, and emotional state
- **Real-time Analysis**: Instant AI-powered classification and performance evaluation
- **Advanced Filtering**: Search and filter players by position, performance, and other criteria

### 🤖 AI-Powered Analysis
- **Machine Learning Classification**: Automatic categorization of players based on performance data
- **Intelligent Recommendations**: Personalized training and development suggestions
- **Performance Prediction**: Data-driven insights for player potential and growth

### 📊 Team Analytics
- **Comprehensive Dashboard**: Visual representation of team performance metrics
- **Comparative Analysis**: Side-by-side player and team comparisons
- **Strategic Insights**: Data-driven recommendations for team composition and strategy

### 🎨 Modern Web Interface
- **Responsive Design**: Optimized for desktop and mobile devices
- **Real-time Updates**: Live data synchronization with Socket.IO
- **Intuitive UX**: Clean, professional interface with smooth animations

## 🛠️ Technology Stack

### 🎯 Core Framework
- **⚡ Next.js 15** - The React framework for production with App Router
- **📘 TypeScript 5** - Type-safe JavaScript for better developer experience
- **🎨 Tailwind CSS 4** - Utility-first CSS framework for rapid UI development

### 🧩 UI Components & Styling
- **🧩 shadcn/ui** - High-quality, accessible components built on Radix UI
- **🎯 Lucide React** - Beautiful & consistent icon library
- **🌈 Framer Motion** - Production-ready motion library for React
- **🎨 Next Themes** - Perfect dark mode in 2 lines of code

### 📋 Forms & Validation
- **🎣 React Hook Form** - Performant forms with easy validation
- **✅ Zod** - TypeScript-first schema validation

### 🔄 State Management & Data Fetching
- **🐻 Zustand** - Simple, scalable state management
- **🔄 TanStack Query** - Powerful data synchronization for React
- **🌐 Axios** - Promise-based HTTP client

### 🗄️ Database & Backend
- **🗄️ Prisma** - Next-generation Node.js and TypeScript ORM
- **🔐 NextAuth.js** - Complete open-source authentication solution
- **🔌 Socket.IO** - Real-time bidirectional communication

### 🎨 Advanced Features
- **📊 TanStack Table** - Headless UI for building tables and datagrids
- **🖱️ DND Kit** - Modern drag and drop toolkit for React
- **📊 Recharts** - Redefined chart library built with React and D3
- **🖼️ Sharp** - High performance image processing

### 🌍 Internationalization & Utilities
- **🌍 Next Intl** - Internationalization library for Next.js
- **📅 Date-fns** - Modern JavaScript date utility library
- **🪝 ReactUse** - Collection of essential React hooks for modern development

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Database (SQLite for development, PostgreSQL for production)

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd workspace-SmartTeamCoach

# Install dependencies
npm install

# Set up the database
npm run db:generate
npm run db:push

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the application running.

## 📁 Project Structure

```
src/
├── app/                 # Next.js App Router pages and API routes
│   ├── api/            # API endpoints
│   ├── globals.css     # Global styles
│   └── layout.tsx      # Root layout
├── components/         # Reusable React components
│   ├── ui/            # shadcn/ui components
│   ├── analysis/      # Player analysis components
│   ├── dashboard/     # Dashboard components
│   ├── strategies/    # Strategy generation components
│   └── training/      # Training planner components
├── hooks/             # Custom React hooks
├── lib/               # Utility functions and configurations
│   ├── db.ts          # Database configuration
│   ├── socket.ts      # Socket.IO configuration
│   └── utils.ts       # Utility functions
└── types/             # TypeScript type definitions
```

## 🎯 Available Scripts

```bash
# Development
npm run dev          # Start development server with hot reload
npm run build        # Build for production
npm run start        # Start production server

# Database
npm run db:generate  # Generate Prisma client
npm run db:push      # Push schema changes to database
npm run db:migrate   # Create and run database migrations
npm run db:reset     # Reset database (development only)

# Code Quality
npm run lint         # Run ESLint for code linting
```

## 🔧 Configuration

### Environment Variables

Create a `.env.local` file in the root directory:

```env
# Database
DATABASE_URL="file:./db/custom.db"

# NextAuth.js
NEXTAUTH_SECRET="your-secret-key"
NEXTAUTH_URL="http://localhost:3000"

# API Keys (if needed)
# Add your API keys here
```

### Database Setup

The application uses Prisma with SQLite for development:

```bash
# Generate Prisma client
npm run db:generate

# Push schema to database
npm run db:push

# (Optional) Create migration
npm run db:migrate
```

## 🤖 AI Features

### Player Classification
- **Input**: Performance metrics, physical condition, age, experience
- **Output**: Player category (High Performance, Balanced, Development Needed, etc.)
- **Algorithm**: Machine learning model trained on sports performance data

### Recommendation Engine
- **Personalized Suggestions**: Training plans, skill development focus
- **Context-Aware**: Considers player's current state and goals
- **Actionable Insights**: Specific, implementable recommendations

### Team Analysis
- **Aggregate Metrics**: Team-wide performance statistics
- **Player Comparisons**: Relative strengths and weaknesses
- **Strategic Planning**: Data-driven team composition recommendations

## 📊 Data Models

### Player
```typescript
{
  id: string;
  name: string;
  position: string;
  age: number;
  performance: {
    offensive: number;    // 1-10 scale
    defensive: number;    // 1-10 scale
  };
  physicalCondition: string;
  emotionalState: string;
  minutesPlayed: number;
  // ... additional fields
}
```

### Analysis Result
```typescript
{
  category: string;
  confidence: number;
  recommendations: string[];
  strengths: string[];
  weaknesses: string[];
  developmentPlan: string[];
}
```

## 🔐 Authentication

The application includes NextAuth.js for secure authentication:

- **Providers**: Email/password, OAuth (configurable)
- **Sessions**: JWT-based session management
- **API Protection**: Route-level authentication guards

## 🌐 Real-time Features

- **Live Updates**: Real-time data synchronization
- **WebSocket Communication**: Bidirectional client-server communication
- **Live Analysis**: Instant feedback on player data changes

## 📱 Responsive Design

- **Mobile-First**: Optimized for mobile devices
- **Tablet Support**: Adaptive layouts for tablets
- **Desktop Enhancement**: Full feature set on desktop

## 🧪 Testing

```bash
# Run tests (when implemented)
npm run test

# Run tests with coverage
npm run test:coverage
```

## 🚀 Deployment

### Production Build
```bash
npm run build
npm run start
```

### Environment Setup
- Set `NODE_ENV=production`
- Configure production database
- Set up proper environment variables
- Enable authentication providers

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- UI components from [shadcn/ui](https://ui.shadcn.com/)
- Icons from [Lucide React](https://lucide.dev/)
- Database ORM by [Prisma](https://prisma.io/)

---

**SmartTeam Coach** - Empowering sports teams with AI-driven insights for better performance and strategic decision-making. 🏆
