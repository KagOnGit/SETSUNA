# SETSUNA 🌟
**Smart Evaluation & Tracking System for UNiversal Anime**

The next-generation anime database platform designed to revolutionize how we discover, rate, and discuss anime. Built to surpass MyAnimeList and AniList with intelligent recommendations and innovative dual-lens rating system.

## 🎯 Vision

SETSUNA becomes the definitive anime intelligence platform — where casual watchers discover hidden gems through AI-powered taste matching, and hardcore fans contribute to the most sophisticated anime evaluation system ever built.

## ✨ Key Features

### Dual-Lens Rating System
- **Vibe Score**: Emotional impact, rewatchability, personal connection
- **Craft Score**: Animation quality, storytelling, technical execution
- **Combined Intelligence**: Richer discussions and better recommendations

### AI-Powered Recommendations
- **Taste DNA**: Personalized profiles based on rating patterns
- **Context-Aware Suggestions**: Match specific aspects you loved
- **Affinity Matching**: Find users with compatible taste

### Social & Gamification
- **Taste Cards**: Shareable graphics of your anime personality
- **Streak System**: Daily engagement with milestone rewards
- **Badge Collection**: Genre expertise and discovery achievements
- **Discord Integration**: Taste matching with friends

## 🛠 Tech Stack

- **Frontend**: Next.js 14, TypeScript, Tailwind CSS
- **Backend**: Next.js API routes, tRPC for type safety
- **Database**: Supabase (PostgreSQL + Auth + Storage)
- **Vector Search**: pgvector for similarity matching  
- **AI**: OpenAI GPT-4 + embeddings
- **Hosting**: Vercel with auto-scaling

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- pnpm (recommended) or npm
- Supabase account
- OpenAI API key

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/setsuna.git
   cd setsuna
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   # Fill in your API keys and database URLs
   ```

4. **Run database migrations**
   ```bash
   pnpm db:push
   ```

5. **Start development server**
   ```bash
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) to see the app.

## 📁 Project Structure

```
setsuna/
├── src/
│   ├── app/                 # Next.js 14 app directory
│   │   ├── (auth)/         # Auth-protected routes
│   │   ├── anime/          # Anime pages
│   │   ├── profile/        # User profiles
│   │   └── api/            # API routes
│   ├── components/         # Reusable UI components
│   │   ├── ui/            # Base components (shadcn/ui)
│   │   ├── anime/         # Anime-specific components
│   │   └── shared/        # Common components
│   ├── lib/               # Utilities and configurations
│   │   ├── db/           # Database utilities
│   │   ├── ai/           # AI integration helpers
│   │   └── utils/        # General utilities
│   └── types/             # TypeScript type definitions
├── prisma/                # Database schema and migrations
├── public/                # Static assets
└── docs/                  # Documentation and specs
```

## 🧪 Development Workflow

### Available Scripts

```bash
pnpm dev          # Start development server
pnpm build        # Build for production
pnpm start        # Start production server
pnpm lint         # Run ESLint
pnpm type-check   # Run TypeScript checks
pnpm db:push      # Push schema changes to database
pnpm db:seed      # Seed database with sample data
pnpm test         # Run tests
```

### Database Management

```bash
# Generate and apply migrations
pnpm db:generate
pnpm db:push

# Reset database (careful!)
pnpm db:reset

# View database in browser
pnpm db:studio
```

## 📊 Roadmap

### Week 1-2: Foundation
- [x] Project setup and core infrastructure
- [ ] Basic anime database and search
- [ ] User authentication system
- [ ] Responsive UI components

### Week 3-4: Rating System
- [ ] Dual-lens rating interface
- [ ] Taste DNA calculation
- [ ] Basic recommendation engine
- [ ] User profiles and history

### Week 5-6: Social Features
- [ ] Following system
- [ ] Activity feeds
- [ ] Taste affinity matching
- [ ] Shareable Taste Cards

### Week 7-8: AI Enhancement
- [ ] OpenAI integration
- [ ] Vector similarity search
- [ ] Advanced recommendations
- [ ] Content generation tools

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Guidelines
- Use TypeScript for all new code
- Follow the existing code style (Prettier + ESLint)
- Write tests for new features
- Update documentation for API changes

### Commit Convention
```
feat: add new feature
fix: bug fix
docs: documentation changes
style: formatting changes
refactor: code refactoring
test: adding tests
chore: maintenance tasks
```

## 📝 API Documentation

API documentation is auto-generated and available at `/api/docs` when running in development mode.

Key endpoints:
- `/api/trpc/anime` - Anime search and details
- `/api/trpc/ratings` - User ratings CRUD
- `/api/trpc/users` - User profiles and taste data
- `/api/trpc/recommendations` - AI-powered suggestions

## 🔧 Environment Variables

Required environment variables (see `.env.example`):

```bash
# Database
DATABASE_URL="postgresql://..."
SUPABASE_URL="https://..."
SUPABASE_ANON_KEY="..."

# Authentication
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="..."

# AI Services
OPENAI_API_KEY="..."

# External APIs
MAL_CLIENT_ID="..."
ANILIST_CLIENT_ID="..."
```

## 🐛 Issues & Support

- **Bug Reports**: Use GitHub Issues with the `bug` label
- **Feature Requests**: Use GitHub Issues with the `enhancement` label  
- **Questions**: Use GitHub Discussions or Discord

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- MyAnimeList and AniList for inspiration
- The anime community for continuous feedback
- Open source contributors and maintainers

---

**Built with ❤️ for the anime community**

[Website](https://setsuna.app) | [Discord](https://discord.gg/setsuna) | [Twitter](https://twitter.com/setsunaapp)
