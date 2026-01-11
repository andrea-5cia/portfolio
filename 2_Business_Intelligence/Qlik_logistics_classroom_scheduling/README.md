# 🏫 Classroom Utilization & Lesson Planning Dashboard  
**Qlik Sense – University Logistics Decision Support**

## 🎯 Objective
Design and develop an **interactive Business Intelligence dashboard** to support the **University logistics office** in planning and optimizing **classroom usage**, using:

- classroom capacity (effective seats),
- expected attendance (students enrolled in courses),
- teaching load (hours and scheduled commitments),
- time distribution (day/hour).

The dashboard supports decisions to:
- prevent overcrowding,
- detect under-utilized classrooms,
- improve scheduling efficiency and space allocation.

---

## 🧰 Tool
- **Qlik Sense**

---

## 📊 Dashboard Overview

### 🔹 Home – KPIs & Classroom Scatter
![Home Overview](images/1aule.png)

Entry point with:
- key KPIs (total classrooms, distinct commitments),
- interactive filters (activity type, building, effective capacity, department/degree),
- **scatter plot of classrooms** to visually spot usage patterns.

The scatter plot represents:
- **Hours of activity** on one axis,
- **Distinct commitments** on the other,
- enabling quick identification of heavily used vs low-usage classrooms.

---

### 🔹 Department Utilization – Summary & Space Distribution
![Department Utilization](images/2aule.png)

Department-level view combining:
- a summary table (hours, classrooms used, distinct commitments),
- a pie chart to show distribution across departments,
- a treemap to highlight the “space footprint” and utilization distribution by department/classroom.

---

### 🔹 Classroom Utilization – Detail View
![Classroom Detail](images/3aule.png)

Classroom-focused analysis including:
- a table of classrooms with **capacity**, **distinct commitments**, and **hours**,
- “Top classrooms” view to identify the most used spaces,
- comparison between **number of commitments** and **total hours** across classrooms (useful to spot scheduling concentration).

---

### 🔹 Planner – Time Slot Load (Day × Hour)
![Planner View](images/4aule.png)

Scheduling-oriented view showing how teaching load is distributed by:
- **hour of the day**
- **day of the week**

Useful to:
- identify peak congestion time slots,
- support rescheduling strategies to flatten demand.

---

### 🔹 Commitments Detail Table – Operational Drill-down
![Commitments Detail](images/5aule.png)

Record-level table designed for operational work:
- building and classroom,
- capacity,
- expected attendance,
- potential occupancy rate,
- course / teaching commitment details.

Supports quick verification and “case-by-case” resolution for critical classes.

---

### 🔹 Criticality Focus – Overcrowding & Under-occupation
![Criticality Analysis](images/6aule.png)

Dedicated monitoring views to classify critical situations:
- **Overcrowding** (>100%)
- **Under-occupation** (<75%)
- **Severe under-occupation** (<50%)

Enables targeted corrective actions:
- move classes to better-fitting rooms,
- consolidate low-attendance lessons,
- reduce pressure on saturated buildings/time slots.

---

### 🔹 Structures Map – Capacity by Building/Classroom
![Structure Map](images/7aule.png)

Treemap of the physical infrastructure:
- buildings → classrooms,
- relative capacity distribution.

Useful for:
- space planning,
- infrastructure reporting,
- identifying capacity concentration across campus.

---

## 🧠 Design Principles
- **Operational BI**: designed for daily decisions, not only reporting
- Strong interactivity (filters + drill-down)
- Clear separation between:
  - **load** (hours, commitments),
  - **capacity fit** (occupancy vs seats)
- Stakeholder-friendly visuals for non-technical users

---

## 🧩 Use Cases
- Classroom allocation planning
- Lesson scheduling optimization
- Prevention of overcrowding
- Detection of inefficient room usage
- Support for logistics office and academic planning

---

## ⚠️ Data Confidentiality
Due to institutional data privacy:
- raw datasets,
- planning systems,
- the full Qlik application  

are not publicly shared.  
Screenshots represent stakeholder-facing dashboard views.

---

## 📬 Author
**Andrea Sciarrillo**  
Data Analyst & Data Scientist  
📧 andreasciarrillo1998@gmail.com | [LinkedIn](https://linkedin.com/in/andrea598)

---

## 🏷️ License
MIT License © 2026 Andrea Sciarrillo
