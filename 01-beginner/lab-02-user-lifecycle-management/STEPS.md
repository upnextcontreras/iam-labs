# Lab 02: User Lifecycle Management - Steps

**Employee:** Alex Thompson · **Platform:** Microsoft Entra ID

- [Joiner: New Hire](#joiner-new-hire)
- [Mover: Department Transfer](#mover-department-transfer)
- [Leaver: Employee Departure](#leaver-employee-departure)
- [Validate with Sign-in Logs](#validate-with-sign-in-logs)

---

## Joiner: New Hire
HR adds Alex Thompson as a new Software Developer in Engineering.

### 1. Create the User
Users → **New user** → **Create new user** → added HR attributes (Job title, Department) → **Review + create**

<p align="center">
  <img width="500" alt="Alex Thompson created with HR attributes" src="LINK-joiner-user-created" />
  <br><em>Alex created with Job title: Software Developer, Department: Engineering</em>
</p>

### 2. Assign to a Group
Same process as [Lab 01](../lab-01-iam-fundamentals/STEPS.md). Added Alex to `Engineering-Team`.

<p align="center">
  <img width="500" alt="Alex in Engineering-Team" src="LINK-joiner-group" />
  <br><em>Alex is a member of Engineering-Team</em>
</p>

### 3. Set a Temporary Password
Users → Alex Thompson → **Reset password** → auto-generate → **Reset**

<p align="center">
  <img width="500" alt="Temporary password generated" src="LINK-joiner-password" />
  <br><em>Temporary password generated. Alex must change it at first sign-in.</em>
</p>

---

## Mover: Department Transfer
Alex transfers from Engineering to Sales.

### 4. Update HR Attributes
Users → Alex Thompson → **Edit properties** → Department: `Sales`, Job title: `Sales Engineer` → **Save**

<p align="center">
  <img width="500" alt="Department updated to Sales" src="LINK-mover-attributes" />
  <br><em>Department and job title updated after the transfer</em>
</p>

### 5. Swap Group Access
Removed Alex from `Engineering-Team` and added him to `Sales-Team`.

| Removed Old Access | Added New Access |
|:---:|:---:|
| <img width="400" alt="Removed from Engineering-Team" src="LINK-mover-removed" /> | <img width="400" alt="Added to Sales-Team" src="LINK-mover-added" /> |
| *Removed from Engineering-Team* | *Added to Sales-Team* |

---

## Leaver: Employee Departure
Alex leaves the company. Access is cut off the same day.

### 6. Block Sign-in
Users → Alex Thompson → **Edit properties** → Block sign in: **Yes** → **Save**

| Admin View | User View |
|:---:|:---:|
| <img width="400" alt="Block sign-in set to Yes" src="LINK-leaver-blocked" /> | <img width="400" alt="Alex unable to sign in" src="LINK-leaver-cant-sign-in" /> |
| *Admin blocks sign-in* | *Alex can no longer sign in* |

### 7. Re-enable the Account (Rehire / Mistake)
Users → Alex Thompson → **Edit properties** → Block sign in: **No** → **Save**

<p align="center">
  <img width="500" alt="Account re-enabled" src="LINK-reenabled" />
  <br><em>Account restored. Disabling instead of deleting makes this possible.</em>
</p>

---

## Validate with Sign-in Logs
Monitoring → **Sign-in logs** → Add filter → User → Alex Thompson → click an entry

<p align="center">
  <img width="600" alt="Sign-in log list" src="LINK-logs-list" />
  <br><em>Successful and blocked sign-in attempts for Alex</em>
</p>

<p align="center">
  <img width="600" alt="Sign-in log details" src="LINK-logs-details" />
  <br><em>Sign-in details: status, IP address, location, device, and Conditional Access result</em>
</p>
