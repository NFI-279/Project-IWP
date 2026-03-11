 Campus Classroom Visibility Platform

## Overview

Campus Classroom Visibility Platform is a real-time web application designed to help students and teachers monitor and manage classroom availability across campus buildings.

The system allows teachers to book classrooms for a specific academic week using predefined time slots, while students can view classroom availability and see which teacher has reserved a room.

The application ensures structured scheduling, prevents booking conflicts, and provides administrative tools for managing campus infrastructure.

---

## User Roles

### Student
- Can register and log in
- Can view classroom availability
- Can filter by building, day, and time slot
- Can see which teacher has booked a classroom
- Cannot create or cancel reservations

### Teacher
- Can register and log in (email must contain "teacher")
- Can book classrooms for a specific week
- Can select predefined time slots
- Cannot have overlapping reservations
- Can cancel their own reservations
- Can view their weekly schedule in calendar format

### Administrator
- Manages campus buildings and classrooms
- Defines classroom capacity
- Adds, edits, or removes classrooms
- Manages building structure
- Does not approve bookings (booking is automatic)

---

## Booking Rules

- Reservations are made for one specific week only
- Teachers must book rooms at the start of each week
- No automatic recurring reservations
- Fixed predefined time slots between 08:00 and 20:00
- A classroom cannot be double-booked
- A teacher cannot have two reservations at the same time

---

# User Stories

## Story 1 - Classroom Booking (Teacher)

As a teacher, I want to reserve classrooms for predefined time slots during a specific academic week so that I can organize my lectures without scheduling conflicts.

- The system allows selection of building, classroom, day, and time slot.
- The system prevents overlapping bookings for the same classroom.
- The system prevents a teacher from booking two classrooms at the same time.
- The reservation is automatically confirmed if no conflict exists.
- The teacher can view their weekly schedule in a calendar format.
- The teacher can cancel their own reservation.

---

## Story 2 - Classroom Visibility (Student)

As a student, I want to view classroom availability in real time so that I can see where lectures are scheduled and which rooms are free.

- The system displays available and reserved classrooms.
- The student can filter by building, day, and time slot.
- The system shows the teacher who booked the classroom.
- Availability updates automatically when a booking is created or canceled.

---

## Story 3 - Campus Infrastructure Management (Administrator)

As an administrator, I want to manage buildings and classrooms so that classroom availability information remains accurate.

- The administrator can add, edit, or delete buildings.
- The administrator can add, edit, or delete classrooms.
- The administrator can define classroom capacity.
- The administrator can manage user roles and accounts.

---

## Technical Characteristics

- Spring Boot backend
- Login and registration using Spring Security
- Encrypted password storage using BCrypt
- Role-based access control (STUDENT / TEACHER / ADMIN)
- User profile page
- Session-based authentication
- File/image upload functionality (building floor plans)
- Responsive frontend developed using Bootstrap
- Real-time classroom availability updates
- Implementation of all agreed user stories
- Dockerized deployment
