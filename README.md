# Hospitality-Booking-Analytics-with-Power-BI
Power BI dashboard built on a hospitality bookings dataset to analyze revenue, occupancy, RevPAR, cancellations, and property performance using a star-schema data model and DAX measures.

# Project Overview

This project implements a Power BI analytics solution for hospitality performance monitoring. It is built on a structured bookings dataset and focuses on revenue, occupancy, capacity utilization, and customer behavior across hotels, cities, room classes, and time periods. The objective is to convert raw booking data into a reliable analytical model and an interactive dashboard suitable for business reporting.

## Data Model

The solution uses a star-schema design with five core tables:

- __dim_date__: Provides calendar attributes including date, month-year, week number, and day type (weekday or weekend).
- __dim_hotels__:
  Contains property-level information such as property ID, property name, category (Luxury or Business), and city.
- __dim_rooms__:
  Defines room types and their corresponding room classes.

- __fact_bookings__: Stores transactional booking-level data including booking status, booking platform, guest count, ratings, and revenue details.

- ____fact_aggregated_bookings__:
Stores daily aggregated capacity and successful bookings by property and room type, used for occupancy and RevPAR calculations.

Relationships are defined using property ID, room category, and date fields to ensure correct filter flow and accurate aggregations.

## Key Metrics and Logic

Business metrics are implemented using DAX measures to ensure correct behavior under all filter contexts. Core metrics include:

- Total Revenue and Realized Revenue based on booking status rules
- ADR (Average Daily Rate)
- Occupancy Percentage
- RevPAR (Revenue per Available Room)
- Cancellation Percentage
- Realization Percentage
- Average Customer Rating

Revenue realization logic accounts for partial revenue loss on cancelled bookings and full realization for checked-out and no-show bookings.

## Dashboard Features 

The dashboard provides:

- KPI cards for high-level performance tracking
- Trend analysis by week for revenue, occupancy, and RevPAR
- Category-level revenue distribution
- Property-level performance tables with conditional formatting
- Slicers for city, property, room class, date, and booking platform

The design supports both summary-level monitoring and detailed drill-down analysis.

## Dashboard Preview


This section shows the final Power BI dashboard built on the hospitality bookings dataset. It highlights key performance indicators, trends, and property-level metrics used for analysis.

<img width="954" height="573" alt="image" src="https://github.com/user-attachments/assets/bb5cc0bb-28ab-4d80-bcf5-1ce655008a18" />

[DASH BOARD LINK (ACCESS DASHBOARD HERE)](https://app.powerbi.com/singleSignOn?pbi_source=desktop&ru=https%3A%2F%2Fapp.powerbi.com%2Fgroups%2Fme%2Freports%2F27c1b378-180b-4bae-bc02-36a055341ceb%3Fpbi_source%3Ddesktop%26noSignUpCheck%3D1)

## Tools and Technologies

- Power BI
- Power Query for data transformation
- DAX for metric calculation
- Star-schema data modeling
## Usage
This project can be used as a reference for:
- Hospitality and revenue analytics use cases
- Power BI data modeling and DAX implementation
- Building KPI-driven dashboards from transactional datasets

It demonstrates end-to-end capability from raw data modeling to business-ready analytical reporting.
