# Budget Register Application

A simple web-based budget tracking application that allows you to record and manage financial transactions with GitHub-based storage.

## Features

- Add, edit, and delete financial entries
- Filter transactions by category
- Store data in a JSON file on GitHub
- Automatic data backup to browser's localStorage

## Setup for GitHub Storage

1. **Create a GitHub Repository**:
   - Go to GitHub and create a new repository
   - Make note of your username and repository name

2. **Create a Personal Access Token**:
   - Go to GitHub Settings > Developer settings > Personal access tokens
   - Generate a new token with 'repo' scope
   - Save this token securely (you'll need it when using the app)

3. **Configure the Application**:
   - Open `index.html` in a code editor
   - Find the GitHub configuration section at the top of the script
   - Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username
   - Replace `YOUR_REPO_NAME` with your repository name

## How to Use

### Local Usage

1. Open the `index.html` file in your web browser
2. Your data will be automatically saved in your browser's localStorage
3. Click "Save to GitHub" to store data in your GitHub repository
4. Click "Load from GitHub" to retrieve data from your GitHub repository

### Running with Local Server

If you have Node.js installed:

1. Open a terminal/command prompt
2. Navigate to the project directory
3. Run `node server.js`
4. Open your browser and go to `http://localhost:3000`

## Hosting on GitHub Pages

To host this application on GitHub Pages:

1. Make sure you've already created a GitHub repository as described in the setup
2. Upload all the files to the repository
3. Go to repository Settings > Pages
4. Select the branch you want to deploy (usually 'main')
5. Save the settings and wait for GitHub to deploy your site
6. Your site will be available at `https://yourusername.github.io/repositoryname/`

## How the GitHub Storage Works

1. When you click "Save to GitHub", the app will:
   - Prompt for your GitHub token if not already provided
   - Convert your data to JSON format
   - Create or update a file called `data/budget_data.json` in your repository

2. When you click "Load from GitHub", the app will:
   - Attempt to load the data file from your repository
   - Parse the JSON data and display it in the application

3. The app also maintains a local backup in your browser's localStorage

## Important Notes

- You need a GitHub account and repository to use the GitHub storage feature
- Your GitHub Personal Access Token is stored in your browser's localStorage
- The data file is stored publicly in your GitHub repository unless your repository is private
- For security, never share your GitHub token with anyone