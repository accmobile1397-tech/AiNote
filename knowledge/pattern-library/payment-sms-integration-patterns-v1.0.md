# Payment & SMS Integration Patterns

## Version 1.0

---

# 1. General Principle

Payment and SMS integrations must follow a configurable provider architecture.

The system should not be tightly coupled to one provider.

Default providers are selected for initial deployment, but the architecture must support adding new providers in the future.

Principles:

- Provider Abstraction First
- Configurable Integration
- Admin Controlled Management
- User Request Workflow
- Future Provider Expansion Ready

---

# 2. Payment Integration Pattern

## Default Payment Gateway

Default provider:

- ZarinPal

All projects should use ZarinPal as the initial payment gateway unless project requirements require another provider.

---

# Payment Gateway Architecture

Payment system should support:

- Multiple payment providers
- Provider switching
- Provider configuration
- Default provider selection

Architecture:

```text
Payment Service
      ↓
Payment Provider Interface
      ↓
Provider Implementations
```

Examples:

- ZarinPal
- Other Payment Gateways

---

# Admin Payment Management

Admin Panel must provide:

## Gateway Management

Admin can:

- Add payment gateways
- Configure credentials
- Enable / Disable gateway
- Set default gateway
- Test connection
- View gateway status

---

# User Payment Preferences

Users should be able to:

- View available payment methods
- Select preferred default payment gateway (when allowed)

The system should respect:

- User preference
- System availability
- Admin policies

---

# New Gateway Request Workflow

Users may request a new payment gateway.

Flow:

```text
User Panel
    ↓
Request New Gateway
    ↓
Admin Panel Review
    ↓
Approve / Reject
    ↓
Implementation / Configuration
    ↓
Enable for Users
```

---

# 3. SMS Integration Pattern

## Default SMS Provider

Default provider:

- IPPanel

All projects should use IPPanel as the initial SMS provider unless requirements require another provider.

---

# SMS Architecture

SMS system should support:

- Multiple SMS providers
- Provider abstraction
- Provider switching
- Default provider selection

Architecture:

```text
Notification Service
      ↓
SMS Provider Interface
      ↓
SMS Provider Implementations
```

Examples:

- IPPanel
- Other SMS Providers

---

# Admin SMS Management

Admin Panel must provide:

## SMS Provider Management

Admin can:

- Add SMS providers
- Configure API credentials
- Enable / Disable providers
- Set default SMS provider
- Test SMS connection
- Monitor status

---

# User SMS Preferences

Users can:

- View available SMS services
- Select preferred SMS provider when applicable

System manages:

- Availability
- Cost
- Priority

---

# New SMS Provider Request Workflow

```text
User
  ↓
Request SMS Provider
  ↓
Admin Review
  ↓
Approve / Reject
  ↓
Configuration
  ↓
Activation
```

---

# 4. Security Rules

Payment and SMS credentials must:

- Never be stored in frontend code
- Use secure environment variables
- Have access control
- Be hidden from normal users
- Be auditable

---

# 5. Future Expansion

The system should be ready for:

Payment:

- Multiple gateways
- International gateways
- Subscription billing
- Refund management

SMS:

- Multiple providers
- Smart routing
- Cost optimization
- Failover strategy

---

**End of Pattern — Version 1.0**
