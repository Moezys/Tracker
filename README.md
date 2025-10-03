# 📈 Tracker - Real-Time Stock Market Dashboard

A modern, real-time stock market tracking application built with Next.js 15, featuring comprehensive market data visualization, personalized watchlists, intelligent alerts, and AI-powered market news summaries.

![Dashboard Preview](https://ik.imagekit.io/a6fkjou7d/dashboard-preview.png?updatedAt=1756378548102)

## ✨ Features

### 🎯 Core Features
- **Real-Time Market Data**: Live stock prices, charts, and market indicators powered by Finnhub API
- **Interactive Dashboard**: Multiple TradingView widgets including market overview, stock heatmaps, and advanced charts
- **Smart Stock Search**: Intelligent search with autocomplete and popular stock suggestions
- **User Authentication**: Secure sign-up/sign-in with Better Auth and MongoDB integration
- **Responsive Design**: Mobile-first design with dark theme optimization

### 📊 Market Analysis Tools
- **Market Overview Widget**: Track major indices and sector performance
- **Stock Heatmap**: Visual representation of market movements by sector and market cap
- **Advanced Charts**: Candlestick and baseline charts with technical analysis
- **Company Profiles**: Detailed company information and financial metrics
- **Market News**: Real-time market news with AI-powered summaries

### 🔔 Intelligent Notifications (Coming Soon)
- **Price Alerts**: Upper and lower threshold notifications
- **Volume Alerts**: Unusual trading activity detection
- **Daily News Summaries**: Personalized market news delivered via email
- **Email Templates**: Professional, responsive email notifications

### 🎨 Design & User Experience
- **Dark Theme**: Sleek dark interface optimized for extended use
- **Modern UI Components**: Built with Radix UI and styled with Tailwind CSS
- **Smooth Animations**: Enhanced user experience with Tailwind animations
- **Mobile Responsive**: Optimized for all device sizes

## 🛠️ Tech Stack

### Frontend
- **Next.js 15**: React framework with App Router and Turbopack
- **TypeScript**: Type-safe development
- **Tailwind CSS 4**: Utility-first CSS framework
- **Radix UI**: Accessible component primitives
- **TradingView Widgets**: Professional financial charts

### Backend & Database
- **MongoDB**: Document database with Mongoose ODM
- **Better Auth**: Modern authentication solution
- **Inngest**: Background job processing and workflow automation
- **Finnhub API**: Real-time market data provider

### Development Tools
- **ESLint**: Code linting and formatting
- **TypeScript**: Static type checking
- **React Hook Form**: Form state management
- **Lucide React**: Beautiful icons

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/pnpm/yarn
- MongoDB database (local or Atlas)
- Finnhub API key ([Get one here](https://finnhub.io))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Moezys/Tracker.git
   cd real-time-market-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   # or
   yarn install
   ```

3. **Environment Setup**
   Create a `.env.local` file in the root directory:
   ```env
   # Database
   MONGODB_URI=your_mongodb_connection_string
   
   # Authentication
   BETTER_AUTH_SECRET=your_secret_key_here
   BETTER_AUTH_URL=http://localhost:3000
   
   # Market Data API
   FINNHUB_API_KEY=your_finnhub_api_key
   NEXT_PUBLIC_FINNHUB_API_KEY=your_finnhub_api_key
   
   # Email Service (Optional)
   NODEMAILER_EMAIL=your_email@domain.com
   NODEMAILER_PASSWORD=your_app_password
   
   # Inngest (Optional)
   INNGEST_EVENT_KEY=your_inngest_event_key
   INNGEST_SIGNING_KEY=your_inngest_signing_key
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   pnpm dev
   # or
   yarn dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
├── app/                          # Next.js App Router
│   ├── (auth)/                  # Authentication pages
│   │   ├── sign-in/            # Sign in page
│   │   └── sign-up/            # Sign up page
│   ├── (root)/                 # Main application pages
│   │   ├── page.tsx            # Dashboard home
│   │   └── stocks/[symbol]/    # Individual stock pages
│   ├── api/                    # API routes
│   ├── globals.css             # Global styles and custom CSS
│   └── layout.tsx              # Root layout
├── components/                  # Reusable React components
│   ├── ui/                     # Base UI components (Radix UI)
│   ├── forms/                  # Form components
│   ├── Header.tsx              # Navigation header
│   ├── NavItems.tsx            # Navigation menu
│   ├── SearchCommand.tsx       # Stock search component
│   ├── TradingViewWidget.tsx   # Chart widget wrapper
│   ├── UserDropdown.tsx        # User menu
│   └── WatchlistButton.tsx     # Watchlist actions
├── database/                   # Database configuration
│   ├── models/                 # Mongoose models
│   └── mongoose.ts             # Database connection
├── hooks/                      # Custom React hooks
├── lib/                        # Utility functions and configurations
│   ├── actions/                # Server actions
│   ├── better-auth/            # Authentication setup
│   ├── inngest/                # Background jobs
│   ├── nodemailer/             # Email templates
│   ├── constants.ts            # App constants
│   └── utils.ts                # Utility functions
├── middleware/                 # Next.js middleware
├── public/                     # Static assets
│   └── assets/                 # Images and icons
└── types/                      # TypeScript type definitions
```

## 🎯 Key Components

### Authentication System
- **Better Auth Integration**: Modern authentication with email/password
- **User Profiles**: Personalized investment goals and risk tolerance
- **Session Management**: Secure session handling with middleware protection

### Market Data Integration
- **Finnhub API**: Real-time stock data, news, and company information
- **TradingView Widgets**: Professional-grade charts and market visualizations
- **Caching Strategy**: Optimized data fetching with Next.js caching

### Email System
- **Responsive Templates**: Mobile-optimized HTML email templates
- **AI-Generated Content**: Personalized welcome emails and news summaries
- **Alert Notifications**: Price and volume alert emails

### Background Jobs
- **Inngest Integration**: Scheduled tasks and event-driven workflows
- **Daily News Summaries**: Automated email delivery
- **User Onboarding**: Welcome email automation

## 🔧 Configuration

### TradingView Widgets
The app uses multiple TradingView widgets configured in `lib/constants.ts`:
- Market Overview
- Stock Heatmap
- Advanced Charts
- Company Profiles
- Technical Analysis

### Email Templates
Professional email templates are available for:
- Welcome emails
- Daily news summaries
- Price alerts (upper/lower)
- Volume alerts
- User re-engagement

## 📱 Responsive Design

The application is fully responsive with:
- **Mobile-first approach**: Optimized for mobile devices
- **Breakpoint system**: Tailwind CSS responsive utilities
- **Touch-friendly interface**: Enhanced mobile interactions
- **Adaptive layouts**: Components adjust to screen size

## 🎨 Theming

### Dark Theme Design
- **Background**: `#050505` (almost black)
- **Surface**: `#141414` (dark gray)
- **Primary**: `#E8BA40` (golden yellow)
- **Text**: Various gray shades for hierarchy
- **Accents**: Green/red for gains/losses

## 🔮 Future Updates

### Watchlist Features
- ✅ **Add/Remove Stocks**: Personalized stock tracking
- ✅ **Watchlist Management**: Organize and categorize stocks
- ✅ **Real-time Updates**: Live price updates for watchlist items
- ✅ **Performance Tracking**: Monitor gains/losses over time

### Cryptocurrency Support
- 🔄 **Crypto Dashboard**: Bitcoin, Ethereum, and major altcoins
- 🔄 **Crypto Charts**: Price charts and technical analysis
- 🔄 **Market Cap Rankings**: Top cryptocurrencies by market cap
- 🔄 **Crypto News**: Latest cryptocurrency news and updates

### Forex Trading
- 🔄 **Currency Pairs**: Major, minor, and exotic currency pairs
- 🔄 **Forex Charts**: Real-time forex charts and indicators
- 🔄 **Economic Calendar**: Important economic events and announcements
- 🔄 **Currency Converter**: Real-time currency conversion tool

### Enhanced Features
- 🔄 **Portfolio Tracking**: Complete portfolio management
- 🔄 **Advanced Alerts**: Custom alert conditions and notifications
- 🔄 **Social Features**: Share insights and follow other traders
- 🔄 **Mobile App**: Native iOS and Android applications

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Finnhub](https://finnhub.io) for market data API
- [TradingView](https://tradingview.com) for charting widgets
- [Better Auth](https://better-auth.com) for authentication
- [Radix UI](https://radix-ui.com) for accessible components
- [Tailwind CSS](https://tailwindcss.com) for styling

---

**Built with ❤️ by [Moezys](https://github.com/Moezys)**

*Stay ahead of the markets with real-time insights and intelligent alerts.*
