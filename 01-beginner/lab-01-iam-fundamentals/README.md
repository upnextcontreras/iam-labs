# Lab 01: IAM Fundamentals

**Platform:** Okta + Entra ID · **Time:** 25-30 min · **Status:** Complete

## Why This Matters
Every organization needs to control who can access its systems. IAM works like the security guard for digital systems: it decides who gets in and what they can do once inside.

## Scenario
> **Your First IAM Task** (from IT Manager)
> Welcome to the team! Get familiar with our identity platform. Create a test user in both Okta and Entra ID, add them to a group, and confirm they can sign in. This is the foundation for everything else you'll do here.

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
