# AnimeRecs

AnimeRecs is a personalized anime recommendation system designed to help anime enthusiasts discover new shows based on their favorite genres. Powered by Weaviate, MyAnimeList dataset, and built using ShadCN Vue and Nuxt, AnimeRecs provides an intuitive interface and accurate recommendations.

## Table of Contents

- [Demo](#demo)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Demo

Check out the live demo of AnimeRecs [here](http://www.animerecs.com).

## Features

- Personalized anime recommendations based on user input
- Simple and intuitive user interface
- Powered by Weaviate for efficient search and recommendations
- Utilizes the comprehensive MyAnimeList dataset

## Tech Stack

- **Frontend:**
  - [ShadCN Vue](https://shadcn.dev/)
  - [Nuxt.js](https://nuxtjs.org/)
- **Backend:**
  - [Node.js](https://nodejs.org/)
  - [Express.js](https://expressjs.com/)
  - [Weaviate](https://weaviate.io/)
- **Database:**
  - MyAnimeList dataset from Kaggle

## Installation

### Prerequisites

- Node.js and npm/yarn installed
- Docker installed
- Kaggle account for downloading the MyAnimeList dataset

### Setup Weaviate

1. Create a `docker-compose.yml` file:

   ```yaml
   version: "3.4"
   services:
     weaviate:
       image: semitechnologies/weaviate:latest
       ports:
         - "8080:8080"
       environment:
         AUTHENTICATION_ANONYMOUS_ACCESS_ENABLED: "true"
         PERSISTENCE_DATA_PATH: "./data"
         DEFAULT_VECTORIZER_MODULE: "text2vec-transformers"
   ```

2. Start Weaviate:

   ```bash
   docker-compose up -d
   ```

### Clone the Repository

```bash
git clone https://github.com/yourusername/animerecs.git
cd animerecs
```

### Install dependencies

`
npm install`

# or

`yarn install`
