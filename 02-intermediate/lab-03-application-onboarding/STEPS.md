# Lab 03: Application Onboarding - Steps

**App:** Zoom · **Platforms:** Okta + Microsoft Entra ID

- [Part 1: Okta](#part-1-okta)
- [Part 2: Microsoft Entra ID](#part-2-microsoft-entra-id)
- [Lab Limitation](#lab-limitation)

---

## Part 1: Okta

### 1. Add Zoom from the App Catalog
Applications → Applications → **Browse App Catalog** → search "Zoom" → **Add Integration**

<p align="center">
  <img width="600" alt="Zoom in Okta app catalog" src="https://github.com/user-attachments/assets/0ebb1088-05c2-47d1-8960-f68f8f19dd94" />
  <br><em>Zoom in the Okta Integration Network (supports SAML, OIDC, and SCIM)</em>
</p>

### 2. Configure General Settings
Set the application label. Subdomain, ACS URL, and Audience URI would come from the company's Zoom account in production.

<p align="center">
  <img width="600" alt="Okta general settings" src="https://github.com/user-attachments/assets/6fff45bf-62bc-4bee-8005-53bce587704c" />
  <br><em>General settings for the Zoom integration</em>
</p>

### 3. Configure Sign-On Options (SAML 2.0)
Selected **SAML 2.0** as the sign-on method. The **Metadata URL** is what gets shared with Zoom's admin to finish the SSO setup.

<p align="center">
  <img width="400" alt="Okta SAML sign-on options" src="https://github.com/user-attachments/assets/48f2ad8e-dedd-4dd2-b9ca-464ea534d14b" />
  <br><em>SAML 2.0 selected, metadata URL generated</em>
</p>

### 4. Assign Users and Groups
Zoom-Contreraslab → **Assignments** → **Assign** → Assign to People / Assign to Groups

<p align="center">
  <img width="500" alt="Zoom integration with no assignments" src="https://github.com/user-attachments/assets/a9b1a4db-229e-4fa3-a4b0-27df651ff10f" />
  <br><em>Integration added. No one has access yet.</em>
</p>

| Assign to People | Assign to Groups |
|:---:|:---:|
| <img width="400" alt="Assign to people" src="https://github.com/user-attachments/assets/30475aa4-258c-4cb4-9869-b3979473c656" /> | <img width="400" alt="Assign to groups" src="https://github.com/user-attachments/assets/aa0b158d-7fba-4217-ab2d-556fb6647873" /> |
| *Assigning an individual user* | *Assigning Engineering-Team (best practice)* |

<p align="center">
  <img width="500" alt="Assignment results" src="https://github.com/user-attachments/assets/e5804db0-0b0e-4e6e-8f3f-b6c287d8661f" />
  <br><em>Test User gets access through the Engineering-Team group</em>
</p>

---

## Part 2: Microsoft Entra ID

### 1. Add Zoom from the App Gallery
Enterprise applications → **New application** → search "Zoom" → **Create**

<p align="center">
  <img width="700" alt="Zoom in Entra app gallery" src="https://github.com/user-attachments/assets/e9de9446-9d0a-475e-bcb1-a7b4eefb68d7" />
  <br><em>Zoom in the Microsoft Entra App Gallery (supports SAML and automatic provisioning)</em>
</p>

### 2. Set Up SAML Single Sign-On
Zoom → **Single sign-on** → **SAML**

<p align="center">
  <img width="600" alt="SAML-based sign-on page" src="https://github.com/user-attachments/assets/6f177bbf-4e88-44af-bc2c-30f85bd818dc" />
  <br><em>SAML setup: Basic config, Attributes & Claims, and Certificates</em>
</p>

### 3. Configure Basic SAML Settings
Filled in the three required fields:
- **Identifier (Entity ID):** unique ID for the app
- **Reply URL (ACS URL):** where Entra sends the SAML response
- **Sign on URL:** where users start the login

| Required Fields | Configured |
|:---:|:---:|
| <img width="400" alt="Required SAML fields" src="https://github.com/user-attachments/assets/2c24c662-4e6e-4306-bfee-8f88e3814f74" /> | <img width="400" alt="SAML fields configured" src="https://github.com/user-attachments/assets/558e11f1-c60c-4c34-9561-34e51a9bb03a" /> |
| *Entra requires all three fields* | *Test values entered (see Lab Limitation)* |

### 4. Test as the User
Assigned Alex Thompson to the app, then signed in at **myapps.microsoft.com** in an Incognito window.

| My Apps Portal | Launching Zoom |
|:---:|:---:|
| <img width="400" alt="Zoom tile on Alex's My Apps" src="https://github.com/user-attachments/assets/d151b11f-d599-481b-bb6d-1d617228b869" /> | <img width="400" alt="Zoom sign-in page" src="https://github.com/user-attachments/assets/93b802dd-3437-4e99-9270-613e7c6108a6" /> |
| *Zoom tile shows up for Alex* | *Clicking the tile sends Alex to Zoom's sign-in* |

---

## Lab Limitation
Finishing SAML SSO for Zoom requires a **paid Zoom account** with admin access, so the Zoom side (uploading the IdP certificate and metadata) couldn't be completed. Test values were used for the Entity ID and ACS URL.

What this lab **does** prove:
- The app was added and configured in both Okta and Entra ID
- Users and groups were assigned correctly
- The app tile shows up for the assigned user and launches the Zoom sign-in

In production, the final step would be exchanging metadata with the Zoom admin. After that, clicking the tile would sign the user straight into Zoom with no password prompt.
