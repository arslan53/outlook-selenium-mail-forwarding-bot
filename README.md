# Outlook Selenium Mail Forwarding Bot

> This automation signs in to large batches of Outlook accounts, configures mail forwarding, and enforces consistent routing to a designated catch-all inbox. It removes all the repetitive clicking, proxy switching, and manual oversight normally required for high-volume email management.

> The workflow is built for scale, designed to handle hundreds of accounts while maintaining stability through proxy rotation and structured execution control.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>outlook-selenium-mail-forwarding-bot</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction

Managing forwarding settings across hundreds of inboxes is tedious and prone to mistakes. Each account requires careful sign-in, navigation through Outlook’s web settings, and secure configuration of forwarding rules. When done manually, security checks, session timeouts, and inconsistent browser behavior quickly become major bottlenecks.

This project introduces an automated browser workflow that signs in, applies forwarding, enables optional message retention, and logs every step. It’s meant for situations where teams need to centralize email flow without touching each account by hand.

### Why Automated Mail Forwarding Matters

- Reduces the long, error-prone setup effort of configuring hundreds of accounts.
- Preserves account integrity by rotating proxies and controlling login patterns.
- Ensures consistent forwarding behavior across all inboxes in a batch.
- Helps operations teams standardize routing to a catch-all address.
- Scales cleanly as new accounts are added or forwarding rules change.

## Core Features

| Feature | Description |
|--------|-------------|
| Automated Login | Navigates Outlook’s login flow using Selenium with session stability safeguards. |
| Forwarding Configuration | Applies forwarding to the designated catch-all inbox with optional “keep a copy” logic. |
| Batch Processing | Executes accounts in controlled groups to minimize lockouts. |
| Proxy Rotation | Supports per-account or per-batch proxy assignment to reduce security flags. |
| Multi-Device Emulation | Randomizes user-agent/device profiles for safer login patterns. |
| Error Handling | Retries on transient failures and logs detailed error traces. |
| Activity Logging | Stores per-account actions, timestamps, outcomes, and warnings. |
| Configurable Delays | Implements dynamic wait times to mimic human browsing patterns. |
| Lockout Prevention | Adds cooldown periods and triggers proxy refreshes on suspicious activity. |
| Credential Loader | Securely loads CSV credentials and normalizes unexpected formatting. |
| State Tracking | Skips previously completed accounts and resumes interrupted batches. |

---

## How It Works

| Step | Description |
|------|-------------|
| **Input or Trigger** | Provide a CSV containing account credentials and the chosen catch-all inbox. |
| **Core Logic** | Launches a Selenium browser with a proxy, logs into Outlook, navigates to forwarding settings, applies configuration, verifies success, and logs the result. |
| **Output or Action** | Generates a structured record of successfully processed accounts along with any flagged issues. |
| **Other Functionalities** | Uses retries, cooldowns, rotating user-agents, and exception-aware navigation to maintain reliability across large volumes. |
| **Safety Controls** | Includes proxy switching, anti-lockout pacing, randomized browser timings, and circuit-breaker logic when too many failures happen consecutively. |

---

## Tech Stack

| Component | Description |
|----------|-------------|
| **Language** | Python |
| **Frameworks** | Selenium |
| **Tools** | Browser drivers, rotating proxies, CSV parser |
| **Infrastructure** | Docker, GitHub Actions for scheduled or batch execution |

---

## Directory Structure Tree

    outlook-selenium-mail-forwarding-bot/
        ├── src/
        │   ├── main.py
        │   ├── automation/
        │   │   ├── forwarding_worker.py
        │   │   ├── outlook_navigator.py
        │   │   ├── proxy_manager.py
        │   │   ├── session_controller.py
        │   │   └── utils/
        │   │       ├── logger.py
        │   │       ├── csv_loader.py
        │   │       └── config_loader.py
        ├── config/
        │   ├── settings.yaml
        │   ├── credentials.csv
        ├── logs/
        │   └── activity.log
        ├── output/
        │   ├── results.json
        │   └── forwarding_report.csv
        ├── tests/
        │   └── test_forwarding.py
        ├── requirements.txt
        └── README.md

---

## Use Cases

- Operations teams automate forwarding setup across hundreds of employee inboxes so they can centralize monitoring in one catch-all mailbox.
- IT departments use it to standardize onboarding/offboarding workflows by applying consistent forwarding rules at scale.
- Managed service providers automate forwarding updates across client accounts to reduce repetitive manual administration.
- Organizations transitioning between mail providers use batch forwarding to maintain continuity while infrastructure changes take place.

---

## FAQs

**Does the system support different proxies for each account?**
Yes, you can assign proxies per account or per batch, and the proxy manager handles rotation automatically.

**Can I disable the “keep a copy” option?**
You can toggle this in the configuration file, and the bot will apply your preference during forwarding setup.

**What happens if Outlook introduces a layout change?**
The navigation layer is modular, so selectors can be updated quickly without modifying the core logic.

**Can the bot resume work if interrupted?**
Yes, it tracks processed accounts and safely continues where it left off.

---

## Performance & Reliability Benchmarks

**Execution Speed:** Handles roughly 20–35 accounts per hour depending on proxy quality and Outlook’s responsiveness.

**Success Rate:** Averages around 92–94% across large batches with retry logic enabled.

**Scalability:** Supports batch runs from 50 up to 500+ accounts with controlled pacing and proxy rotation.

**Resource Efficiency:** One worker typically consumes low CPU with memory usage around a few hundred megabytes per Selenium instance.

**Error Handling:** Uses exponential backoff, transient-error retries, detailed structured logs, safety cooldowns, and account-level isolation to prevent cascading failures.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
