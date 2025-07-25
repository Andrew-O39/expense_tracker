# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project does not yet follow semantic versioning (still in development).

## [Unreleased]

### Added
- User registration and login functionality
- Budget creation and category-based tracking
- Expense logging for user-defined budgets
- Support for period-based and category-based expense views
- Budget alert system based on usage thresholds:
  - 50% (half-limit)
  - 80–99% (near-limit)
  - 100%+ (limit-exceeded)
- HTML-based email templates using Jinja (`email_alert.html`)
- Email alert notifications for budget usage via SendGrid
- Dynamic username inclusion and year rendering in email templates
- Enhanced email layout with clear visual alert icons and structure
- **Spending summary endpoint**:
  - Supports optional category filtering
  - Groups and aggregates expenses by time period (`weekly`, `monthly`, `yearly`)
  - Real-time summary calculation based on `created_at` timestamps
  - Returns structured data using Pydantic response models

### Improved
- Overall alert messaging structure and logic
- Email deliverability (successfully sending authenticated emails via SMTP/SendGrid)
- Reduced risk of alert duplication through alert log checks
- Normalized category and period input to avoid mismatches in queries

---

## [0.1.0] – Project initialized

### Added
- Project scaffolding and development environment setup