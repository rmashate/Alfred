# Alfred - Recipe Generation Service

Alfred is a web service that helps generate recipe ideas based on available ingredients and preferences.

## Features

- Generate recipes based on available ingredients
- Consider dietary preferences and restrictions
- Get detailed instructions and cooking times

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/rmashate/Alfred.git
   cd Alfred
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: .\venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Copy `.env.example` to `.env` and add your OpenAI API key:
   ```bash
   cp .env.example .env
   ```

5. Run the application:
   ```bash
   flask run
   ```

## API Usage

### Generate Recipe

```bash
curl -X POST http://localhost:5000/api/recipes/generate \
  -H "Content-Type: application/json" \
  -d '{
    "ingredients": ["chicken", "rice", "broccoli"],
    "preferences": {
      "cuisine": "Asian",
      "dietary": "low-carb"
    }
  }'
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.