  # ULMS WinForms Application — Software Testing Portfolio

  ## Disclaimer

  This repository contains work completed as part of a university assignment. **The main application (`ULMSWinFormsApp`) was provided by the university and was
  authored by Lusukama Selemani (ICT Senior Lecturer / Microsoft Certified Trainer).** I do not claim ownership of, nor take credit for, the application code
  itself.

  This project is hosted on my GitHub solely to demonstrate my software testing skills and serve as a portfolio piece for prospective employers and collaborators.
  I have no intention of selling, redistributing, or claiming this system as entirely my own work.

  ---

  ## What Was Provided (University)

  The `ULMSWinFormsApp` project is the **Umoja Learning Management System (ULMS)**, a .NET WinForms desktop application built for educational and assessment
  purposes. It includes:

  - **Login Form** — Authentication with hardcoded credentials
  - **Dashboard** — Central navigation hub linking to all modules
  - **Student Registration** — Captures student details with age validation
  - **Course Enrollment** — Enrolls students into predefined courses
  - **Marks Capture** — Records subject marks, calculates averages, and determines pass/fail status
  - **Reports** — Generates simulated student, marks, and enrollment reports
  - **3 Data Models** — `Student`, `Enrollment`, and `MarkRecord`

  The application contains **intentionally planted defects** (e.g. missing input validation, a deliberate performance bottleneck, weak business-rule enforcement)
  designed as testing scenarios for the assignment.

  ## What I Created (My Work)

  The `testingProject` is **entirely my own work**, built using **MSTest (.NET)** to test the provided application. It contains:

  ### Functional Tests (15 tests)
  | ID | Area | Description |
  |----|------|-------------|
  | TC-01 | Login | Valid credentials return success |
  | TC-02 | Login | Invalid credentials are rejected |
  | TC-03 | Login | Correct username with wrong password is rejected |
  | TC-04 | Login | Empty credentials are rejected |
  | TC-05 | Enrollment | Valid enrollment data is stored correctly |
  | TC-06 | Enrollment | Empty course name should fail validation |
  | TC-07 | Enrollment | Duplicate enrollment should be rejected |
  | TC-08 | Marks | Average calculation correctness |
  | TC-09 | Marks | Non-numeric input is handled gracefully |
  | TC-10 | Marks | Negative marks should be rejected |
  | TC-11 | Marks | Boundary test — pass threshold at 50 |
  | TC-12 | Marks | All-zero marks produce a fail result |
  | TC-13 | Marks | All-maximum marks produce correct average |
  | TC-14 | Reports | Marks report average is accurate |
  | TC-15 | Reports | Missing report type shows appropriate message |

  ### Non-Functional Tests (7 tests)
  | ID | Category | Description |
  |----|----------|-------------|
  | NFT-01 | Performance | Report generation completes within 2 seconds |
  | NFT-02 | Performance | Login responds within 1 second |
  | NFT-03 | Security | Correct username alone does not grant access |
  | NFT-04 | Security | Correct password alone does not grant access |
  | NFT-05 | Security | SQL injection attempts are rejected |
  | NFT-06 | Reliability | 100 rapid login attempts without crashing |
  | NFT-07 | Reliability | Alternating valid/invalid logins remain stable |

  Several tests are **intentionally designed to fail**, exposing the planted defects in the application (e.g. missing validation, incorrect calculations,
  performance issues). This is by design — the purpose is to demonstrate that the tests correctly identify bugs.

  ---

  ## Tech Stack

  - **Language:** C#
  - **Framework:** .NET 10.0 (Windows Forms)
  - **Testing:** MSTest SDK 4.0.2
  - **IDE:** Visual Studio 2026
  - **Version Control:** Git / GitHub

  ---

  ## Author

  **Joshua De Klerk**
  - Testing project and all test cases are my original work
  - Application code is credited to **Lusukama Selemani** (university lecturer)

  ## License

  This repository is for **educational and portfolio purposes only**. The application code remains the intellectual property of its original author. Not for
  commercial use or redistribution.
