# Environment Variables Setup

Create a `.env` file in the root directory with the following variables:

```env
# Google Gemini API Configuration
GEMINI_API_KEY=your_gemini_api_key_here

# Flask Secret Key (generate a random long string for production)
SECRET_KEY=your-secret-key-here

# Database Configuration
# Default: sqlite:///users.db
# For Render persistent disk: sqlite:////opt/render/project/src/instance/users.db
SQLALCHEMY_DATABASE_URI=sqlite:///users.db
```

## Setup Instructions:

1. Create a `.env` file in the root directory
2. Add your Gemini API key
3. Generate a secure SECRET_KEY (you can use: `python -c "import secrets; print(secrets.token_hex(32))"`)
4. Keep the database URI as default for local development

## For Render Deployment:

In Render dashboard, add these environment variables:
- `GEMINI_API_KEY`: Your Gemini API key
- `SECRET_KEY`: Generated secret key
- `SQLALCHEMY_DATABASE_URI`: `sqlite:////opt/render/project/src/instance/users.db` (for persistent storage)
