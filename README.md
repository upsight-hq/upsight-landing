# Upsight Waitlist Landing Page

Public landing page for Upsight waitlist signups, built with static HTML and published via GitHub Pages.

## Overview

This repository contains a static landing page that explains Upsight's value proposition to Shopify app developers and collects waitlist signups. Each signup is recorded with:
- Email address
- Source (utm parameters, referrer, or "direct")
- Timestamp

## Features

- Responsive design for mobile and desktop
- Form validation for email addresses
- Source tracking from URL parameters and referrer
- Integration with Upsight API for signup storage
- GitHub Pages hosting (automatic)

## How Signups Work

1. Visitor lands on the page via a link (with utm parameters for tracking)
2. Visitor enters email and clicks "Join the waitlist"
3. Form captures:
   - Email address
   - Source (from `utm_source`, `utm_medium`, `utm_campaign`, referrer, or "direct")
4. Data is sent to the Upsight API (`/waitlist/signup`)
5. API stores the signup in the database with timestamp
6. Signups are accessible via `/waitlist/signups` endpoint

## Deployment

This page is automatically published to GitHub Pages at:
`https://upsight-hq.github.io/upsight-landing/`

Any push to the main branch triggers automatic deployment.

## Development

The site is entirely static HTML with vanilla JavaScript - no build process needed.

To test locally, open `index.html` in a browser. Note: the signup form will not work in local development without a backend connection.
