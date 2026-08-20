# Hospital-Queue-Management
Hospital Queue Management is a C language project used to manage patients in a hospital using the **Queue Data Structure**. It follows the **FIFO (First In First Out)** method, where the first patient entering the queue is treated first. The system stores patient details, displays the queue, and removes treated patients.
# 🏥 Hospital Queue Management System

## 📌 Project Overview

The **Hospital Queue Management System** is a simple software application designed to manage patients in a hospital queue efficiently. Instead of maintaining a manual queue, the system generates a unique token number for every patient and processes patients in an organized order.

The main goal of this project is to **reduce waiting time, avoid confusion, and make patient management easier for hospital staff and doctors**.

---

## 🎯 Objectives

* Generate a unique token for every patient.
* Maintain patients in an organized queue.
* Display the current and next patient.
* Allow the doctor/receptionist to serve the next patient.
* Remove served patients from the queue.
* Reduce manual work and patient confusion.

---

## ✨ Main Features

* 👤 Patient registration
* 🎫 Automatic token generation
* 📋 Queue display
* ➡️ Next patient functionality
* 🗑️ Remove served patient
* 🔢 Display current queue size
* 💻 Simple and user-friendly interface

---

## ⚙️ Working

The system follows the **FIFO (First In, First Out)** principle.

```text
Patient Registration
        ↓
Generate Token
        ↓
Add Patient to Queue
        ↓
Doctor Calls Next Patient
        ↓
Patient is Served
        ↓
Remove Patient from Queue
```

For example:

```text
Patient A → Token 101
Patient B → Token 102
Patient C → Token 103

Current Patient → 101
Next Patient    → 102
```

---

## 💻 Basic Queue Implementation

The following C++ code demonstrates the core queue functionality used in the project:

```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> patients;

    // Adding patients
    patients.push(101);
    patients.push(102);
    patients.push(103);

    cout << "Current Patient: "
         << patients.front() << endl;

    // Patient is served
    patients.pop();

    cout << "Next Patient: "
         << patients.front() << endl;

    cout << "Patients Waiting: "
         << patients.size() << endl;

    return 0;
}
```

### Output

```text
Current Patient: 101
Next Patient: 102
Patients Waiting: 2
```

---

## 👨‍⚕️ Patient Registration Example

A simple patient structure can be used to store patient information:

```cpp
struct Patient {
    int token;
    string name;
    int age;
};

Patient p1;

p1.token = 101;
p1.name = "Rahul";
p1.age = 25;
```

Patients can then be stored in a queue:

```cpp
queue<Patient> patientQueue;

patientQueue.push(p1);
```

The next patient can be accessed using:

```cpp
Patient current = patientQueue.front();

cout << "Token: " << current.token << endl;
cout << "Name: " << current.name << endl;
```

---

## 🛠️ Technologies Used

* **Language:** C++
* **Concept:** Queue / FIFO
* **Data Structure:** Queue
* **IDE:** VS Code / Code::Blocks
* **Version Control:** Git & GitHub

> The technology stack can be modified if the project uses a web-based implementation.

---

## 📂 Project Structure

```text
Hospital-Queue-Management/
│
├── main.cpp
├── README.md
└── .gitignore
```

---

## 🚀 How to Run

### Clone the repository

```bash
git clone https://github.com/your-username/hospital-queue-management.git
cd hospital-queue-management
```

### Compile

```bash
g++ main.cpp -o hospital_queue
```

### Run

```bash
hospital_queue
```

---

## 📈 Advantages

* Reduces manual queue management.
* Makes patient processing systematic.
* Easy to implement and understand.
* Demonstrates practical use of the **Queue data structure**.
* Can be upgraded into a complete hospital management system.

---

## 🔮 Future Scope

The project can be further improved by adding:

* Online appointment booking
* Doctor and department selection
* Emergency patient priority queue
* SMS/notification system
* Web or mobile application
* Database for storing patient records
* Estimated waiting-time display

---

## 👨‍💻 Author

**Pruthviraj Patil**
B.Tech – Computer Science & Engineering

---

### ⭐ Project Summary

> **Hospital Queue Management System uses the Queue data structure to organize patients according to their arrival time, providing a simple and efficient approach to hospital queue management.**
