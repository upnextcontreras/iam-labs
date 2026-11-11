# Lab 02: User Lifecycle Management - Steps

**Employee:** Alex Thompson · **Platform:** Microsoft Entra ID

- [Joiner: New Hire](#joiner-new-hire)
- [Mover: Department Transfer](#mover-department-transfer)
- [Leaver: Employee Departure](#leaver-employee-departure)
- [Rehire: Restoring Access](#rehire-restoring-access)

---

## Joiner: New Hire
HR adds Alex Thompson as a new Software Developer in Engineering.

### 1. Create the User
Users → **New user** → **Create new user** → added HR attributes (Job title, Department) → **Review + create**

<p align="center">
  <img width="400" alt="Alex Thompson created with HR attributes" src="https://github.com/user-attachments/assets/d5bc90f1-07a8-48f9-971e-4454cc8ce8fe" />
  <br><em>Alex created with Job title: Software Developer, Department: Engineering</em>
</p>

### 2. Assign to a Group
Same process as [Lab 01](../lab-01-iam-fundamentals/STEPS.md). Added Alex to `Engineering-Team`.

<p align="center">
  <img width="600" alt="Alex in Engineering-Team" src="https://github.com/user-attachments/assets/b7358232-3f21-44b6-ad5f-c9b936078ad0" />
  <br><em>Alex is a member of Engineering-Team</em>
</p>

### 3. Set a Temporary Password
Users → Alex Thompson → **Reset password** → auto-generate → **Reset**

<p align="center">
  <img width="600" alt="Temporary password generated" src="https://github.com/user-attachments/assets/2f7f712c-96c5-49cc-a356-f6ea75f74b8a" />
  <br><em>Temporary password generated. Alex must change it at first sign-in.</em>
</p>

---

## Mover: Department Transfer
Alex transfers from Engineering to Sales. Old access is removed and new access is granted.

### 4. Swap Group Access
Removed Alex from `Engineering-Team` and added him to `Sales-Team`.

<p align="center">
  <img width="600" alt="Removed from Engineering-Team" src="https://github.com/user-attachments/assets/c62415dd-a74d-4907-8800-4560abd0a043" />
  <br><em>Alex removed from Engineering-Team</em>
</p>

<p align="center">
  <img width="400" alt="Sales-Team" src="https://github.com/user-attachments/assets/94e5f3b8-0a6d-4fa2-a83c-ba362279252c" />
  <br><em>Adding Alex to Sales-Team</em>
</p>

<p align="center">
  <img width="600" alt="Added to Sales-Team" src="https://github.com/user-attachments/assets/d64fbe93-b896-40ad-8740-edbeaf5c8d6d" />
  <br><em>Alex is now a member of Sales-Team</em>
</p>

---

## Leaver: Employee Departure
Alex leaves the company. Access is cut off the same day.

### 5. Block Sign-in
Users → Alex Thompson → **Edit properties** → Block sign in: **Yes** → **Save**

| Admin View | User View |
|:---:|:---:|
| <img width="400" alt="Block sign-in set to Yes" src="https://github.com/user-attachments/assets/a275be8e-3252-4b09-8b2c-9c6c5257f4ec" /> | <img width="350" alt="Alex unable to sign in" src="https://github.com/user-attachments/assets/fae5bae2-598e-4902-a6b9-0e2364f9a77c" /> |
| *Admin blocks sign-in* | *Alex can no longer sign in* |

---

## Rehire: Restoring Access
Alex is rehired (or the account was disabled by mistake). Because the account was **disabled, not deleted**, access can be restored in seconds, with the same identity, groups, and history.

### 6. Unblock Sign-in
Users → Alex Thompson → **Edit properties** → Block sign in: **No** → **Save**

<p align="center">
  <img width="400" alt="Alex signed in after access restored" src="https://github.com/user-attachments/assets/a93a1a70-c2e9-46d7-bf31-1dc476d17a09" />
  <br><em>Alex signs in successfully after the account is unblocked</em>
</p>

### 7. Confirm in Sign-in Logs
Monitoring → **Sign-in logs** → Add filter → User → Alex Thompson

<p align="center">
  <img width="700" alt="Sign-in logs for Alex Thompson" src="https://github.com/user-attachments/assets/f0955153-566e-4d01-b3bd-60fc290fab76" />
  <br><em>Logs show the full story: blocked sign-in while disabled, then successful sign-in after access was restored</em>
</p>
