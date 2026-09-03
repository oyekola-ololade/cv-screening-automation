# Security & Responsible Use

Candidate Screening handles a high-sensitivity domain. The current repository is a portfolio implementation under repair and must not be used with real candidate data without a substantially stronger security/governance layer.

## Do not use this repository version for

- real hiring decisions;
- real candidate CVs or protected personal information;
- public internet-facing intake without authentication/rate limiting;
- automated rejection without accountable human review;
- production retention of candidate records in a demonstration-oriented Google Sheet.

## Public-repository rules

- Never commit candidate names, emails, CV text, phone numbers, addresses, employment histories, or other PII.
- Never commit OpenAI, Google, webhook, or spreadsheet credentials.
- Use synthetic candidate fixtures only.
- Replace placeholder Sheet/resource IDs before controlled testing.
- Keep test credentials isolated from production accounts.

## Production requirements beyond this portfolio build

- authenticated intake and authorization;
- least-privilege data access;
- explicit retention/deletion policy;
- audit logs;
- encrypted transport/storage appropriate to the chosen services;
- bias/error evaluation and documented review criteria;
- human decision accountability and an appeal/review path;
- incident response and access revocation procedures.

Report sensitive issues privately to the repository owner rather than posting candidate or credential data in a public issue.
