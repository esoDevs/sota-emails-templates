# sotita-emails-templates

HTML email templates for Sotita authentication flows. All templates use inline styles and Spanish copy.

## Templates

| Template | Purpose | Variables |
| --- | --- | --- |
| templates/reset_password.html | Password reset verification code | `{{ .Token }}`, `{{ .CurrentYear }}` |
| templates/confirm_signup.html | Confirm signup email | `{{ .ConfirmationURL }}`, `{{ .CurrentYear }}` |
| templates/change_email_address.html | Confirm email change | `{{ .NewEmail }}`, `{{ .ConfirmationURL }}`, `{{ .CurrentYear }}` |
| templates/invite_user.html | Invite a user to create an account | `{{ .ConfirmationURL }}`, `{{ .CurrentYear }}` |
| templates/magic_link.html | Magic link login | `{{ .ConfirmationURL }}`, `{{ .CurrentYear }}` |
| templates/reauthentication.html | Reauthentication verification code | `{{ .Token }}`, `{{ .CurrentYear }}` |

## Notes

- Placeholders use Go template syntax: `{{ .Field }}`
- The templates are designed for 600px width and include a fallback link or code block
