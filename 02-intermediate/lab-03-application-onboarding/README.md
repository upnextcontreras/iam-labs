# Lab 03: Application Onboarding

**Platform:** Okta + Entra ID · **Time:** 35-40 min · **Status:** Complete

## Why This Matters
One of the first tasks in a real IAM role is application onboarding: connecting apps to the company's identity system. It's how employees get into tools like Zoom, Salesforce, or Slack with one login instead of a separate password for each app.

## Scenario
> **New App Integration Request** (from HR Operations Manager)
> We just purchased a new SaaS app for our team. Can you add it to our identity platform so employees can log in with their company credentials?

**My job:** Add the app to Okta or Entra ID, configure SSO, and (optionally) enable user provisioning.

## What I Did
- Added applications from the app catalogs in Okta and Entra ID
- Configured SAML single sign-on settings
- Assigned users and groups to the applications
- Reviewed how SCIM provisioning creates accounts in the app automatically

Full walkthrough with screenshots: [STEPS.md](STEPS.md)

## Lessons Learned
- Assign apps to groups, not individual users, so access follows group membership.
- SSO setup means exchanging SAML metadata (Entity ID, ACS URL, certificate) with the app owner.
- SSO handles login, but provisioning (SCIM) is what creates the account in the app.
