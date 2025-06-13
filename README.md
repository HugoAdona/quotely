# Quotely 📝

A random quote generator API built with Node.js by Hugo Adona.

## 🌟 Features

- **Random Quote Generation**: Get single or multiple random quotes with their authors
- **JSON Database**: Quotes are stored in a pre-defined JSON database for fast access
- **RESTful API**: Clean and simple API endpoints
- **Author Attribution**: Each quote comes with proper author attribution
- **Lightweight**: Minimal dependencies for optimal performance

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/HugoAdona/quotely.git
cd quotely
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

The API will be available at `http://localhost:3000` (or your configured port).

## 📚 API Endpoints

### Get a Random Quote
```
GET /api/quote
```

Returns a single random quote with its author.

**Response:**
```json
{
  "quote": "The only way to do great work is to love what you do.",
  "author": "Steve Jobs"
}
```

### Get Multiple Random Quotes
```
GET /api/quotes?count=5
```

Returns multiple random quotes. Use the `count` parameter to specify how many quotes you want (default: 1, max: 50).

**Response:**
```json
{
  "quotes": [
    {
      "quote": "Be yourself; everyone else is already taken.",
      "author": "Oscar Wilde"
    },
    {
      "quote": "In the middle of difficulty lies opportunity.",
      "author": "Albert Einstein"
    }
  ]
}
```

## 🛠️ Usage Examples

### JavaScript (Fetch API)
```javascript
// Get a single quote
fetch('/api/quote')
  .then(response => response.json())
  .then(data => console.log(data.quote, '- ' + data.author));

// Get multiple quotes
fetch('/api/quotes?count=3')
  .then(response => response.json())
  .then(data => data.quotes.forEach(item => 
    console.log(item.quote, '- ' + item.author)
  ));
```

### cURL
```bash
# Get a single quote
curl http://localhost:3000/api/quote

# Get 5 random quotes
curl http://localhost:3000/api/quotes?count=5
```

## 📁 Project Structure

```
quotely/
├── src/
│   ├── routes/
│   ├── data/
│   │   └── quotes.json
│   └── app.js
├── package.json
├── README.md
└── .gitignore
```

## 🎯 Use Cases

- Daily inspiration apps
- Quote of the day widgets
- Writing prompts for journaling
- Social media content
- Educational applications
- Motivational displays

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Adding New Quotes

To add new quotes to the database:

1. Edit the `src/data/quotes.json` file
2. Follow the existing format:
```json
{
  "quote": "Your quote here",
  "author": "Author Name"
}
```
3. Ensure proper JSON formatting
4. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Hugo Adona**
- GitHub: [@HugoAdona](https://github.com/HugoAdona)

## 🙏 Acknowledgments

- Thanks to all the great minds whose quotes inspire us daily
- Built with ❤️ and Node.js

---

*"The best way to predict the future is to create it." - Peter Drucker*