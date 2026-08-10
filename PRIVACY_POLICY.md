# Privacy Policy

**Effective Date:** August 10, 2026  
**Last Updated:** August 10, 2026

## 1. Introduction

This Privacy Policy describes how **Innotel** ("we," "our," or "us") collects, uses, stores, and protects your information when you use our social media management service, Postiz, hosted at **psa.innotel.us** (the "Service").

Postiz is an open-source social media scheduling and management platform. This instance is self-hosted and operated by Innotel. By using the Service, you agree to the data practices described in this policy.

---

## 2. Information We Collect

### 2.1 Account Information
When you create an account, we collect:
- **Name** and **email address**
- **Password** (stored as a salted, hashed value — we never store plaintext passwords)
- **Profile picture** (if provided)
- **Organization/workspace name** (if applicable)
- **Language and timezone preferences**

### 2.2 Social Media Platform Connections
When you connect social media accounts to the Service, we collect and store:
- **OAuth access and refresh tokens** (encrypted at rest) for each connected platform
- **Platform usernames** and account identifiers
- **Granted OAuth scopes** and permissions
- **Content and engagement data** retrieved via platform APIs, including:
  - Posts, comments, and messages you create or schedule through the Service
  - Post-level analytics (impressions, clicks, reach, engagement metrics)
  - Audience aggregate data

**Important:** You authenticate directly with each social media platform (X, LinkedIn, Facebook, YouTube, etc.) through their official OAuth flows. We do not collect your raw social media passwords, and we never ask you to paste API keys into the Service.

### 2.3 Content You Provide
We store content you create, upload, or schedule through the Service, including:
- Text posts, captions, and hashtags
- Images, videos, and audio files
- Scheduling metadata (dates, times, recurrence)
- AI-generated content suggestions (if AI features are enabled)

### 2.4 Billing Information
If you subscribe to a paid plan:
- We collect billing email, address, and tax identification information
- **Payment card details are handled directly by Stripe**, our payment processor. We do not store or have access to your full credit card number — only a tokenized reference and the last four digits.

### 2.5 Usage and Technical Data
We automatically collect certain information when you access the Service:
- **IP address** and derived approximate location (country/region)
- **Browser type** and operating system
- **Device identifiers**
- **Session timestamps** and authentication logs
- **Pages visited** and features used within the Service
- **Error and crash reports**

### 2.6 AI Feature Data
If you use AI-assisted features (captions, hashtags, image generation), the prompts and content you submit are transmitted to third-party AI model providers as sub-processors.

---

## 3. How We Use Your Information

We use the information we collect for the following purposes:

| Purpose | Description |
|---|---|
| **Service Delivery** | To schedule and publish posts to your connected social media accounts, retrieve analytics, and provide the core functionality of the Service |
| **Account Management** | To authenticate you, maintain your account, and provide customer support |
| **Billing** | To process payments, manage subscriptions, and send invoices |
| **Improvement** | To analyze usage patterns, diagnose technical issues, and improve the Service |
| **Security** | To detect and prevent fraud, abuse, and unauthorized access |
| **Communication** | To send service-related notifications, updates, and (with your consent) marketing communications |
| **Legal Compliance** | To comply with applicable laws, regulations, and legal requests |

We do **not** sell your personal information. We do **not** use your content or social media data to train machine learning models.

---

## 4. Data Storage and Security

### 4.1 Hosting Infrastructure
This Service is **self-hosted** on infrastructure controlled by Innotel. All data is stored on servers under our direct control using the following technologies:

| Component | Purpose |
|---|---|
| **PostgreSQL 17** | Primary application database (user accounts, posts, schedules, settings) |
| **PostgreSQL 16** | Temporal workflow engine database (job execution history, scheduled post states) |
| **Redis 7** | Caching, session data, and job queues |
| **Elasticsearch 7** | Temporal workflow visibility and execution history indexing |
| **Local file storage** | Uploaded media (images, videos, audio) |

### 4.2 Security Measures
We implement industry-standard safeguards to protect your data:
- **Encryption in transit:** All connections to the Service are encrypted using TLS (HTTPS)
- **Encryption at rest:** OAuth tokens and sensitive credentials are encrypted before storage
- **Password hashing:** All passwords are salted and hashed using secure, one-way algorithms
- **Access control:** Role-based access controls limit who can view or modify data
- **Regular updates:** We apply security patches and updates to all infrastructure components
- **Monitoring:** We log authentication events and monitor for suspicious activity

### 4.3 Data Location
Your data is stored on servers in the United States. By using the Service, you consent to the transfer and storage of your information in this jurisdiction.

---

## 5. Third-Party Services and Sub-Processors

To provide the Service, we rely on the following third-party services which act as data sub-processors:

### 5.1 Social Media Platforms
When you connect accounts, data is exchanged with the following platforms per your authorization:

