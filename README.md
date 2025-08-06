# Memetic Review

A newspaper-style website for the Memetic Review publication.

## Project Structure

- `index.html` - Homepage ("Today's Noospaper")
- `columns.html` - Columns section
- `styles.css` - Shared styles for consistent design across all pages
- `Gotham/` - Font files directory

## Local Development

### Testing the Website Locally

1. Open Terminal
2. Navigate to the project directory:
   ```bash
   cd /Users/catatafish/repos/memetic_universe
   ```
3. Start a local web server:
   ```bash
   python3 -m http.server 8000
   ```
4. Open your browser and visit: `http://localhost:8000`
5. Click through the navigation links to test all pages
6. Press `Ctrl + C` in Terminal to stop the server

### Alternative Server Options

If Python 3 isn't available, try:
- Python 2: `python -m SimpleHTTPServer 8000`
- Node.js: `npx http-server`
- PHP: `php -S localhost:8000`

## Features

- Responsive newspaper-style design
- Custom Gotham font integration
- Consistent header and navigation across all pages
- Active page highlighting in navigation