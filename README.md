 # Profanity Check API

This API endpoint, built with `hono-js`, uses a vector database from Upstash and is deployed on Cloudflare as a worker. It checks the profanity level of a given message and returns a response indicating whether the message contains profanity, along with a score representing the severity.

## Features

- **Profanity Detection**: Analyze messages for profanity.
- **Scoring System**: Receive a score indicating the severity of the profanity.
- **Deployment**: Seamless deployment as a Cloudflare Worker.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/)
- [hono-js](https://hono.dev/)
- [Upstash](https://upstash.com/)
- [Cloudflare Account](https://www.cloudflare.com/)

### Installation

1. **Clone the repository:**
   
   ```sh
   git clone https://github.com/MansoorHussain12/profanity-api.git
   
   cd profanity-api

3. **Install Dependecies:**
```sh
   npm install
```

3. **Configure Upstash:**
   - Set up your Upstash vector database and obtain your credentials.
   - Create ***Wrangler.toml*** file and add Upstash credentials to it.
     
4. **Deploy on Cloudflare:**
   - ```sh
     npm run deploy

### Usage
To check the profanity level of a message, send a `POST` request to the API endpoint with a JSON object containing the message.

**Request**
```sh
{
  "message": "Hello World"
}
```
**Response**
If no profanity is detected:

```sh
{
  "isProfanity": false,
  "score": 0.76693106
}
```



