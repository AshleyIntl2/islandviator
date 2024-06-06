# ChatGPT Bot for Virgin Islands Visitors

This project is a chatbot built in Golang that uses the ChatGPT API and integrates various other APIs to provide comprehensive information to visitors, locals, and expats in the Virgin Islands. The bot can provide details on activities, hotels, weather, and more.

## Features

- Chat with GPT-3 for general inquiries.
- Get real-time information on activities and sightseeing.
- Find and book hotels.
- Retrieve current weather conditions.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/my-chatbot.git
    cd my-chatbot
    ```

2. Initialize Go modules:
    ```bash
    go mod tidy
    ```

3. Install dependencies:
    ```bash
    go get ./...
    ```

## Configuration

1. Create a `.env` file in the root directory of your project:
    ```env
    CHATGPT_API_KEY=your_chatgpt_api_key
    ACTIVITIES_API_KEY=your_activities_api_key
    HOTELS_API_KEY=your_hotels_api_key
    WEATHER_API_KEY=your_weather_api_key
    ```

2. Update the configuration as needed in the `config/config.go` file.

## Usage

1. Run the application:
    ```bash
    go run main.go
    ```

2. The server will start on port 8080. You can access it via `http://localhost:8080`.

3. Use the following endpoints to interact with the bot:
    - `/chat?prompt=your_prompt` - Chat with GPT-3.
    - `/activities?location=your_location` - Get activities in a specific location.
    - `/hotels?location=your_location` - Find hotels in a specific location.
    - `/weather?location=your_location` - Get weather conditions for a specific location.

## API Endpoints

### Chat with GPT-3
```http
GET /chat?prompt=your_prompt
