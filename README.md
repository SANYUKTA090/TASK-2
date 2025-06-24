# TASK-2: Phishing Email Analysis

1) Objective
Analyze a phishing email sample to identify characteristics of spoofing, social engineering, and potential threat vectors using email headers and content clues.

2) Email Sample
- File analyzed: `sample-4.eml`
- Source: Internship-provided email sample

3) Phishing Indicators Identified
| Indicator                            | Description |
| Spoofed Sender                       | `manpowergroup.no` domain used, but SPF failed (SoftFail) |
| Untrusted IP                         | Sent from `91.227.208.189`, not authorized for that domain |
| Misleading Content                   | Vague unsubscribe notice with no service name |
| Social Engineering Attempt           | Designed to provoke action (response/click) |
| SPF/DKIM/DMARC Review                | SPF: SoftFail, DKIM: Pass, DMARC: Pass (but spoof still possible) |

4) Header Analysis Summary
- SPF: SoftFail → Suspicious sender
- DKIM: Pass
- DMARC: Pass
- Sent through: Microsoft SMTP but originating from `rs-189.mta.anpdm.com`

5) Conclusion
This email is likely phishing. The spoofed domain, failed SPF, and vague language point to a potential attack. Users should not respond or click on anything if such emails are received.

6) Tools Used
- Google Toolbox Header Analyzer: https://toolbox.googleapps.com/apps/messageheader/
- Manual header inspection
- Base64 decoder for email body

7) summary
This repository contains the analysis of a phishing email sample as part of a cybersecurity internship task. The analysis focuses on identifying signs of email spoofing, header anomalies, and social engineering techniques. Key findings include a failed SPF check, suspicious sender IP, and vague unsubscribe content — all common traits in phishing attempts. The analysis enhances awareness of email threats and practical skills in using tools like header analyzers.

8) email attachment
![image](https://github.com/user-attachments/assets/4150ce40-32b7-4787-bd9b-a0d82460fde2)
