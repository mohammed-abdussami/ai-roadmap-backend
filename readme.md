# Pocketbase backend for ai-roadmap.com

## Setup Instructions

### Option 1: Using Docker (Recommended)
```bash
docker build -t ai-roadmap-backend .
docker run -p 8090:8090 ai-roadmap-backend
```

### Option 2: Local Setup
1. Install Go 1.20 or higher
2. Clone the repository
3. Run: `go mod download` to install dependencies
4. Run: `go run main.go serve --dir data --http 0.0.0.0:8090`
5. PocketBase will start at http://localhost:8090

## Database Schema
1. Import the schema from `pb_schema/pb_schema.json` into your PocketBase admin panel
2. Go to http://localhost:8090/_/ to access the admin dashboard
3. Import the schema file in Settings > Export/Import

## Notes
- Database files will be created in the `pb_data` directory locally
- The `.gitignore` protects your local database from being committed
- Each collaborator will have their own local database after setup