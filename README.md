Here’s the updated version of the assessment test with the database design and migration requirements included:

---

### Assessment Test: Backend and Frontend Development for German "Scheine" System

**Objective:**  
You are tasked with creating a system that allows doctors to generate different types of "Scheine" (e.g., AU, Überweisung, Rezepte) commonly used in German medical practices. The system will consist of a backend to process the form data and generate a PDF, and a frontend interface for doctors to input the required information and preview the results before generating the final "Schein."

### Technology Stack:
- **Backend**: 
  - **ExpressJS**
  - **TypeORM** with PostgreSQL
  - **NodeJS PDF generator** (e.g., PDFKit or another of your choice)

- **Frontend**: 
  - **Vite**
  - **React**

### Task Description:

#### 1. **Backend Development (ExpressJS, TypeORM, PostgreSQL)**
   - Set up an ExpressJS server.
   - **Database Design**: Create a PostgreSQL database using TypeORM to store information about the "Scheine." The schema should include both common fields (e.g., patient details, doctor details, Schein type) and type-specific fields (e.g., diagnosis for AU, prescription details for Rezepte). Design the schema to support scalability for future types of "Scheine."
   - Implement TypeORM migrations to create the necessary tables in the database.
   - Develop an API endpoint to accept input data (e.g., patient information, diagnosis, doctor's signature) from the frontend and store it in the database.
   - Use a NodeJS PDF generator (e.g., PDFKit) to take the input and generate a PDF based on a provided template (see the attached PDF, `Mustersammlung.pdf`, for an example of a "Schein" format).
   - Create an additional endpoint to preview the generated PDF.

#### 2. **Frontend Development (Vite, React)**
   - Create a React frontend that allows doctors to input the required information for the "Schein."
   - Form fields should include the following input fields (examples from the PDF template):
     - Name and Surname of the patient
     - Date of birth
     - Diagnosis
     - Doctor's signature (simulated with a text input)
     - Additional fields based on the type of "Schein" (AU, Überweisung, Rezepte).
   - Provide a dropdown to select the type of "Schein" the doctor is creating.
   - Add a "Preview" button that submits the form data to the backend and displays the generated PDF in a preview window.

#### 3. **Generating the PDF**
   - Upon receiving the input from the frontend, use the NodeJS PDF generator to write the information into the correct positions on the provided PDF template (`Mustersammlung.pdf`).
   - The generated PDF should contain all the information in the correct format and location based on the template.
   - Return the generated PDF as a file download or preview it directly in the frontend.

### Requirements:

#### Backend:
- Implement a REST API to handle form submissions.
- Store the form data in a PostgreSQL database using TypeORM.
- Use TypeORM migrations to create and manage the database schema, ensuring proper relationships between entities (e.g., patients, doctors, "Scheine").
- Use a PDF generation library to insert the form data into the specified fields of the PDF template.
- Ensure proper error handling for missing or invalid input.

#### Frontend:
- Create a responsive form interface using React.
- Validate the form input to ensure all required fields are filled.
- Implement a "Preview" button that fetches the PDF preview from the backend.
- Render the preview in the frontend before generating the final PDF.

### Instructions:
1. **Project Setup:**
   - Initialize a new Vite project for the frontend.
   - Set up an ExpressJS server for the backend.
   - Configure TypeORM with PostgreSQL to store form data and implement migrations for database schema creation.
   - Install necessary libraries (e.g., `pdfkit`, `axios`, `react-router`).

2. **Submission:**
   - Provide a link to the GitHub repository with your implementation.
   - Include a README with setup instructions and any design decisions you made.
   - The README should also include sample requests and responses for the API.

### Evaluation Criteria:
- **Functionality**: Does the system allow for the creation, preview, and generation of "Scheine" in PDF format?
- **Database Design**: Is the database schema well-structured, scalable, and designed to support multiple "Schein" types, both now and in the future? Are TypeORM migrations implemented correctly?
- **Code Quality**: Is the code clean, modular, and well-structured?
- **User Experience**: Is the frontend intuitive and easy to use for doctors?
- **PDF Accuracy**: Does the PDF match the provided template, and are the form fields properly placed?
- **Error Handling**: Are missing or invalid inputs handled gracefully?
- **Documentation**: Is the project well-documented with clear setup instructions?

---

Good luck! We look forward to seeing your submission.

---

This version includes both database design and migration requirements using TypeORM, ensuring the applicant demonstrates proficiency in handling database schema design and implementation through migrations.
