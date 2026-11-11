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

| Admin View | Test User View |
|:---:|:---:|
| <img width="400" alt="Admin suspended user" src="https://github.com/user-attachments/assets/f4453b33-abf7-41ab-bc5c-fafe455a1792" /> | <img width="400" alt="Test user unable to sign in" src="https://github.com/user-attachments/assets/7ce91e7b-df31-4648-9638-5764b9ef89e0" /> |
| *Admin suspends Test User* | *Test User can no longer sign in* |

<p align="center">
  <img width="500" alt="User suspended in People list" src="https://github.com/user-attachments/assets/ffb01cad-177a-4f8e-ac4c-317d0bf68885" />
  <br><em>Test User now shows as Suspended in the directory</em>
</p>

---

## Part 2: Microsoft Entra ID

### 1. Create a User
Entra ID → Users → **New user** → **Create new user** → fill in Basics and Properties → **Review + create**

| Basics | Properties |
|:---:|:---:|
| <img width="400" alt="Creating user in Entra - basics" src="https://github.com/user-attachments/assets/f6525b06-2c5d-4741-af52-a3ad825ff780" /> | <img width="400" alt="Creating user in Entra - properties" src="https://github.com/user-attachments/assets/51775be0-0c78-46cc-948f-816cdeb070ca" /> |
| *Filling in the user's basic info* | *Adding job title and department* |

<p align="center">
  <img width="400" alt="Review and create user" src="https://github.com/user-attachments/assets/e59bd46f-119f-49aa-9984-47019b50cfd2" />
  <br><em>Reviewing the user before creating</em>
</p>

<p align="center">
  <img width="600" alt="User created in Entra ID" src="https://github.com/user-attachments/assets/107d788e-9b2e-4dce-9986-ef2bb1a6538a" />
  <br><em>Test User created in Entra ID</em>
</p>

---

### 2. Create a Group and Assign the User
Entra ID → Groups → **New group** → Security, `Engineering-Team`, Assigned → add member → **Create**

<p align="center">
  <img width="400" alt="Creating group in Entra ID" src="https://github.com/user-attachments/assets/fabc5c35-5e8b-48a5-9b09-a2bf98358c8e" />
  <br><em>Creating the Engineering-Team security group</em>
</p>

<p align="center">
  <img width="600" alt="Group created in Entra ID" src="https://github.com/user-attachments/assets/876dada2-c75b-44d3-aa41-5a3e53a37a36" />
  <br><em>Engineering-Team group created</em>
</p>

<p align="center">
  <img width="600" alt="Adding user to group" src="https://github.com/user-attachments/assets/0c83a234-a04b-422c-9874-d30cfe12c1aa" />
  <br><em>Adding Test User to the group</em>
</p>

<p align="center">
  <img width="500" alt="User assigned to group" src="https://github.com/user-attachments/assets/cc60a9a4-0519-4e26-bbe5-d79556d72b62" />
  <br><em>Test User is now a member of Engineering-Team</em>
</p>

---

### 3. Reset a Password
Users → select user → **Reset password** → **Reset**

<p align="center">
  <img width="600" alt="Admin resetting password" src="https://github.com/user-attachments/assets/162d3e4f-5430-41dc-957d-9cbe7cb4a843" />
  <br><em>Admin resetting Test User's password</em>
</p>

<p align="center">
  <img width="600" alt="Temporary password generated" src="https://github.com/user-attachments/assets/34a05c81-4fdb-4e74-aa10-f574f39b49d6" />
  <br><em>Temporary password generated</em>
</p>

<p align="center">
  <img width="400" alt="Test user signed in" src="https://github.com/user-attachments/assets/44fc9531-cd7c-44b5-8cae-1a4d3365e201" />
  <br><em>Test User signed in with the new password</em>
</p>

---

### 4. Disable the Account
Users → select user → **Edit properties** → Block sign in: **Yes** → **Save**

| Admin View | Test User View |
|:---:|:---:|
| <img width="400" alt="Admin blocks sign-in" src="https://github.com/user-attachments/assets/0079a592-dc17-4cdd-8427-340b58e08950" /> | <img width="400" alt="Test user unable to sign in" src="https://github.com/user-attachments/assets/062b014b-1e08-40ba-ba03-dc60100876f1" /> |
| *Admin blocks sign-in for Test User* | *Test User can no longer sign in* |

---

### 5. Validate with Sign-in Logs
Monitoring → **Sign-in logs** → Add filter → User → Test User

<p align="center">
  <img width="700" alt="Entra ID sign-in logs" src="https://github.com/user-attachments/assets/05220b9f-a3ee-475b-a5ad-a67b63e4d698" />
  <br><em>Sign-in logs confirming the blocked sign-in attempt</em>
</p>
