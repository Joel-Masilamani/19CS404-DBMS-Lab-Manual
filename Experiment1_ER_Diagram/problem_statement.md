# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
University

## ER Diagram:
![438532434-b8184a94-0773-4294-be8b-8d254aca72d5](https://github.com/user-attachments/assets/7b7325d4-c4f8-42e3-b232-f077e3af8e5f)
## Entities and Attributes:
UNIVERSITY

    Attributes: Name, Place

STUDENT

    Attributes: Student ID, Name, Year

COURSE

    Attributes: Course Name, Course Code, Slot, Pre-requisite

PROFESSOR

    Attributes: Name, Professor ID, Working Experience

## Relationships and Constraints:
admission (UNIVERSITY — STUDENT)

    Cardinality: One university can admit many students; each student is admitted to one university.

    Participation: Total participation from STUDENT, partial from UNIVERSITY.

enrolls (STUDENT — COURSE)

    Cardinality: One student can enroll in multiple courses; each course can have many students.

    Participation: Partial participation from both STUDENT and COURSE.

handled (COURSE — PROFESSOR)

    Cardinality: One professor can handle multiple courses; each course is handled by one professor.

    Participation: Total from COURSE, partial from PROFESSOR.

## Extension (Prerequisite ):
The prerequisite attribute is added directly to the COURSE entity.

This implies that each course may have a prerequisite course defined (modeled as a self-referencing attribute, i.e., prerequisite course name/code).

## Design Choices:
Entity Selection:

    Chose UNIVERSITY, STUDENT, COURSE, and PROFESSOR as they represent key real-world concepts in an academic scenario.

Relationship Modeling:

    admission models the process of a student joining a university.

    enrolls captures course registration by students.

    handled shows which professor teaches which course.

Attributes:

    Added essential identifying and descriptive attributes like IDs and names to uniquely distinguish entities.

Assumptions:

    Each course has only one professor.

    Each student belongs to only one university.

    Prerequisites are modeled simply as text (or course code reference) within the COURSE entity.
## RESULT
A complete ER model of a university system that defines students, courses, professors, and their interrelationships, including prerequisites, with proper constraints and rationale.
