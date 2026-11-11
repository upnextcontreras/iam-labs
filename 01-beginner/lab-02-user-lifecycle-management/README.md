# Lab 02: User Lifecycle Management

**Platform:** Entra ID · **Time:** 25-30 min · **Status:** In Progress

## Why This Matters
User lifecycle management is the core of IAM. Every employee joins (Joiner), changes roles (Mover), and eventually leaves (Leaver). Managing this lifecycle securely and efficiently is what IAM engineers do every day.

## Scenario
> **HR System Sync Request** (from HRIS Team)
> Workday is now our system of record for employees. We need Entra ID accounts created automatically when HR adds a new hire, updated when someone transfers departments, and disabled the day someone leaves. Can you set up the Workday → Entra ID lifecycle flow?

**My job:** Walk through the full Joiner / Mover / Leaver flow in Entra ID, using HR data as the trigger.

## What I Did
- **Joiner:** Created a new hire account and assigned groups
- **Mover:** Updated department and group membership after a transfer
- **Leaver:** Blocked sign-in and removed access
- Validated each change with sign-in and audit logs

Full walkthrough with screenshots: [STEPS.md](STEPS.md)

## Lessons Learned
- HR should be the source of truth, so IAM changes follow HR events, not ad-hoc requests.
- Movers are the riskiest stage: remove old access, don't just add new access.
- Leavers must be disabled the same day to prevent orphaned accounts.
