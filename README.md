# Spatz-2 - Advanced Fullstack Svelte Template

An enhanced fullstack template built with Svelte 5, featuring advanced form handling, payment integration, and modern UI components.

## Tech Stack

- **SvelteKit 5** - Modern fullstack web framework
- **PocketBase** - Backend with authentication and database
- **OpenAI** - AI chatbot functionality
- **TailwindCSS** - Utility-first styling
- **shadcn-svelte** - Modern UI components
- **svelte-superforms** - Advanced form handling
- **Zod** - Schema validation
- **Stripe** - Payment processing

## Features

- **User Authentication** - Complete auth system with PocketBase
- **User Profile Management** - Client-side profile and settings
- **Payment Integration** - Stripe subscriptions and payments
- **AI Chatbot** - OpenAI-powered conversational interface
- **Advanced Forms** - svelte-superforms with Zod validation
- **Modern UI** - shadcn-svelte components and animations
- **Theme Support** - Dark/light mode switching
- **Command Palette** - Quick navigation with CMD+j
- **Guestbook** - User interaction system
- **Admin Dashboard** - PocketBase admin interface

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- PocketBase (download from pocketbase.io)
- pnpm package manager

### Installation

1. **PocketBase Setup:**
```bash
# Download and extract PocketBase
# Start PocketBase server
./pocketbase serve --http="0.0.0.0:8090"
```

2. **Client Setup:**
```bash
git clone <repository-url>
cd spatz-2
pnpm install
cp .env.example .env.local
# Edit .env.local with your configuration
pnpm run dev
```

3. Access the application at `http://localhost:5173`

### Environment Variables

Create a `.env.local` file with:
```env
PUBLIC_POCKETBASE_URL=http://localhost:8090
# Add other required environment variables
```

## Development

### Project Structure

```
/src
├── /lib
│   ├── /schema.ts (Zod schema)
│   └── app.d.ts (global types)
├── /assets
│   └── /images
├── /components
│   ├── /magic-ui (svelte-animations)
│   └── /ui (shared components)
├── /stores (global state)
├── /routes
│   │
│   ├── /notifications
│   ├── /privacy
│   ├── /subscriptions
│   ├── /technologies
│   ├── /terms
│   │
│   ├── /guestbook
│   │   └── /post
│   │       └── /[id]
│   ├── /users
│   │   └── /[id]
│   │
│   ├── /ai
│   │   ├── /chat
│   │   ├── /context
│   │   ├── /image-gen
│   │   └── /agent (n8n Workflow)
│   │
│   ├── /donate
│   │   ├── /cancel (redirect when cancelling stripe payment)
│   │   └── /success (redirect after successful stripe payment)
│   │
│   ├── /checkout
│   │   ├── /payment (redirect when cancelling stripe payment)
│   │   ├── /cancel (redirect when cancelling stripe payment)
│   │   └── /success (redirect after successful stripe payment)
│   │
│   ├── /api
│   │   ├── /chat (OpenAI streaming API)
│   │   ├── /donate (for stripe payments)
│   │   ├── /fortune (fetch random tech founder quote)
│   │   ├── /image-gen (OpenAI DALL-E)
│   │   ├── /agent (n8n Workflow)
│   │   ├── /repo-data
│   │
│   │__ /auth (Pocketbase auth)
│   │   ├── /login
│   │   ├── /register
│   │   ├── /logout
│   │   └── /reset-password
│   │
│   └── /my (user-specific routes)
│       └── /settings
│           ├── /account
│           ├── /profile
│           ├── /security (for password management)
│           └── /subscription (existing stripe subscriptions)
/pocketbase
├── pb_schema.json
/static
└── /docs (general documentation)

```

## Development

### Project Structure

```
/src
├── /lib
│   ├── /schema.ts (Zod schema)
│   └── app.d.ts (global types)
├── /assets
│   └── /images
├── /components
│   ├── /magic-ui (animations)
│   └── /ui (shared components)
├── /stores (global state)
├── /routes
│   ├── /guestbook
│   ├── /ai (nested routes)
│   ├── /api
│   └── /my (user-specific routes)
```

### Additional Features

- **Icons**: Provided by Iconify/Svelte with searchable icon library
- **Animations**: GSAP-powered animations for smooth interactions
- **Payments**: Stripe integration for subscription management

## Deployment

The application can be deployed to Vercel, Netlify, or any other hosting platform that supports SvelteKit applications.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests to improve the template.
