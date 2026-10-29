TRUSTLOS PRODUCT WEBSITE + USER PORTAL
======================================

This is a responsive marketing/product website concept for a Loan Origination System (LOS), including registration, login, password reset request, user profile editing, and Supabase database storage.

FILES
- index.html: product landing page, feature sections, account forms and profile screen
- style.css: responsive styling for desktop and mobile
- app.js: Supabase authentication and profile persistence
- supabase-schema.sql: profile table, row-level security policies, and profile creation trigger

IMPORTANT: This is a starter project, not a deployed live website. Authentication/database functions require your own Supabase project configuration.

SETUP
1. Create a project at https://supabase.com.
2. In Supabase Dashboard > SQL Editor, run all SQL in supabase-schema.sql.
3. In Supabase Project Settings > API / API Keys, copy the Project URL and public anon/publishable key.
4. Edit app.js and replace the placeholders:
   const SUPABASE_URL = "YOUR_SUPABASE_PROJECT_URL";
   const SUPABASE_ANON_KEY = "YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY";
5. Never put a service_role key, database password, or secret key in app.js.
6. In Supabase Authentication settings, configure email confirmation and allowed redirect URLs. Add your eventual GitHub Pages URL.
7. Create a GitHub repository and upload index.html, style.css, app.js, supabase-schema.sql and README.txt to its root.
8. In GitHub repository Settings > Pages, publish from the main branch and /(root).
9. Test with two separate test accounts. Confirm each account can only read/update its own profile.

FEATURES
- LOS product overview and landing page
- Feature sections: application management, workflow visibility, document coordination, integration-ready design
- Responsive dashboard mockup (illustrative, not live loan data)
- Email/password registration and login through Supabase Auth
- Password reset email request
- User profile: full name, company, phone, job title and short bio
- PostgreSQL profile persistence
- Row Level Security (RLS) policies limiting profile access to the authenticated owner

SECURITY / PRODUCTION NOTES
- The Supabase public anon/publishable key may be used in browser code only when Row Level Security is enabled and policies are correctly configured.
- Do not expose service-role/secret keys.
- This marketing site does not yet implement a live loan application workflow, AI chatbot, admin dashboard, billing, or production support operations. The dashboard in the hero is an illustrative mockup.
- Before production, review privacy notices, terms, cookie practices, abuse protection, logging, accessibility, backups, email delivery, and data-retention rules.
- Do not collect sensitive financial documents, government IDs, or real borrower data in this starter without a proper security and compliance review.
