# AWS IAM User Security: Permissions & MFA

**Student:** Manaswi Harmalkar  
**Service:** AWS Identity and Access Management (IAM)  
**Practical topic:** Create an IAM user, review assigned permissions, and enable Multi-Factor Authentication (MFA).

## Aim
To understand basic AWS identity security by reviewing an IAM user's permissions and enabling MFA for console sign-in.

## Practical work documented
1. Opened the AWS IAM console and located the IAM user `manaswi-practical-user`.
2. Reviewed the user's attached permissions. The screenshot shows `AgentRegistryReadOnlyAccess` attached through a group and `IAMUserChangePassword` attached directly.
3. Assigned a virtual MFA device to the IAM user.
4. Verified that the user summary displayed **Console access: Enabled with MFA**.

## Screenshots
Screenshots are in the `screenshots/` folder:

- `01-IAM-User-Created.png` – IAM user listed in the IAM console.
- `02-IAM-Permissions.png` – User's assigned policies and group attachment.
- `03-IAM-MFA-Enabled.png` – MFA device assigned and console access enabled with MFA.

Some account-identifying details have been redacted in these copies for safer public GitHub sharing.

## Result
The screenshots document an IAM user, its current permission assignments, and successful MFA assignment. This demonstrates a basic identity-security configuration in AWS.

## Security notes
- MFA improves sign-in security by requiring a second authentication factor.
- Follow least privilege: grant only the permissions needed for the task.
- Do not upload passwords, access keys, secret keys, MFA QR codes, recovery codes, or unredacted account details to GitHub.
- This repository documents the configuration shown in the screenshots; it does not contain credentials or automate AWS resource creation.

## Repository structure
```text
Manaswi_AWS_IAM_MFA_Practical/
├── README.md
└── screenshots/
    ├── 01-IAM-User-Created.png
    ├── 02-IAM-Permissions.png
    └── 03-IAM-MFA-Enabled.png
```

## GitHub upload checklist
- [ ] Create a repository, for example `AWS-IAM-MFA-Security-Practical`.
- [ ] Upload `README.md` and the `screenshots/` folder.
- [ ] Check that all three images display correctly in GitHub.
- [ ] Confirm no passwords, secret keys, QR codes, or private credentials are included.
- [ ] Commit the files with a message such as `Add AWS IAM MFA practical screenshots and README`.
- [ ] Open the repository page and verify the README renders correctly.
