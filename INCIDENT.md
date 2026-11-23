# Secret Leak Incident Response

## Scenario
A fake registry token was accidentally committed to Git.

## Response Procedure
1. Revoke or rotate the exposed token immediately.
2. Remove the secret from Git history.
3. Add automated secret scanning to prevent future leaks.
4. Verify that the replacement token is stored securely.

## Lesson Learned
Deleting a secret from a file does not remove it from Git history.
