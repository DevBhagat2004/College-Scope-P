 College Scope

A user-friendly dashboard for searching and comparing college data using the U.S. Department of Education's College Scorecard API.

## Overview

College Scope simplifies the process of finding specific information about colleges and universities. Instead of navigating through complex datasets, users can easily search for any college and select the specific data fields they want to see, all through an intuitive web interface.

## Features

- **Smart Search**: Search for any college or university by name
- **Custom Data Selection**: Choose from a comprehensive list of data fields (enrollment, costs, outcomes, etc.)
- **User-Friendly Labels**: Technical field names are translated into readable descriptions
- **Real-Time Results**: Get the most current data available from the College Scorecard API
- **Data Organization**: Results are automatically sorted by data type (integers, floats, strings)
- **Error Handling**: Clear error messages for invalid searches or missing data

## Tech Stack

- **Frontend**: React.js, Vite
- **Backend**: Node.js, Express.js
- **Libraries**: Axios, CORS, React-Select
- **API**: College Scorecard API (U.S. Department of Education)

## Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- npm or yarn
- A College Scorecard API key (free from [collegescorecard.ed.gov](https://collegescorecard.ed.gov))

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/DevBhagat2004/College-Scope-P.git
   cd College-Scope-P
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Set up environment variables**

   Create `.env` files in both backend and frontend directories (these are in .gitignore for security):

   **Backend (.env)**
   ```env
   PORT=5000
   API_KEY=your_college_scorecard_api_key_here
   ```

   **Frontend (.env)**
   ```env
   VITE_URL=http://localhost:5000
   ```

   > **Note**: You can use any available port number for the backend. Just make sure the VITE_URL in the frontend matches your backend port.

5. **Get your API key**
   - Visit [collegescorecard.ed.gov](https://collegescorecard.ed.gov)
   - Sign up for a free API key
   - Add it to your backend `.env` file

## 🏃‍♂️ Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm start
   ```
   Backend will run on `http://localhost:5000` (or your specified PORT)

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm run dev
   ```
   Frontend will run on `http://localhost:5173`

3. **Open your browser** and navigate to `http://localhost:5173`

## How to Use

1. **Search for a College**: Enter the name of any college or university in the search bar
2. **Select Data Fields**: Use the dropdown menu to choose which information you want to see (e.g., enrollment size, tuition costs, graduation rates)
3. **Submit**: Click the Submit button to fetch the data
4. **View Results**: Results are automatically organized by data type for easy reading
5. **Reset**: Use the Reset button to clear your search and start over

## API Information

This project uses the College Scorecard API with the following structure:

```
https://api.data.gov/ed/collegescorecard/v1/schools?api_key=YOUR_API_KEY&school.name=Harvard University&fields=id,school.name,latest.student.size
```

- **Rate Limit**: 1000 requests per hour for free accounts
- **Data Fields**: All available fields are defined in the College Scorecard Data Dictionary
- **Latest Data**: The app automatically prefixes fields with "latest." to get the most current data

## Project Structure

```
College-Scope-P/
├── frontend/
│   ├── src/
│   │   ├── Search.jsx
│   │   ├── Dropdown.jsx
│   │   ├── options.json
│   │   └── App.jsx
│   └── .env
├── backend/
│   ├── server.js
│   └── .env
└── README.md
```

## Error Handling

The application includes comprehensive error handling:

- **No Options Selected**: Returns "Error 400: Please select the Options!"
- **Invalid College Name**: Returns "Not Being able to get Data from API, check field Name & School Name"
- **API Rate Limits**: Displays appropriate error messages when rate limits are exceeded


## Acknowledgments

- [U.S. Department of Education](https://www.ed.gov/) for providing the College Scorecard API
- [College Scorecard](https://collegescorecard.ed.gov/) for making college data accessible

Project Link: [https://github.com/DevBhagat2004/College-Scope-P](https://github.com/DevBhagat2004/College-Scope-P)

---

⭐ If you found this project helpful, please give it a star!
