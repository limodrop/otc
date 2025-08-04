# Oregon Town Car - Luxury Transportation Service

## Overview

Oregon Town Car is a luxury transportation service application built as a full-stack web application. The system provides a professional online presence for a premium car service company, featuring service information, fleet details, quote requests, contact forms, and testimonials. The application showcases luxury transportation services including airport transfers, corporate travel, special events, and city-to-city rides with a sophisticated, elegant design befitting a high-end service provider.

**Recent Changes (August 2025):**
- Fixed CSS import order issue to resolve build warnings
- Created all component files in proper directory structure
- Updated booking links to use correct URL: https://accounts.oregontowncar.com/
- Fixed TypeScript type errors in storage and form handling
- Implemented complete luxury website with black/gold theme
- Added Mini Coach to fleet (14 passengers, $150/hour)
- Updated contact information with actual business details:
  - Office: 4260 SW 110th Ave, Beaverton, Oregon
  - Email: hello@oregontowncar.com
  - Phone: +1 (503) 353-7755

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **React SPA**: Built with React 18 using TypeScript and functional components with hooks
- **Routing**: Uses Wouter for lightweight client-side routing with a simple home page and 404 fallback
- **Styling**: Tailwind CSS with custom luxury theme colors (gold accents, deep blacks, charcoals) and Shadcn/ui component library
- **Typography**: Google Fonts integration (Playfair Display for headings, Inter for body text) to create an elegant, premium feel
- **State Management**: React Query for server state management and form handling with React Hook Form
- **UI Components**: Comprehensive Shadcn/ui component system providing consistent, accessible interface elements

### Backend Architecture
- **Express.js Server**: RESTful API server with middleware for JSON parsing, CORS, and request logging
- **Storage Layer**: Abstracted storage interface with in-memory implementation (MemStorage) for development, designed to be easily replaceable with database implementation
- **API Endpoints**: RESTful endpoints for quote requests and contact messages with proper validation and error handling
- **Development Setup**: Vite integration for hot module replacement and development server proxy

### Data Storage Solutions
- **Development Storage**: In-memory storage using Map collections for quick development and testing
- **Database Ready**: Drizzle ORM configured for PostgreSQL with schema definitions and migration support
- **Schema Design**: Two main entities - quote requests (customer service inquiries) and contact messages (general inquiries) with proper TypeScript typing

### Validation and Type Safety
- **Zod Schemas**: Runtime validation for API requests using Zod with automatic TypeScript type inference
- **Drizzle Integration**: Type-safe database schema definitions that generate TypeScript types and Zod validation schemas
- **Shared Types**: Common type definitions shared between client and server to ensure consistency

### External Dependencies
- **UI Framework**: Radix UI primitives for accessible, unstyled components
- **Styling**: Tailwind CSS for utility-first styling with PostCSS processing
- **Database**: Configured for Neon Database (PostgreSQL) with connection pooling
- **Development**: Vite for fast development builds and HMR, ESBuild for production builds
- **Forms**: React Hook Form with Zod resolvers for robust form validation
- **Notifications**: Toast notifications for user feedback on form submissions

### Design Patterns
- **Component Composition**: Modular React components with clear separation of concerns
- **Custom Hooks**: Reusable logic extraction (mobile detection, toast notifications)
- **Repository Pattern**: Storage abstraction allowing easy switching between implementations
- **API Abstraction**: Centralized API request handling with consistent error management
- **Responsive Design**: Mobile-first approach with responsive navigation and layouts

The application is structured as a monorepo with clear separation between client, server, and shared code, making it maintainable and scalable for a luxury transportation business.