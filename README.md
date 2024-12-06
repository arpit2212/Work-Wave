# WorkWave

WorkWave is a comprehensive job portal platform designed to connect employers and job seekers seamlessly. Employers can post job listings, and job seekers can browse and apply for jobs that match their skills and preferences.

---

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

- **Frontend**: [React.js](https://reactjs.org/), [Tailwind CSS](https://tailwindcss.com/)
- **Backend**: [Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/)
- **Database**: [Supabase](https://supabase.com/)
- **Authentication**: [Supabase Auth](https://supabase.com/auth)
- **Hosting**: [Vercel](https://vercel.com/) (Frontend), [Supabase](https://supabase.com/) (Backend)
- **Other Tools**: REST APIs, Git, CI/CD pipelines

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/workwave.git
   cd workwave
Install dependencies:

bash
Copy code
npm install
Set up environment variables:

Create a .env file in the root directory.

Add the following variables:

env
Copy code
NEXT_PUBLIC_SUPABASE_URL=<Your Supabase Project URL>
NEXT_PUBLIC_SUPABASE_ANON_KEY=<Your Supabase Public Anon Key>
SUPABASE_SERVICE_KEY=<Your Supabase Service Role Key>
NODE_ENV=development
To get these keys:

Go to your Supabase Dashboard.
Copy the Project URL and Anon Key from the API Settings page.
Copy the Service Role Key from the Settings > API > Service Role section.
Start the development server:

bash
Copy code
npm run dev
Access the application: Open your browser and navigate to http://localhost:3000.

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
Go to the SQL editor and set up the following tables:
users
sql
Copy code
CREATE TABLE users (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  name TEXT NOT NULL,
  role TEXT CHECK (role IN ('employer', 'job_seeker')) NOT NULL,
  created_at TIMESTAMP DEFAULT now()
);
jobs
sql
Copy code
CREATE TABLE jobs (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  title TEXT NOT NULL,
  description TEXT,
  company_name TEXT NOT NULL,
  location TEXT,
  posted_by UUID REFERENCES users(id) ON DELETE CASCADE,
  created_at TIMESTAMP DEFAULT now()
);
applications
sql
Copy code
CREATE TABLE applications (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  job_id UUID REFERENCES jobs(id) ON DELETE CASCADE,
  applicant_id UUID REFERENCES users(id) ON DELETE CASCADE,
  status TEXT CHECK (status IN ('pending', 'reviewed', 'accepted', 'rejected')) DEFAULT 'pending',
  applied_at TIMESTAMP DEFAULT now()
);
Enable Row Level Security (RLS) for the tables and configure policies to control data access for users.
Contributing
We welcome contributions! To contribute:

Fork the repository.
Create a new branch for your feature:
bash
Copy code
git checkout -b feature-name
Commit your changes:
bash
Copy code
git commit -m "Add your message"
Push to your branch:
bash
Copy code
git push origin feature-name
Submit a pull request.
License
This project is licensed under the MIT License.

Contact
For any inquiries or support, reach out to us at support@workwave.com.

Happy coding! 🚀

css
Copy code

This version updates the database to **Supabase**, includes instructions for setting up the data