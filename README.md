# Timesheet-Report-Automation
This repository houses the script and workflow architecture model for the Automated Google Sheets Timesheet and PDF Reporting System.

# System Architecture
### EMPLOYEE INTERACTION LAYER              

Employee Arrives On-Site

          ↓
          
   Scan Site QR Code
   
          |
          v
          
 Complete Clock-In / Clock-Out Google Form
 
          |
          |
          v

Captured Data:
- Employee Name
- Job Site
- Clock-In Timestamp
- Clock-Out Timestamp
- Date
- Additional Timecard Information


                              |
                              v


  ### DATA COLLECTION LAYER


                 Google Forms Response Database

                              |
                              |
                              v


┌──────────────────────────────────────────────────────────────┐
│                DATA PROCESSING & AUTOMATION LAYER            │
└──────────────────────────────────────────────────────────────┘

                 Google Apps Script Automation Engine

                              |
        ------------------------------------------------
        |                     |                        |
        v                     v                        v

 Data Validation       Time Calculations        Workforce Logic

 - Validate entries    - Calculate hours       - Clock-in status
 - Detect duplicates   - Daily totals          - Active employee count
 - Normalize names     - Weekly totals         - Attendance tracking
 - Format timestamps   - Labor cost            - Missing clock-outs


                              |
                              v


┌──────────────────────────────────────────────────────────────┐
│                    PROCESSED DATA LAYER                      │
└──────────────────────────────────────────────────────────────┘

              Structured Workforce Timesheet Database

                              |
        ------------------------------------------------
        |                                              |
        v                                              v


┌───────────────────────────────┐        ┌───────────────────────┐
│     OPERATIONAL DASHBOARD     │        │ REPORTING AUTOMATION  │
└───────────────────────────────┘        └───────────────────────┘

Real-Time Workforce Tracking             Scheduled Daily Report

- Employees currently onsite              10:30 PM Trigger
- Active workforce count                        |
- Daily labor hours                           |
- Site labor costs                            v
- Weekly labor costs                   Google Apps Script Executes
                                                  |
                                                  v
                                      Collect Daily Workforce Data
                                                  |
                                                  v
                                        Generate PDF Report
                                                  |
                                                  v
                                      Automated Email Delivery


                              |
                              v


┌──────────────────────────────────────────────────────────────┐
│                    MANAGEMENT REVIEW LAYER                   │
└──────────────────────────────────────────────────────────────┘

Project Support Review

- Validate timecard accuracy
- Identify missing punches
- Review labor utilization
- Approve corrections


                              |
                              v


Leadership Review

Daily Operational Insights:
- Workforce attendance
- Labor expenditures
- Productivity trends
- Timekeeping exceptions
