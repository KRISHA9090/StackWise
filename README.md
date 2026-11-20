# StackWise - AI Powered Library/Bookshop Management System

An intelligent management system for libraries and bookshops, powered by AI for smarter cataloging, recommendations, and inventory insights.

---

## About

StackWise helps libraries and bookshops manage their catalog, members, borrowing, and sales in one place. It uses AI to recommend books, forecast demand, and auto-fill book details from an ISBN.

---

## Features

- Book catalog management with full metadata support
- Member registration and role-based access (admin, librarian, member)
- Book issue and return with automatic fine calculation
- Real-time inventory tracking with low-stock alerts
- Sales and invoicing for bookshops
- Multi-branch support
- AI-powered book recommendations
- Demand forecasting for smarter stocking
- AI chatbot for natural-language book search
- Auto metadata enrichment from ISBN
- Duplicate detection
- Analytics dashboard with reports

---

## Use Cases

**Public and Academic Libraries**
Librarians issue and return books, track due dates, manage member profiles, and send overdue reminders. Inventory can be tracked across multiple branches.

**Independent and Online Bookshops**
Owners manage stock in real time, process sales, generate invoices, and send personalized book recommendations to customers.

**Educational Institutions**
Schools and colleges suggest textbooks based on enrolled courses, let faculty reserve books, and enforce borrowing limits for students.

**AI-Assisted Reader Experience**
Readers get personalized book suggestions, can ask the chatbot questions in plain language, and browse books by mood or theme.

**Business Intelligence for Owners**
Owners forecast demand, analyze reader sentiment from reviews, and view dashboards showing top books and revenue trends.

**Automated Catalog Enrichment**
Staff enter an ISBN and the system fetches the cover, description, and genre automatically. Duplicate entries are flagged before they clutter the catalog.

---

## Tech Stack

**Frontend**
React.js, Redux Toolkit, Tailwind CSS, Axios, React Router, Recharts

**Backend**
Node.js, Express.js, Mongoose, JWT, bcrypt, Cloudinary

**Database**
MongoDB (with optional MongoDB Atlas and Redis caching)

**AI Service**
Python, Flask, scikit-learn, Prophet, HuggingFace, LangChain, OpenAI GPT

**DevOps**
Docker, GitHub Actions, Nginx

**Testing**
Jest, Supertest, React Testing Library, Pytest

---

## Problems Solved

**Manual cataloging is slow and error-prone**
AI metadata enrichment fills in book details from an ISBN, cutting cataloging time by up to 80 percent.

**Recommendations feel generic**
A hybrid recommendation engine delivers personalized suggestions that increase reader engagement and circulation.

**Overstocking and understocking**
Demand forecasting predicts which titles to stock, reducing dead inventory and preventing stockouts.

**Scattered systems and paper registers**
A single dashboard centralizes catalog, members, borrowing, sales, and analytics.

**Search feels rigid**
An AI chatbot lets users search in plain language instead of exact keywords.

**Duplicate records clutter the catalog**
Semantic duplicate detection flags near-identical entries before they are saved.

**Owners lack actionable insights**
Real-time dashboards and sentiment analysis give owners data-driven decision-making power.

**Weak access control**
JWT-based role access ensures only admins and librarians can perform sensitive actions.

**Single-location limitation**
Multi-branch support with branch-specific inventory and inter-branch transfers.

**High operational cost**
An open-source stack and modular microservice design keep costs low and scale easily.

---

## Getting Started

### Prerequisites

- Node.js v18 or higher
- MongoDB v6 or higher
- Python 3.10 or higher
- Git

### Installation

Clone the repository.

```
git clone https://github.com/your-username/stackwise.git
cd stackwise
```

Install backend dependencies.

```
cd server
npm install
```

Install frontend dependencies.

```
cd ../client
npm install
```

Install AI service dependencies.

```
cd ../ai-service
pip install -r requirements.txt
```

### Environment Variables

Create a `.env` file in the server folder.

```
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret_key
OPENAI_API_KEY=your_openai_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

Create a `.env` file in the client folder.

```
REACT_APP_API_URL=http://localhost:5000/api
```

Create a `.env` file in the ai-service folder.

```
FLASK_PORT=8000
OPENAI_API_KEY=your_openai_key
```

### Run the App

Open three terminals.

Backend:

```
cd server
npm run dev
```

AI Service:

```
cd ai-service
python app.py
```

Frontend:

```
cd client
npm start
```

Open http://localhost:3000 in your browser.

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /auth/register | Register a new user |
| POST | /auth/login | Login and get a token |
| GET | /books | List all books |
| POST | /books | Add a new book |
| PUT | /books/:id | Update a book |
| DELETE | /books/:id | Delete a book |
| POST | /borrow | Issue a book |
| PUT | /borrow/:id/return | Return a book |
| GET | /recommendations/:userId | Get book recommendations |
| POST | /chatbot | Ask the AI assistant |

---

## Project Structure

```
stackwise/
  client/         React frontend
  server/         Node and Express backend
  ai-service/     Python AI microservice
  docs/           Documentation and screenshots
  docker-compose.yml
  README.md
```

---

## Roadmap

- [x] Core catalog and borrowing system
- [x] Role-based authentication
- [x] AI recommendation engine
- [x] Chatbot assistant
- [x] Demand forecasting
- [ ] Mobile app
- [ ] Barcode and QR scanning for issue and return
- [ ] Payment gateway integration (Stripe and Razorpay)
- [ ] Multi-language support
- [ ] Advanced analytics dashboard with charts
- [ ] Public API for third-party integrations

---

## Contributing

1. Fork the repository.
2. Create a branch.

```
git checkout -b feature/your-feature
```

3. Commit your changes.

```
git commit -m "Add your feature"
```

4. Push the branch.

```
git push origin feature/your-feature
```

5. Open a Pull Request.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---



---

If you find StackWise useful, please give the repository a star.
