# WorkWave

WorkWave is a comprehensive job portal platform designed to connect employers and job seekers seamlessly. Employers can post job listings, and job seekers can browse and apply for jobs that match their skills and preferences.

---
## Screenshots of website : 

![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20001547.png)
![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20002559.png)
![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20002607.png)
![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20002619.png)
![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20001547.png)
![Screenshots](https://github.com/arpit2212/Work-Wave/blob/master/public/companies/Screenshot%202024-12-07%20002634.png)


## Features

### For Employers:
- Post job openings with detailed descriptions.
- Manage and edit job listings.
- Review applications from candidates.

### For Job Seekers:
- Create a user profile with skills, experience, and resume.
- Search for jobs based on filters like location, role, and industry.
- Apply for jobs with a single click.
- Track application statuses.

### Additional Features:
- User-friendly interface for intuitive navigation.
- Secure authentication for both employers and job seekers.
- Notifications for new job postings and application updates.

---

## Tech Stack

- **Frontend**: [React](https://reactjs.org/) with [Vite](https://vitejs.dev/)
- **UI Framework**: [ShadCN](https://shadcn.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Authentication**: [Clerk.js](https://clerk.dev/)
- **Database**: [Supabase](https://supabase.com/)
- **Hosting**: [Vercel](https://vercel.com/) (Frontend), [Supabase](https://supabase.com/) (Backend)

---

## Installation

### Prerequisites

Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v16+)
- [Vite](https://vitejs.dev/)
- A Supabase account

---

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/workwave.git
   cd workwave


2. Install dependencies:

bash
Copy code
npm install


3. Set up environment variables:

Create a .env file in the root directory.

Add the following variables:

env
Copy code
VITE_SUPABASE_URL=<Your Supabase Project URL>
VITE_SUPABASE_ANON_KEY=<Your Supabase Public Anon Key>
VITE_CLERK_FRONTEND_API=<Your Clerk Frontend API Key>
VITE_CLERK_JWT_KEY=<Your Clerk JWT Key>
To retrieve these keys:

Supabase: Go to your Supabase Dashboard and copy the Project URL and Anon Key from the API Settings page.
Clerk.js: Access the API keys from the Clerk Dashboard under the project's API settings.

4. Start the development server:

bash
Copy code
npm run dev

Access the application: Open your browser and navigate to http://localhost:5173.

Folder Structure
bash
Copy code
workwave/
├── src/
│   ├── components/     # Reusable components
│   ├── pages/          # Page-level components
│   ├── styles/         # Styling files
│   ├── utils/          # Utility functions
│   └── services/       # API service handlers
├── backend/
│   ├── models/         # Database models
│   ├── routes/         # API endpoints
│   ├── controllers/    # Business logic
│   └── middleware/     # Authentication and validation
└── README.md

Setting up Supabase

Create a new project on Supabase.


Happy coding! 🚀