| Platform | Data Shared | Purpose |
|---|---|---|
| **X (Twitter)** | Posts, media, analytics | Publishing and retrieving engagement data |
| **LinkedIn** | Posts, media, analytics | Publishing and retrieving engagement data |
| **Facebook / Instagram** | Posts, media, analytics | Publishing and retrieving engagement data |
| **YouTube** | Videos, metadata, analytics | Publishing and retrieving engagement data |
| **TikTok** | Videos, metadata, analytics | Publishing and retrieving engagement data |
| **Pinterest** | Pins, media, analytics | Publishing and retrieving engagement data |
| **Reddit** | Posts, comments | Publishing content |
| **Discord** | Messages, embeds | Publishing content to channels |
| **Slack** | Messages, files | Publishing content to workspaces |
| **Mastodon** | Posts, media | Publishing to federated instances |
| **Threads** | Posts, media | Publishing content |
| **Dribbble** | Shots, media | Publishing design content |
| **GitHub** | Repository content | Publishing and managing content |
| **Beehiiv** | Newsletter content | Publishing and managing newsletters |

Each platform has its own privacy policy governing how they handle your data. We encourage you to review each platform's privacy practices.

### 5.2 Payment Processing
- **Stripe, Inc.** — Processes subscription payments. Stripe receives your payment card details directly; we never see or store your full card number. [Stripe Privacy Policy](https://stripe.com/privacy)

### 5.3 AI Services (If Enabled)
- **OpenAI, L.P.** — Processes prompts for AI-generated captions, hashtags, and content suggestions. Under OpenAI's API data usage policy, data submitted through the API is not used to train or improve their models. See [OpenAI's API data usage policy](https://openai.com/enterprise-privacy) for details.

### 5.4 Analytics and Error Tracking (If Configured)
We may optionally use error tracking services to diagnose and resolve technical issues. Currently, no external analytics or error tracking services are active. If enabled in the future, specific services will be listed here and you will be notified.

We do not sell or share your personal data with third parties for their own marketing purposes.

---

## 6. Data Retention

| Data Category | Retention Period |
|---|---|
| **Account information** | Retained for the life of your account plus 90 days after deletion |
| **Posts and content** | Retained until you delete them or delete your account |
| **Uploaded media** | Retained until you delete the associated content or your account |
| **OAuth tokens** | Retained until you disconnect the platform or delete your account |
| **Billing records** | Retained for 7 years (for tax and legal compliance) |
| **Usage logs** | Retained for up to 90 days |
| **Temporal workflow history** | Retained per Temporal's default namespace configuration; typically 3–30 days of execution history |
| **Backups** | If configured, backup snapshots are retained for up to 30 days |

Upon account deletion, your personal data is removed from our active systems. Data may persist in encrypted backups (if configured) for up to 30 days before permanent deletion. Temporal workflow execution records are subject to Temporal's built-in retention policies and will expire automatically.

---

## 7. Your Rights

Depending on your jurisdiction, you may have the following rights regarding your data:

| Right | Description |
|---|---|
| **Access** | Request a copy of the personal data we hold about you |
| **Rectification** | Correct inaccurate or incomplete data |
| **Deletion** | Request deletion of your personal data |
| **Portability** | Receive your data in a structured, machine-readable format |
| **Restriction** | Limit how we process your data in certain circumstances |
| **Objection** | Object to processing based on legitimate interests |
| **Withdraw Consent** | Withdraw consent where processing is based on consent |

To exercise any of these rights, contact us at the email address listed in Section 10. We will respond within 30 days. You may also manage many of these directly through your account settings within the Service.

If you are located in the European Economic Area (EEA) or the United Kingdom, you have the right to lodge a complaint with your local data protection supervisory authority.

---## 8. Cookies and Tracking

The Service uses the following cookies set by the Postiz application:

| Cookie | Purpose | Duration |
|---|---|---|
| **Session / JWT tokens** | Authenticate your identity and maintain your login session | Session to 30 days |
| **CSRF tokens** | Prevent cross-site request forgery attacks | Session |
| **Preference cookies** | Remember your UI preferences (language, timezone, theme) | Up to 1 year |

You can control cookies through your browser settings. Disabling essential cookies may prevent the Service from functioning properly.

We do not use third-party advertising cookies or tracking pixels for ad targeting.

---

## 9. Children's Privacy

The Service is not intended for individuals under the age of 16. We do not knowingly collect personal information from children. If you believe a child has provided us with personal data, please contact us immediately.

---

## 10. Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of material changes by:
- Posting the updated policy at https://psa.innotel.us/privacy
- Sending an email to the address associated with your account (for significant changes)
- Displaying a notice within the Service

Your continued use of the Service after changes take effect constitutes acceptance of the updated policy.

---

## 11. Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or our data practices, please contact us:

**Innotel**  
**Email:** admin@innotel.us  
**Website:** https://psa.innotel.us  
**Privacy Policy:** https://psa.innotel.us/privacy

For urgent privacy or security concerns, including suspected data breaches, please include "PRIVACY" or "SECURITY" in your email subject line for priority handling.

---

## 12. Legal Basis for Processing (EEA & UK Users)

For users in the European Economic Area and the United Kingdom, we process your personal data on the following legal bases:

| Processing Activity | Legal Basis |
|---|---|
| Account creation and Service delivery | Performance of a contract |
| Billing and payment | Performance of a contract |
| Security monitoring | Legitimate interest |
| Service improvement analytics | Legitimate interest (or consent, where required) |
| Marketing communications | Consent |
| AI feature inputs | Consent |
| Legal compliance | Legal obligation |

---

*This privacy policy applies solely to the self-hosted Postiz instance operated by Innotel at psa.innotel.us. It does not apply to postiz.com or any other Postiz deployment operated by third parties.*
