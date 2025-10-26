# Requirement Analysis in Software Development

This repository provides a comprehensive overview of the Requirement Analysis process in the software development lifecycle (SDLC). It covers key concepts, activities, and artifacts used to define, document, and validate software requirements, using a booking management system as a practical example.

---

## What is Requirement Analysis?

Requirement Analysis is a crucial phase in the software development lifecycle (SDLC). It is the process of defining the expectations and needs of the users for a software system or product. This process involves discovering, analyzing, documenting, and validating all the requirements for the system.

The primary goal is to bridge the gap between stakeholders (like users, customers, and business managers) and the development team. By understanding *what* the system needs to do, *how* it should perform, and *what constraints* it must operate under, the team can build the *right* product. Its importance in the SDLC cannot be overstated, as errors or ambiguities found in the requirements phase are the most common cause of project failure and are significantly more costly to fix later in the development process.

---

## Why is Requirement Analysis Important?

A thorough Requirement Analysis is critical for the success of any software project. Its key benefits include:

* **Sets Clear Objectives:** It provides a clear, shared understanding of the project's goals for the development team, stakeholders, and end-users. This alignment prevents misunderstandings and "scope creep" (where the project's features expand uncontrollably).
* **Reduces Costs and Risks:** Identifying and correcting errors, inconsistencies, or missing requirements during this early phase is significantly cheaper and easier than fixing them after the code has been written. It minimizes the risk of building the wrong system.
* **Establishes a Basis for Planning and Validation:** Clearly defined requirements are the foundation for all project planning, cost estimation, and scheduling. Crucially, they serve as the basis for testing and validation. The quality assurance (QA) team uses these requirements to create test cases that verify the system works exactly as intended.

---

## Key Activities in Requirement Analysis

The Requirement Analysis process is typically broken down into the following key activities:

* **Requirement Gathering:** The initial step of collecting high-level requirements from all stakeholders (e.g., users, customers, business managers).
* **Requirement Elicitation:** The process of actively discovering and drawing out more detailed requirements. This involves techniques like stakeholder interviews, workshops, surveys, brainstorming sessions, and observing existing systems.
* **Requirement Documentation:** Formally documenting the elicited requirements in a clear, concise, and unambiguous way. Common artifacts include a Software Requirement Specification (SRS) document, user stories, and use cases.
* **Requirement Analysis and Modeling:** Analyzing the documented requirements to identify inconsistencies, ambiguities, or incompleteness. Modeling techniques (like use case diagrams, data flow diagrams, or entity-relationship diagrams) are often used to visualize the system's behavior, data, and structure.
* **Requirement Validation:** The process of ensuring that the documented requirements are correct, complete, and accurately reflect the stakeholders' needs. This is often done through formal reviews and walkthroughs with stakeholders to get their sign-off.

---

## Types of Requirements

Requirements are broadly classified into two categories: Functional and Non-functional.

**[USER ACTION]:** Please **replace** the generic examples below with specific requirements from your booking management project case study.

### Functional Requirements

Functional Requirements define *what* the system is supposed to do. They describe the specific behaviors, functions, or operations of the system.

**Examples (for a booking management project):**

* **User Authentication:** A user must be able to create an account using an email and password.
* **Search:** A user must be able to search for available listings (e.g., hotels, venues) based on location, date, and number of guests.
* **Booking:** A registered user must be able to select a listing and complete a booking for a specific date range.
* **Payment:** The system must process payments via credit card and PayPal.
* **Listing Management:** A "Host" user must be able to create, edit, and delete their own listings.

### Non-functional Requirements

Non-functional Requirements (NFRs) define *how* the system should perform. They describe the qualities, constraints, and operational characteristics of the system.

**Examples (for a booking management project):**

* **Performance:** The search results page must load in under 3 seconds, even with 10,000 active listings.
* **Security:** All user passwords must be hashed and salted before being stored in the database. All payment transactions must be encrypted using SSL.
* **Usability:** The booking process (from search to confirmation) must be completable by a new user in 5 steps or fewer.
* **Availability:** The system must have 99.9% uptime (be operational 99.9% of the time).
* **Compatibility:** The website must be fully responsive and functional on popular web browsers (Chrome, Firefox, Safari) and on mobile (iOS, Android) devices.

---

## Use Case Diagrams

A Use Case Diagram is a visual modeling tool used in Requirement Analysis. It illustrates the system's functionality by showing the relationships between "Actors" (users or other systems) and the "Use Cases" (the actions or goals the actor can achieve).

**Benefits:**
* Provides a high-level, easy-to-understand view of the system's scope.
* Helps identify *who* will interact with the system and *what* they need to do.
* Serves as an excellent communication tool for all stakeholders, both technical and non-technical.

### Example Diagram for the ALX Booking System

**[USER ACTION]:** You must create the diagram described below using a tool like `Draw.io` or `Lucidchart`. Export the diagram as `alx-booking-uc.png`, add it to your repository, and ensure the image link below works.

alx-booking-uc.png

**Guide for your diagram:**

* **Actors:**
    * **User (Guest):** A person browsing the site.
    * **Registered User:** A user who has logged in.
    * **Host (Owner):** A person who lists properties for booking.
    * **Admin:** A system administrator.
    * **Payment Gateway:** The external system that processes payments.
* **Use Cases:**
    * Search for Listing
    * View Listing Details
    * Create Account
    * Log In
    * Book Listing
    * Make Payment
    * Manage Bookings
    * Create Listing
    * Manage Listings
    * Manage Users
    * Process Refund

---

## Acceptance Criteria

Acceptance Criteria (AC) are a set of predefined conditions that a software feature must meet to be considered complete and accepted by a stakeholder (like the product owner or user). They are written from the end-user's perspective, are testable, and remove all ambiguity from a requirement.

**Importance:**
* They clearly define the "Definition of Done" for a feature or user story.
* They ensure everyone (developers, testers, stakeholders) is on the same page.
* They form the direct basis for acceptance testing.

### Example: Acceptance Criteria for "Checkout Feature"

**[USER ACTION]:** Please **review and adapt** this generic example to match the specific "Checkout feature" from your case study.

**User Story:** As a registered user, I want to review my selection and pay for my booking so that I can confirm my reservation.

**Acceptance Criteria:**

* **Scenario 1: Successful Payment (Credit Card)**
    * **Given** I am on the "Checkout" page
    * **And** I see a summary of my booking (listing name, selected dates, and total price).
    * **When** I fill in valid credit card information (Card Number, Expiry Date, CVC)
    * **And** I click the "Confirm and Pay" button
    * **Then** the payment is processed successfully.
    * **And** I am redirected to a "Booking Confirmation" page.
    * **And** I receive a confirmation email with my booking details.

* **Scenario 2: Failed Payment (Invalid Card)**
    * **Given** I am on the "Checkout" page
    * **When** I fill in invalid or expired credit card information
    * **And** I click the "Confirm and Pay" button
    * **Then** the payment is declined.
    * **And** I remain on the Checkout page.
* **And** I see a clear error message (e.g., "Your payment was declined. Please check your card details.").

* **Scenario 3: Apply Discount Code**
    * **Given** I am on the "Checkout" page
    * **And** I have a valid discount code
    * **When** I enter the code in the "Discount Code" field
    * **And** I click "Apply"
    * **Then** I see the total price updated to reflect the discount.
* **And** the discount amount is clearly displayed.
