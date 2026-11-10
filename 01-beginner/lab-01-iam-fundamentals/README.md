# Lab 01: IAM Fundamentals

**Platform:** Okta + Entra ID
**Time:** 25-30 min
**Status:** Complete

## Objective
Practice the core tasks an IAM engineer handles every day in both Okta and Microsoft Entra ID.

## What I Did
- Created a test user in Okta and Entra ID
- Created an `Engineering-Team` group and assigned the user
- Reset the user's password
- Disabled the account
- Validated the changes with sign-in logs

Full walkthrough with screenshots: [STEPS.md](STEPS.md)

## Lessons Learned
- Groups make access easier to manage: change the group, not each user.
- Disable accounts instead of deleting them, so audit logs are kept.
- Always verify identity before resetting a password.
