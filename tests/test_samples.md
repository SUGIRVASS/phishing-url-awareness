# Test Results

Python: 3.13.7
Operating system: Darwin
Date: 2026-11-06

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs found. This does NOT prove safety. | No listed warning signs found. This does NOT prove safety. | PASS |
| 2 | `http://192.0.2.10/account` | Uses an IP address instead of a familiar domain.<br>Uses HTTP. HTTPS alone does not prove trust. | Uses an IP address instead of a familiar domain.<br>Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3 | `http://example.com@sample.invalid/login` | Contains an @ symbol; inspect carefully.<br>Uses HTTP. HTTPS alone does not prove trust. | Contains an @ symbol; inspect carefully.<br>Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Contains many hostname segments/subdomains. | Contains many hostname segments/subdomains. | PASS |
| 5 | `https://xn--example.invalid/` | Contains a punycode-style hostname. | Contains a punycode-style hostname. | PASS |

## Notes

The checker examines URL text without connecting to websites.
These warning signs are clues, not proof of malicious activity.
A URL with no detected warnings is not necessarily safe.
