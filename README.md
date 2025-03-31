# WeLocal Transport Service

Local transportation and logistics service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Payment Processing**: Stripe
- **Maps Integration**: Google Maps API
- **Real-time Communication**: Socket.io
- **Push Notifications**: Firebase Cloud Messaging

## Features

- Route planning and optimization
- Real-time vehicle tracking
- Driver management
- Passenger booking system
- Fare calculation
- Payment processing
- Route analytics
- Emergency services integration
- Vehicle maintenance tracking
- Driver ratings and reviews
- Schedule management
- Multi-modal transport options

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- Stripe account
- Google Maps API key
- Firebase project
- Redis (for real-time features)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-transport-service.git
   cd welocal-transport-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8085
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   GOOGLE_MAPS_API_KEY=your-google-maps-api-key
   FIREBASE_PROJECT_ID=your-firebase-project-id
   FIREBASE_PRIVATE_KEY=your-firebase-private-key
   REDIS_URL=redis://localhost:6379
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-transport-service .
docker run -p 8085:8085 welocal-transport-service
```

## API Endpoints

### Route Management
- `GET /api/v1/routes` - Get routes list
- `POST /api/v1/routes` - Create route
- `GET /api/v1/routes/:id` - Get route details
- `PUT /api/v1/routes/:id` - Update route
- `DELETE /api/v1/routes/:id` - Delete route

### Vehicle Management
- `GET /api/v1/vehicles` - Get vehicles list
- `POST /api/v1/vehicles` - Add vehicle
- `GET /api/v1/vehicles/:id` - Get vehicle details
- `PUT /api/v1/vehicles/:id` - Update vehicle status
- `GET /api/v1/vehicles/:id/maintenance` - Get maintenance history

### Driver Management
- `GET /api/v1/drivers` - Get drivers list
- `POST /api/v1/drivers` - Add driver
- `GET /api/v1/drivers/:id` - Get driver details
- `PUT /api/v1/drivers/:id` - Update driver status
- `GET /api/v1/drivers/:id/ratings` - Get driver ratings

### Booking Management
- `GET /api/v1/bookings` - Get bookings list
- `POST /api/v1/bookings` - Create booking
- `GET /api/v1/bookings/:id` - Get booking details
- `PUT /api/v1/bookings/:id/status` - Update booking status
- `DELETE /api/v1/bookings/:id` - Cancel booking

### Real-time Tracking
- `GET /api/v1/tracking/vehicles` - Get vehicle locations
- `GET /api/v1/tracking/vehicles/:id` - Get specific vehicle location
- `POST /api/v1/tracking/vehicles/:id/update` - Update vehicle location

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── payments/        # Payment processing
├── maps/            # Maps integration
├── tracking/        # Real-time tracking
├── notifications/   # Push notifications
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure payment processing
- Real-time data encryption

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 