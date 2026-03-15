# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Messappar.at is a simple static website for a reading circle focused on Karen Barad's "Meeting the Universe Halfway". The site displays session information, registration links, and provides access to the book PDF.

## Development Commands

**Start the server:**
```bash
node app.js
```
The server runs on `http://localhost:3000`

**Install dependencies:**
```bash
npm install
```

## Architecture

This is a minimal Express.js application with no build process, no tests, and no client-side JavaScript.

**Server (`app.js`):**
- Single-file Express 5.1.0 server
- Serves static files from the `public/` directory
- Runs on port 3000 (hardcoded)

**Frontend (`public/`):**
- `index.html` - Main page with reading circle session information
- `style.css` - Styling with animated gradient backgrounds
- `atlas.svg` - Favicon
- `files/` - Contains the book PDF

**Content updates:**
- Session information is directly edited in `index.html`
- No database or CMS - all content is static HTML

## Port Configuration

The server port is hardcoded to 3000 in `app.js:3`. To change it, modify the `port` constant.
