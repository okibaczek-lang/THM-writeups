# CSRF - THM ROOM

## What is CSRF
CSRF (Cross-Site Request Forgery) allows an attacker to force a logged-in user’s browser to send unwanted authenticated requests using existing session cookies.

## Requirements
- user is authenticated
- browser sends cookies automatically
- no proper CSRF protection (token / SameSite / origin check)

## Exploitation

### Lab 1 (no protection)
- no CSRF protection on email change
- crafted HTML page triggered email change request in victim’s session

### Lab 2 (weak protection)
- CSRF token was predictable/not properly bound to session
- reused token allowed request execution via crafted HTML interaction

## Detection
- test state-changing actions (email/password/role)
- check if CSRF token exists and is validated
- try sending requests without/with modified token
- test cross-site request execution

## Impact
Account changes or privilege changes performed without user consent.
