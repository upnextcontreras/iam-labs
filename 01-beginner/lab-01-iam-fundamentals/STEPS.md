# Lab 01: IAM Fundamentals - Steps

- [Part 1: Okta](#part-1-okta)
- [Part 2: Microsoft Entra ID](#part-2-microsoft-entra-id)

---

## Part 1: Okta

### 1. Create a User
Directory → People → **Add Person** → enter user details → **Activate now** → **Save**

<p align="center">
  <img width="500" alt="Creating user in Okta" src="https://github.com/user-attachments/assets/a55cd07b-fa31-4039-9a7c-364dec21148b" />
  <br><em>Filling in the new user's details</em>
</p>

<p align="center">
  <img width="500" alt="Test user created in Okta" src="https://github.com/user-attachments/assets/75c3168a-23c1-4f79-bc1c-bc7746dac085" />
  <br><em>Test user created and active</em>
</p>

---

### 2. Create a Group and Assign the User
Directory → Groups → **Add Group** → name it `Engineering-Team` → **Save** → **Assign People**

<p align="center">
  <img width="500" alt="Creating group in Okta" src="LINK-creatingroupsokta" />
  <br><em>Creating the Engineering-Team group</em>
</p>

<p align="center">
  <img width="500" alt="Group created in Okta" src="LINK-groupcreatedokta" />
  <br><em>Engineering-Team group created</em>
</p>

<p align="center">
  <img width="500" alt="Assigning user to group" src="LINK-assigning_to_group" />
  <br><em>Assigning Test User to the group</em>
</p>

<p align="center">
  <img width="500" alt="User assigned to group" src="LINK-assignedtogroup2" />
  <br><em>Test User is now a member of Engineering-Team</em>
</p>

---
### 3. Reset a Password
Directory → People → select user → More Actions → **Reset Password**

![Okta - password reset](screenshots/05-okta-password-reset.png)

### 4. Disable the Account
Directory → People → select user → More Actions → **Suspend**

![Okta - suspend user](screenshots/07-okta-suspend-user.png)

---

## Part 2: Microsoft Entra ID

### 1. Create a User
Entra ID → Users → **New user** → **Create new user** → fill in Basics and Properties → **Review + create**

![Entra ID - create user](screenshots/02-entra-create-user.png)

### 2. Create a Group and Assign the User
Entra ID → Groups → **New group** → Security, `Engineering-Team`, Assigned → add member → **Create**

![Entra ID - group](screenshots/04-entra-group.png)

### 3. Reset a Password
Users → select user → **Reset password** → **Reset**

![Entra ID - password reset](screenshots/06-entra-password-reset.png)

### 4. Disable the Account
Users → select user → **Edit properties** → Block sign in: **Yes** → **Save**

![Entra ID - block sign-in](screenshots/08-entra-block-sign-in.png)

### 5. Validate with Sign-in Logs
Monitoring → **Sign-in logs** → Add filter → User → confirm the blocked sign-in

![Entra ID - sign-in logs](screenshots/09-entra-sign-in-logs.png)
