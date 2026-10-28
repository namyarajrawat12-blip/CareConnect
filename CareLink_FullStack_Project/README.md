# CareLink Full-Stack Hospital Management System

College mini-project prototype using HTML/CSS/JavaScript, Java 21, Spring Boot, JDBC, Maven, and MySQL.

## Run locally
1. Install JDK 21, Maven 3.9+, and MySQL 8+.
2. In MySQL Workbench, execute all of `database/schema.sql`.
3. In a terminal from this folder, set your local database credentials:
   `export DB_URL='jdbc:mysql://localhost:3306/carelink?serverTimezone=UTC'`
   `export DB_USER='root'`
   `export DB_PASSWORD='YOUR_MYSQL_PASSWORD'`
4. Run `mvn spring-boot:run`.
5. Open `http://localhost:8080`. Test API at `http://localhost:8080/api/health`.

## Demo accounts
Admin: admin@carelink.in / admin123
Doctor: doctor@carelink.in / doctor123
Patient: patient@carelink.in / patient123

These are demonstration-only credentials. This prototype does not implement production authentication or enforce secure role authorization. Use fictional patient data only.

## Included modules
Dashboard, patient registration, doctors, appointments, medical records, medicines, admissions, bills, consent register and audit log. The Java API serves the frontend and reads/writes MySQL.

## API
GET /api/health, GET /api/dashboard, POST /api/auth/login,
GET/POST/DELETE /api/patients, GET/POST /api/doctors,
GET/POST /api/appointments, GET/POST /api/records,
GET /api/medicines, GET /api/admissions, GET /api/bills,
GET/POST /api/consents, PATCH /api/consents/{id}/revoke,
GET /api/audit-logs.

## GitHub upload
Extract ZIP, open this folder in VS Code/GitHub Desktop, commit files, then publish/push the repository. Do not upload passwords, .env files, or real patient information.

## Limitations
Educational prototype only. Consent is stored and revocable but production-grade identity verification, server-side role-based access control, and complete enforcement of consent before medical-record access still need implementation. Test locally before presenting.
