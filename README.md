# ExpiryScanApp

## Overview
ExpiryScanApp is an Android mobile application that scans product expiration dates using the device camera and OCR, validates them locally, and provides clear status feedback to the user.

The app is designed for healthcare, warehouse, retail, and home inventory use where expired products must be quickly identified and logged.

---

## Core Features

### 1. Camera-Based Scanning
- Uses device camera to capture expiration dates
- Supports common formats:
  - MM/YY
  - MM/YYYY
  - MM-DD-YYYY
  - YYYY-MM-DD
- Handles partial or unclear dates conservatively

### 2. OCR (On-Device)
- Uses **on-device OCR only**
- No cloud processing
- Works offline
- Privacy-first design

### 3. Date Validation Logic
Each scanned item is assigned one of three statuses:

- **VALID**
  - Expiration date is beyond warning threshold
- **WARNING**
  - Expiration date within configurable window (default: 30 days)
- **EXPIRED**
  - Expiration date has passed

Invalid or unreadable dates are flagged for manual review.

---

## Batch Scan Session
- Users can scan multiple items in one session
- Results displayed as a list with:
  - Date
  - Status (color-coded)
  - Confidence indicator
- Session persists until user manually clears it

---

## User Configuration
- Warning window is **user-configurable**
- Default: 30 days
- Future expansion may allow category-based thresholds

---

## Platform & Tech Constraints
- Platform: Android
- Framework: Expo (v54)
- OCR: On-device ML Kit
- Camera: Expo-compatible camera library
- No account login required
- No cloud dependency

---

## Non-Goals (Explicitly Out of Scope)
- No inventory syncing
- No cloud storage
- No user accounts
- No ads
- No analytics tracking

---

## Development Status
- Repository initialized
- App concept finalized
- README is the authoritative design reference
- Next step: implement buildable skeleton app
