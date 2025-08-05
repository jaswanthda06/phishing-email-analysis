# 📧 Phishing Email Analysis - Cybersecurity Internship Task 2

## ✅ Task Objective:
Oka suspicious email ni analyze chesi, phishing indicators ni identify cheyyadam.

## ✅ Tools Used:
- Gmail (Original Message headers view)
- MXToolbox Email Header Analyzer
- Browser for domain & IP blacklist checking

## ✅ Sample Email Details:
- **From:** Gautam Kumawat <support@hackingflix.com>
- **To:** jaswanth****@gmail.com
- **Subject:** 🗝️ Here's Your Login Link, JASWANTH KUMAR?
- **SPF Result:** PASS with IP 192.254.118.25
- **DKIM Result:** PASS with domain hackingflix.com
- **DMARC Result:** PASS

## ✅ Observations:
| Indicator | Result |
|-----------|--------|
| DMARC Compliance | ✅ PASS |
| SPF Authentication | ✅ PASS |
| DKIM Authentication | ✅ PASS |
| Source IP Address | 192.254.118.25 |
| Domain Name | hackingflix.com |

## ✅ My Findings:
- SPF, DKIM, DMARC all passed → technically email is authenticated.
- But **domain hackingflix.com** is not a well-known trusted brand (suspicious).
- IP Address `192.254.118.25` was found listed in spam blacklists (seen in header analysis earlier).
- **Sender name & domain mismatch** with the email content (hackingflix unrelated to login links).
- Social engineering possible — email uses personal name to gain trust.

## ✅ Conclusion:
Even though SPF, DKIM, DMARC passed, the **blacklisted IP** and **suspicious domain** indicate this could be a phishing attempt. Always verify sender authenticity beyond just header pass results.

