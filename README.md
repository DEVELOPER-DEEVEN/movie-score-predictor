# Movie Score Predictor

Predict user movie ratings on a scale of 1 to 10 using a full-stack solution powered by Google Cloud, Machine Learning, and Angular.

## 🚀 Overview

Movie Score Predictor is an end-to-end application that predicts how a user might rate a movie. It leverages:
- **BigQuery** for data storage and analytics
- **Vertex AI** for machine learning model training and prediction
- **MongoDB** for user and movie data
- **Google Cloud Functions (Java)** for backend logic and API
- **Angular** for a modern, interactive web frontend

## 🏗️ Architecture

- **Backend**: Java-based Google Cloud Function exposes REST/GraphQL endpoints, connects to BigQuery, Vertex AI, and MongoDB.
- **Frontend**: Angular SPA for users to rate movies and view predictions.
- **ML Pipeline**: Trains and serves a model using Vertex AI, with data sourced from BigQuery.

## 📦 Tech Stack

- Java (Google Cloud Functions)
- Angular 14+
- Google BigQuery
- Vertex AI
- MongoDB
- Docker (for frontend deployment)
- Nginx (serving Angular app)

## 🖥️ Getting Started

### Prerequisites

- Node.js & npm
- Java 11+
- Google Cloud account (with BigQuery, Vertex AI, Cloud Functions enabled)
- MongoDB instance

### Backend (Java Cloud Function)

1. Navigate to `src/main/java/gcf2/`
2. Deploy the function using Google Cloud CLI:
   ```sh
   gcloud functions deploy movieScorePredictor --runtime java11 --trigger-http --allow-unauthenticated
   ```
3. Configure environment variables for BigQuery, Vertex AI, and MongoDB.

### Frontend (Angular)

1. Navigate to `angular-web-app/`
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run locally:
   ```sh
   ng serve
   ```
   Visit [http://localhost:4200](http://localhost:4200)

4. To build for production:
   ```sh
   ng build --prod
   ```

5. (Optional) Use Docker for deployment:
   ```sh
   docker build -t movie-score-frontend .
   docker run -p 80:80 movie-score-frontend
   ```

## 🧪 Testing

- **Backend**: Use Postman or curl to test deployed endpoints.
- **Frontend**: Run `ng test` for unit tests.

## 📊 Data

- Sample movie datasets included: `movies.csv`, `movies_train.csv`, `movies_bq_src.csv`

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

See [LICENSE- Project gcf2](./LICENSE- Project gcf2) and [angular-web-app/LICENSE](./angular-web-app/LICENSE) for details.

---

*Built with ❤️ using Google Cloud and Angular.*# movie-score-predictor
