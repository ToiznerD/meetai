# MeetAI 🤖

A modern AI-powered meeting platform that enables you to create intelligent agents to join and participate in your video meetings. Built with Next.js, Stream Video, and OpenAI integration.

## ✨ Features

### 🤖 AI Agents
- **Custom AI Agents**: Create personalized AI agents with custom instructions
- **Meeting Participation**: Agents can join video calls and interact with participants
- **Intelligent Responses**: Powered by OpenAI's GPT models for natural conversation

### 📹 Video Meetings
- **Real-time Video Calls**: Powered by Stream Video SDK
- **Live Transcription**: Automatic speech-to-text during meetings
- **Meeting Management**: Schedule, join, and manage meetings with ease

### 📊 Meeting Analytics
- **Auto-generated Summaries**: AI-powered meeting summaries with key insights
- **Transcript Processing**: Detailed meeting transcripts with speaker identification
- **Meeting History**: Track all your meetings and their outcomes

### 🔐 Authentication & Security
- **Secure Authentication**: Built with Better Auth
- **User Management**: Complete user account system
- **Session Management**: Secure session handling

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives
- **React Hook Form** - Form handling
- **TanStack Query** - Data fetching and caching

### Backend
- **tRPC** - End-to-end typesafe APIs
- **Drizzle ORM** - Type-safe database queries
- **PostgreSQL** - Primary database (Neon)
- **Inngest** - Background job processing

### AI & Video
- **OpenAI API** - AI agent capabilities
- **Stream Video SDK** - Video calling infrastructure
- **Stream Chat SDK** - Real-time messaging

### Authentication
- **Better Auth** - Modern authentication solution
- **Polar SDK** - Payment and subscription management

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ 
- PostgreSQL database
- OpenAI API key
- Stream Video account
- Stream Chat account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/meetai.git
   cd meetai
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```
   
   Fill in the required environment variables:
   ```env
   # Database
   DATABASE_URL="postgresql://..."
   
   # Authentication
   BETTER_AUTH_SECRET="your-secret-key"
   BETTER_AUTH_URL="http://localhost:3000"
   
   # OpenAI
   OPENAI_API_KEY="your-openai-api-key"
   
   # Stream Video
   NEXT_PUBLIC_STREAM_VIDEO_API_KEY="your-stream-video-key"
   STREAM_VIDEO_SECRET_KEY="your-stream-video-secret"
   
   # Stream Chat
   NEXT_PUBLIC_STREAM_CHAT_API_KEY="your-stream-chat-key"
   STREAM_CHAT_SECRET_KEY="your-stream-chat-secret"
   
   # Inngest
   INNGEST_EVENT_KEY="your-inngest-event-key"
   INNGEST_SIGNING_KEY="your-inngest-signing-key"
   ```

4. **Set up the database**
   ```bash
   npm run db:push
   ```
   *Don't forget to create a database*

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router
│   ├── (auth)/            # Authentication pages
│   ├── (dashboard)/       # Main dashboard pages
│   ├── call/              # Video call pages
│   └── api/               # API routes
├── components/            # Reusable UI components
├── modules/               # Feature modules
│   ├── agents/           # AI agents management
│   ├── meetings/         # Meeting management
│   ├── call/             # Video calling
│   └── auth/             # Authentication
├── db/                   # Database schema and connection
├── lib/                  # Utility libraries
├── trpc/                 # tRPC configuration
└── inngest/              # Background job functions
```

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run db:push` - Push database schema changes
- `npm run db:studio` - Open Drizzle Studio

## 🤖 How AI Agents Work

1. **Create an Agent**: Define your agent's personality and instructions
2. **Schedule a Meeting**: Set up a meeting and assign your agent
3. **Agent Joins**: The AI agent automatically joins the video call
4. **Real-time Interaction**: The agent participates in conversations using OpenAI
5. **Post-meeting Processing**: Automatic transcription and AI-generated summaries

## 🔄 Meeting Lifecycle

1. **Upcoming** - Meeting is scheduled
2. **Active** - Meeting is in progress
3. **Processing** - Meeting ended, generating summary
4. **Completed** - Summary and transcript ready
5. **Cancelled** - Meeting was cancelled

## 🎯 Key Features Explained

### AI Agent Creation
- Custom instructions for agent behavior
- Personality and response style configuration
- Integration with OpenAI's GPT models

### Video Calling
- High-quality video and audio
- Screen sharing capabilities
- Real-time transcription
- Multi-participant support

### Meeting Summaries
- AI-generated overviews
- Key points and action items
- Timestamped sections
- Speaker identification

## 🚀 Deployment

The application is designed to be deployed on Vercel with the following services:

- **Database**: Neon PostgreSQL
- **Video**: Stream Video
- **Background Jobs**: Inngest
- **Authentication**: Better Auth

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [Stream](https://getstream.io/) for video and chat infrastructure
- [OpenAI](https://openai.com/) for AI capabilities
- [Radix UI](https://www.radix-ui.com/) for accessible components
- [Tailwind CSS](https://tailwindcss.com/) for styling

---

Built with ❤️ using modern web technologies
