---
layout: essay
type: essay
title: "Final Project Idea"
date: 2025-04-01
published: true
labels:
  - Software Engineering
  - Nextjs
---

## Overview

### The Problem

While commuting to UH Mānoa, some students have reported feeling uneasy in certain areas due to recurring encounters with individuals exhibiting unusual behavior — such as frequently standing in the same spot or shouting late at night. These situations may not be urgent or criminal but still contribute to discomfort, especially when walking alone or after dark.

These incidents are rarely documented or analyzed, often shared only through rumors or social media. Without a structured way to report and visualize these experiences, the community lacks both awareness and a means to respond compassionately and constructively.

### The Solution

This app allows UH Mānoa students and residents to report non-urgent but concerning encounters in the campus area. Users can anonymously report “suspicious locations” or “frequently seen individuals” using a simple form, and those reports will be visualized on a map using color-coded pins based on the number of similar reports.

In addition, the app will display nearby support services (like shelters, food banks, or mental health care), helping bridge the gap between concerned community members and those who may need assistance. It also allows reports to be sent to relevant organizations such as campus security, welfare nonprofits, or DPS, depending on the severity level.

Collected data will be visualized using D3.js to show heatmaps of frequently reported areas and time-based trends. The app will also suggest safer walking routes that avoid high-report zones.

---

## Names of the proposers

Rei Fukuzawa

---

## Mockup Page Ideas

1. **Home / Map Page**  
   - Google Maps embedded with pins showing user reports  
   - Filter by severity (Safe, Caution, Danger)

2. **Report Page**  
   - Form for submitting a new report (location, time, description, perceived level)

3. **Support Services Page**  
   - List/map of nearby shelters, food banks, and support organizations

4. **Safety Route Finder**  
   - Input current location and destination → suggests safest walking route

5. **Data Dashboard**  
   - D3.js graphs showing weekly trends, heatmaps, and common report locations

6. **Login Page**  
   - Firebase Auth (Google or UH email)

---

## Use Case Ideas

- A student walking home from late class wants to check if any areas have been flagged recently.
- A user reports a non-threatening but strange interaction with someone near a bus stop.
- A student feels uncomfortable seeing someone sleeping near a study area every day and wants to make a compassionate report.
- Campus security uses the heatmap data to increase patrols in certain locations.
- A support organization uses the reports to plan outreach activities.

---

## Beyond the Basics

- **Severity-based thresholds**: Only display reports about individuals if multiple users confirm similar concerns, to prevent false reporting or bias.
- **Anonymity-first design**: Users can report without creating an account; login is only needed for route and data analysis tools.
- **Support-first mindset**: Instead of labeling people as “dangerous,” reports emphasize behavior and context to avoid discrimination.
- **Community collaboration**: Potential partnerships with UH’s DPS, social work orgs, and community service offices.

---

