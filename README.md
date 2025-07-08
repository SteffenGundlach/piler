![test workflow](https://github.com/jsuto/piler/actions/workflows/test.yaml/badge.svg)

piler is an open source email archival application. Please visit https://www.mailpiler.org/ for more.

Features:

- built-in smtp server
- archival rules
- retention rules
- legal hold
- message and attachment deduplication
- message compression
- message encryption
- digital fingerprinting and verification
- full text search
- simple and expert search
- save search criteria
- tagging emails
- view, export, restore emails
- bulk import/export messages
- access control
- AD / LDAP authentication
- IMAP, POP3 authentication
- single sign-on (SSO)
- Google Apps support
- Office 365 support
- STARTTLS support
- Google Authenticator support for 2-factor authentication
- i18n
- customisable theme
- audit logs
- search in audit logs
- online status info
- accounting
- recognised formats: PST, EML, Maildir, mailbox

## Smarthost forwarding

Archived emails can optionally be forwarded to an external SMTP server once they
have been stored. Set `smtp_forward` to the hostname (and optional port) of the
smarthost in `piler.conf`. Authentication and TLS are supported via the
following options:

- `smtp_forward_tls` – enable TLS for the connection
- `smtp_forward_user` and `smtp_forward_password` – credentials for SMTP AUTH
- `smtp_forward_timeout` – connection timeout in seconds
- `smtp_forward_envelope_from` – override the envelope sender

If these parameters are defined, each message will be sent to the configured
server immediately after archiving.
