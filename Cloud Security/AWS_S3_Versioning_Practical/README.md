# AWS S3 Bucket Versioning Practical

## Aim
To create an Amazon S3 bucket, enable bucket versioning, upload a text file, update the same file, and verify that S3 keeps multiple object versions.

## AWS Services Used
- Amazon S3
- AWS Management Console

## Configuration
- **Bucket name:** `manaswi-s3practical-2026`
- **AWS Region:** Asia Pacific (Mumbai) `ap-south-1`
- **Test object:** `version-test.txt`
- **Versioning:** Enabled

## Procedure
1. Open the Amazon S3 console.
2. Create or open the bucket `manaswi-s3practical-2026`.
3. Open **Properties** and enable **Bucket Versioning**.
4. Upload `version-test.txt`.
5. Change the file contents and upload the same filename again.
6. Open the object and select the **Versions** tab.
7. Confirm that both the current version and the previous version are listed.

## Result
**Practical completed successfully.** Bucket versioning is enabled, and the Versions tab shows two versions of `version-test.txt`. This demonstrates that S3 can preserve earlier object versions when a file with the same key is uploaded again.

## Screenshots
Evidence screenshots are available in the `screenshots/` folder:

1. `01-S3-Bucket-Created.png` - S3 bucket list.
2. `02-Versioning-Enabled.png` - Bucket Versioning shows **Enabled**.
3. `03-File-Upload-Success.png` - Successful upload confirmation.
4. `04-S3-Object-Versions.png` - Two object versions visible in the Versions tab.

## Important Notes
- Keep S3 Block Public Access enabled unless public access is explicitly required for a controlled exercise.
- Do not upload passwords, access keys, personal information, or other sensitive data.
- S3 versioning helps recover previous object versions, but it does not replace backups or access controls.
- AWS charges may apply depending on usage and storage. Delete practice resources when no longer needed, after confirming that your instructor does not need them.

## GitHub Upload Checklist
- [ ] Upload this `README.md`.
- [ ] Upload the complete `screenshots/` folder.
- [ ] Confirm all four screenshots are visible in the repository.
- [ ] Open the README on GitHub and verify its formatting.
- [ ] Copy the repository link for submission.
