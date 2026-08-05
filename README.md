# Shift Sheet

A personal timesheet and activity log app for fuel transport drivers, built to replace a paper timesheet with a fast, phone-friendly digital form.

## The Problem

As a fuel transport driver, I have to fill out a paper timesheet by hand every shift. For every stop on my route (typically 8-10+ stops per shift), I have to record:

- Location
- Invoice number
- Time arrived
- Time left
- Total time (calculated manually)
- Comments (activity — loading, unloading, fueling, inspection, etc.)
- Odometer/mileage reading

Mileage in particular just keeps incrementing stop to stop, so I'm rewriting most of the same number over and over. On top of that, at loading/unloading stops I also fill out a separate paper delivery ticket for the customer with its own invoice number, mileage, and times — meaning key data gets handwritten twice, on two different forms, every single stop.

## The Goal

Build a mobile-friendly web app that:

1. Replaces the paper timesheet with a fast, phone-based digital entry form
2. Reduces repetitive handwriting and manual re-entry (especially mileage and known/repeated locations)
3. Auto-calculates time-per-stop and daily totals instead of manual math
4. Outputs a completed PDF at the end of the shift that can be submitted to dispatch/payroll, matching the official company timesheet format

This isn't meant to replace the customer-facing delivery ticket — that stays a physical, signed paper document. The goal is just to eliminate the duplicate effort of also handwriting a separate internal timesheet.

**Note:** This is a personal project, not an officially sanctioned company tool. It's built as a real, deployed portfolio project to support a career transition into IT/cloud work.

## Status

Early build in progress. Page one (shift header, add-stop flow, auto-calculated time/mileage, PDF generation) is built and working on both desktop and mobile.

## Planned Tech Stack

- **Frontend:** HTML/CSS/JavaScript, hosted on AWS S3 + CloudFront
- **Backend:** AWS API Gateway + Lambda
- **Database:** DynamoDB
- **PDF generation:** A PDF library (e.g., PDFKit) run inside Lambda
