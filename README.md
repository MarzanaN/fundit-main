# Fundit 💸 – Personal Expense and Budget Tracker

**Fundit** is a full-stack web application designed to help users manage their income, expenses, savings, and financial goals efficiently through a beautifully designed interface with interactive visualizations and user-friendly features. 

Fundit empowers individuals to track their finances, create savings goals, set budgets, and monitor repayments, all while enjoying the flexibility to explore as a guest.

Live App: 🌐 [https://www.fundit-app.com](https://www.fundit-app.com)

---

## 📦 Repositories

- **Frontend**: [fundit-frontend](https://github.com/MarzanaN/fundit-frontend)
- **Backend**: [fundit-backend](https://github.com/MarzanaN/fundit-backend)

---

## ⚙️ Tech Stack

| Component        | Technology / Service                                                            |
|------------------|----------------------------------------------------------------------------------|
| Frontend         | React with Tailwind CSS, AOS animations, React Icons, Chart.js                   |
| Backend          | Django + Django REST Framework (Deployed on Render)                             |
| Authentication   | JWT via `rest_framework_simplejwt`                                              |
| Database         | PostgreSQL (via `dj_database_url`)                                              |
| Static Files     | WhiteNoise                                                                      |
| Email            | Gmail SMTP                                                                      |
| Deployment       | Render (Backend), Vercel (Frontend) with custom domain                          |
| API Testing      | Postman                                                                          |



---

## ✨ Features

### 🔓 Public Routes

- **Pages**: Home, About, Features, Support
- **Dark theme design** with branded colors
- **User Authentication**:
  - Register with email verification
  - Sign in with email & password
  - Forgot/reset password flow
- **Guest Mode**: One-click "Explore as Guest" simulates a fully functioning user with dummy data and unique session handling

---

### 🔐 Authenticated Routes (Light theme)

After signing in or exploring as guest:

#### **Navbar**
- User icon displays the first name
- Dropdown with: `Settings`, `Support`, and `Logout`

---

## 📊 Main Pages

### 1. **Dashboard**
An overview of the user’s financial life:

- **Yearly Overview**: Pie chart showing income, expenses, and savings
- **Monthly Breakdown**: 
  - Select any month
  - View income/expense data as a pie chart or list
- **Goals Preview**: Top two active savings goals with progress bars
- **Net Income Tracker**: Quarterly breakdown with area charts showing income, expenses, and net

---

### 2. **Income Page**

- **Create Income Entry**: Add income with date, category (or custom), amount, recurring status
- **Update Entries**: Edit/delete monthly entries
- **Visual Sections**:
  - Monthly Pie Chart (by category)
  - Line Graph Overview (up to 13 months)

---

### 3. **Expenses Page**

- **Create Expense**: Add one-time or recurring expenses
- **Create Budget**: Assign budgets to categories with monthly recurrence
- **Update Entries**: Edit/delete expenses or budgets
- **Visual Sections**:
  - Monthly Breakdown: Pie chart of expenses
  - Top 5 Recurring Expenses
  - Budget Tracker: Progress bars comparing expenses vs. budget

---

### 4. **Savings & Repayments Page**

- **Create General Savings**: Manual savings tracker with logs
- **Create Savings Goal**: Track goals with deadlines and progress bars
- **Create Repayment Goal**: Similar to savings goals but for debts
- **Sections**:
  - General Savings: View +/− history, duration, and updates
  - Savings Goals: Track target, progress, deadline
  - Repayment Goals: Track repayment progress, outstanding amount

---

### 5. **Support Page**

- Same layout for guests and users
- Form includes: name, email (auto-filled), issue category, message
- Sends email to Fundit support inbox

---

### 6. **Settings Page**

- Editable user info: First/Last Name, Email, DOB, Sex, Currency
- Password change via secured flow
- **Delete Account**:
  - Requires reason, feedback, star rating, confirmation checkbox
  - Sends a detailed summary to Fundit email

---

## 🔧 Installation

### 1. Clone the Repositories

```bash
git clone https://github.com/MarzanaN/fundit-frontend.git
git clone https://github.com/MarzanaN/fundit-backend.git
```

---

### 2. Backend Setup (Django)

```bash
cd fundit-backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Create a `.env` file in the root of the backend and add:

```env
SECRET_KEY=your_django_secret
DEBUG=True
DATABASE_URL=your_postgresql_db_url
EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_email_password
```

Run the server:

```bash
python manage.py migrate
python manage.py runserver
```

---

### 3. Frontend Setup (React)

```bash
cd fundit-frontend
npm install
npm start
```

Make sure the frontend is configured to communicate with the backend API (e.g., `http://localhost:8000`) in your `.env` or config file.

---

## 🌍 Deployment

- **Backend**: [Render](https://render.com/)
- **Frontend**: [Vercel](https://vercel.com/) — deployed to [https://www.fundit-app.com](https://www.fundit-app.com)
- **Static Files**: Served using WhiteNoise
- **Database**: PostgreSQL in production

---

## 📩 Contact

Built and maintained by **Marzana N**.

Have questions or feedback?  
Submit an issue or reach out via the support form on the website:  
🔗 [https://www.fundit-app.com/support](https://www.fundit-app.com/support)

---

## 📜 License

This project is licensed under the **MIT License**.


