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
  <img width="500" alt="Creating group in Okta" src="https://github.com/user-attachments/assets/6f29f6b5-e565-445f-9e9a-e0ef1f7a6e6b" />
  <br><em>Creating the Engineering-Team group</em>
</p>

<p align="center">
  <img width="500" alt="Group created in Okta" src="https://github.com/user-attachments/assets/1eb8413e-b05d-499f-b793-49224ee1f65a" />
  <br><em>Engineering-Team group created</em>
</p>

<p align="center">
  <img width="500" alt="Assigning user to group" src="https://github.com/user-attachments/assets/3c58bd26-9f28-42b0-aee6-6125c68a6dfc" />
  <br><em>Assigning Test User to the group</em>
</p>

<p align="center">
  <img width="500" alt="User assigned to group" src="https://github.com/user-attachments/assets/fd1d3aa7-11f7-4299-a272-02c985ebf48a" />
  <br><em>Test User is now a member of Engineering-Team</em>
</p>

---

### 3. Reset a Password
Directory → People → select user → **Reset or Remove password**

| Admin View | Test User View |
|:---:|:---:|
| <img width="400" alt="Admin reset password" src="https://github.com/user-attachments/assets/0b60bf87-7e7a-4f9a-8806-7b86fd418511" /> | <img width="400" alt="Test user signed in" src="https://github.com/user-attachments/assets/5a03a829-6dcb-4b40-8483-a19000c9c519" /> |
| *Admin resetting Test User's password* | *Test User signed in with the new password* |

---

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
