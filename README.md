# Event Splash - Event Registration System

Event registration system built with React, TypeScript, Supabase, and Tailwind CSS. Students can browse events and manage their registrations.

## Features

- **Authentication**: Email/password via Supabase Auth
- **Event Management**: Create, view, and manage events
- **Registrations**: Capacity-aware registration with status tracking
- **Dashboard**: View your registered events
- **Responsive UI**: Mobile, tablet, and desktop

## Technology Stack

- **Frontend**: React 18 + TypeScript + Vite
- **Styling**: Tailwind CSS with custom gradient designs
- **Backend**: Supabase (Database + Authentication + Real-time)
- **Database**: PostgreSQL with Row Level Security (RLS)
- **Icons**: Lucide React
- **Deployment**: Ready for GitHub deployment

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd event-registration-system
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up Supabase**
   - Create a new project at [supabase.com](https://supabase.com)
   - Copy your project URL and anon key
   - Create a `.env` file from `.env.example`
   - Add your Supabase credentials

4. **Run database migrations**
   - Go to your Supabase dashboard → SQL Editor
   - Copy and run the migration from `supabase/migrations/create_events_system.sql`

5. **Start the development server**
   ```bash
   npm run dev
   ```

## Database Schema

### Events Table
- **id**: Unique identifier
- **title**: Event name
- **description**: Event details
- **date**: Event date
- **time**: Event time
- **location**: Venue information
- **capacity**: Maximum participants
- **registered_count**: Current registrations
- **category**: Event type
- **organizer**: Organization name
- **image_url**: Optional event image

### Registrations Table
- **id**: Unique identifier
- **event_id**: Reference to event
- **user_id**: Reference to user
- **registered_at**: Registration timestamp
- **status**: Registration status

## Key Features

### For Students:
- Browse upcoming events with detailed information
- Register for events with real-time availability checking
- Personal dashboard to manage registrations
- Cancel registrations before event dates
- Responsive design for all devices

### For Event Organizers:
- Create new events with comprehensive details
- Set event capacity and manage registrations
- Upload event images and categorize events
- Track registration counts in real-time

### Security Features:
- Row Level Security (RLS) for data protection
- User authentication required for all actions
- Users can only manage their own registrations
- Event creators can manage their events

## Design Notes

- **Modern Gradient UI**: Beautiful blue-to-purple gradients
- **Smooth Animations**: Hover effects and transitions
- **Card-based Layout**: Clean, organized information display
- **Mobile-first Design**: Optimized for all screen sizes
- **Loading States**: Visual feedback for user actions
- **Status Indicators**: Clear registration and availability status

## Responsive Breakpoints

- **Mobile**: < 768px (Stack layout, bottom navigation)
- **Tablet**: 768px - 1024px (2-column grid)
- **Desktop**: > 1024px (3-column grid, full features)

## Deployment

### Easy GitHub Deployment

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Deploy to Vercel/Netlify**
   - Connect your GitHub repository
   - Add environment variables
   - Deploy automatically

3. **Set up Supabase**
   - Ensure RLS policies are enabled
   - Configure authentication settings
   - Update CORS settings for your domain

### Environment Variables for Deployment
```
VITE_SUPABASE_URL=your_production_supabase_url
VITE_SUPABASE_ANON_KEY=your_production_supabase_anon_key
```

## Sample Data

The system includes sample events to demonstrate functionality:
- Guest Lecture: Modern Development Practices
- Annual Sports Festival
- Cultural Night 2024
- Web Development Workshop

## Development

### Available Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Project Structure
```
src/
├── components/          # React components
├── contexts/           # React contexts (Auth)
├── lib/               # Utility functions (Supabase client)
├── types/             # TypeScript type definitions
└── App.tsx            # Main application component
```

## Security Considerations

- All database operations use Row Level Security
- User authentication required for sensitive actions
- Input validation on both client and server
- CORS properly configured for production
- Environment variables for sensitive data

## Support

For questions or issues:
1. Check the documentation
2. Review the database migration file
3. Ensure Supabase is properly configured
4. Verify environment variables are set correctly

## Future Enhancements

- Email notifications for event reminders
- Event categories with filtering
- Admin panel for user management
- Event analytics and reporting
- QR code generation for events
- Integration with calendar apps

---

Built with React, TypeScript, Supabase, and Tailwind CSS.