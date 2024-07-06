# Football Players Rating Application

## Overview

This application allows users to filter and view football players from EA FC 24 database based on their ratings, positions, and other criteria. The application reads player data from a CSV file and displays it in a user-friendly web interface.

## Features

- **Filter Players by Rating**: Filter players based on minimum and maximum ratings.
- **Position Filtering**: Filter players by their positions.
- **Random Selection**: Randomly select a specified number of players that meet the filtering criteria.
- **Health Check Endpoint**: A simple health check endpoint to verify the server status.

## Technology Stack

- **Server-side**: Node.js, Express.js
- **View Engine**: EJS
- **CSV Parsing**: `csv-parser`

## Getting Started

### Prerequisites

- Node.js (v12.x or higher)
- npm (v6.x or higher)

### Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/yourusername/football-players-rating-app.git
   cd football-players-rating-app
   ```

2. **Install dependencies**:
   ```sh
   npm install
   ```

3. **Ensure the CSV file is in place**:
   - Place the `male_players.csv` file inside the `res` directory.

### Running the Application

1. **Start the development server**:
   ```sh
   npm run start
   ```

2. **Open your browser** and navigate to `http://localhost:3000` to view the application.

### Health Check

To check if the server is running, visit:
```sh
http://localhost:3000/health
```

## Directory Structure

```plaintext
├── res
│   └── male_players.csv  # CSV file containing player data
├── views
│   └── players.ejs       # EJS template for rendering players
├── app.js                # Main application file
├── package.json          # npm package file
├── .env.example          # Example environment configuration file
├── .gitignore            # Git ignore file
└── README.md             # README file
```

## Usage

### Filtering Players

1. Navigate to the homepage.
2. Use the filters to specify:
   - Minimum rating (`minRating`)
   - Maximum rating (`maxRating`)
   - Number of players to display (`numPlayers`)
   - Positions (optional, can select multiple positions)

3. Click the "Go" button to view the filtered list of players.

## Example Queries

- **Filter by Rating and Number of Players**:
  ```
  http://localhost:3000/?minRating=80&maxRating=90&numPlayers=5
  ```

- **Filter by Rating, Number of Players, and Position**:
  ```
  http://localhost:3000/?minRating=80&maxRating=90&numPlayers=5&position=Forward
  ```
