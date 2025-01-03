# Automatic Time Table Generator

An automated timetable generation system using Spring Boot for Backend and React for Frontend.

## Project Overview

The automatic timetable generator helps educational institutions automatically schedule classes optimally, avoiding time and location conflicts.

### Key Features

- Automated timetable generation based on constraints
- Teacher, class, and classroom management
- Subject and teaching time management
- Schedule conflict detection and resolution
- Multiple export formats (PDF, Excel)
- User-friendly interface

## System Requirements

### Backend (Spring Boot)
- Java JDK 17+
- Spring Boot 3.x
- MySQL 8.0
- Maven 3.8+

### Frontend (React)
- Node.js 18.x+
- npm 9.x or yarn
- React 18.x
- TypeScript 5.x

## Installation & Running

### Backend

1. Clone repository:
```bash
git clone https://github.com/your-username/automatic-timetable.git
cd automatic-timetable/backend
```

2. Configure database in `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/timetable_db
spring.datasource.username=your_username
spring.datasource.password=your_password
```

3. Run application:
```bash
mvn spring-boot:run
```

Backend will run at `http://localhost:8080`

### Frontend

1. Navigate to frontend directory:
```bash
cd ../frontend
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Configure API endpoint in `.env`:
```
REACT_APP_API_URL=http://localhost:8080/api
```

4. Run application:
```bash
npm start
# or
yarn start
```

Frontend will run at `http://localhost:3000`

## Project Structure

### Backend
```
src/
├── main/
│   ├── java/
│   │   └── com/timetable/
│   │       ├── controllers/
│   │       ├── models/
│   │       ├── repositories/
│   │       ├── services/
│   │       ├── config/
│   │       └── utils/
│   └── resources/
│       └── application.properties
```

### Frontend
```
src/
├── components/
├── pages/
├── services/
├── utils/
├── hooks/
├── types/
└── App.tsx
```

## API Documentation

API is documented using Swagger UI, accessible at:
`http://localhost:8080/swagger-ui.html`

### Main endpoints:

- `POST /api/timetable/generate`: Generate new timetable
- `GET /api/timetable/{id}`: Get timetable information
- `GET /api/teachers`: Get teachers list
- `GET /api/classes`: Get classes list
- `GET /api/rooms`: Get rooms list

## Contributing

1. Fork the project
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add some amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Create Pull Request

## License

This project is licensed under the MIT License. See `LICENSE` for details.
