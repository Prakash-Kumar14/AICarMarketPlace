
# AI Car Marketplace

A full-stack car marketplace built with Next.js, Supabase, Prisma, Tailwind CSS, ArcJet, and Shadcn UI. This project demonstrates modern web development practices, AI integration, and scalable architecture for buying, selling, and managing cars online.

## Features
- Car listing, search, and filtering
- Admin dashboard for managing cars, users, and test drives
- AI-powered car image analysis (Gemini AI)
- User authentication (Clerk)
- Test drive booking and management
- Saved cars and reservations
- Supabase storage for car images
- Row Level Security (RLS) policies for data protection
- Responsive UI with Shadcn and Tailwind CSS

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/ai-car-marketplace.git
cd ai-car-marketplace
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
Create a `.env` file in the root directory with the following variables:

```env
# Connect to Supabase via connection pooling
DATABASE_URL=

# Direct connection to the database. Used for migrations
DIRECT_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

GEMINI_API_KEY=
ARCJET_KEY=

NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
```

Fill in the values from your Supabase, Clerk, and Gemini AI accounts.

### 4. Set up the database
Run Prisma migrations to create the database tables:
```bash
npx prisma migrate dev
```

### 5. Start the development server
```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to view the app.

## Supabase Configuration
- Enable Row Level Security (RLS) and add policies for your tables and storage buckets.
- Create a `car-images` storage bucket for car image uploads.

## Folder Structure
- `app/` - Next.js app directory (routes, pages, layouts)
- `actions/` - Server actions for business logic
- `components/` - UI components
- `hooks/` - Custom React hooks
- `lib/` - Utility libraries (Prisma, Supabase, helpers)
- `prisma/` - Prisma schema and migrations
- `public/` - Static assets and images

## Technologies Used
- Next.js
- Supabase
- Prisma
- Tailwind CSS
- Shadcn UI
- Clerk (auth)
- Gemini AI
- ArcJet

## License
MIT

---
For more details, see the code and comments in each folder. Contributions welcome!
