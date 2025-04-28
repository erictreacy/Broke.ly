# Broke.ly

![Broke.ly Logo](https://placeholder.svg?height=100&width=100&query=B)

> Where your money goes to die.

Broke.ly is a personal finance budgeting application that helps you track, manage, and visualize your spending habits. With a touch of humor and practicality, Broke.ly makes the painful process of budgeting slightly less painful.

## Features

- **User Authentication**: Secure signup and login functionality
- **Dashboard**: Overview of your financial situation at a glance
- **Budget Management**: Create and manage budgets for different categories
- **Transaction Tracking**: Log and categorize your income and expenses
- **Reports**: Visualize your spending patterns with charts and graphs
- **Calendar View**: See your financial events in a calendar format
- **Account Linking**: Connect to external payment services (Venmo, PayPal, etc.)
- **Settings**: Customize your experience with various preferences

## Tech Stack

- **Frontend**: Next.js 14 (App Router), React
- **Styling**: Tailwind CSS, shadcn/ui components
- **Authentication & Database**: Supabase
- **Form Handling**: React Hook Form with Zod validation

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Supabase account

### Environment Setup

Create a `.env.local` file in the root directory with the following variables:

\`\`\`
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
\`\`\`

### Installation

1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/yourusername/brokely.git
   cd brokely
   \`\`\`

2. Install dependencies:
   \`\`\`bash
   npm install
   # or
   yarn install
   \`\`\`

3. Run the development server:
   \`\`\`bash
   npm run dev
   # or
   yarn dev
   \`\`\`

4. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Supabase Setup

### Database Schema

Set up the following tables in your Supabase project:

1. **profiles** - User profile information
2. **accounts** - Financial accounts (checking, savings, credit cards)
3. **categories** - Transaction categories
4. **transactions** - Financial transactions
5. **budgets** - Budget allocations by category

### Authentication

Broke.ly uses Supabase Authentication with email/password login. Make sure to:

1. Enable Email auth provider in Supabase Auth settings
2. Configure email templates if needed
3. Set up appropriate redirect URLs

## Project Structure

\`\`\`
broke.ly/
├── app/                  # Next.js App Router
│   ├── auth-test/        # Authentication diagnostic tool
│   ├── dashboard/        # Dashboard pages
│   ├── login/            # Login page
│   ├── signup/           # Signup page
│   ├── settings/         # Settings pages
│   └── layout.tsx        # Root layout
├── components/           # Reusable React components
│   ├── ui/               # shadcn/ui components
│   └── logo.tsx          # Logo component
├── lib/                  # Utility functions
│   ├── supabase.ts       # Supabase client for client components
│   └── supabase-server.ts # Supabase client for server components
├── middleware.ts         # Next.js middleware for auth
└── public/               # Static assets
\`\`\`

## Authentication Flow

1. Users sign up with email and password
2. Email verification (optional)
3. Login with credentials
4. Session management via Supabase Auth
5. Protected routes via middleware

## Troubleshooting

If you encounter authentication issues:

1. Check that your Supabase environment variables are correctly set
2. Run the authentication diagnostic tool at `/auth-test`
3. Verify that cookies are being properly set
4. Check browser console for any errors

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Next.js](https://nextjs.org/)
- [Supabase](https://supabase.io/)
- [shadcn/ui](https://ui.shadcn.com/)
- [Tailwind CSS](https://tailwindcss.com/)

---

Built with 💸 and 😭 by the Broke.ly team
