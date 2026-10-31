# AWS S3 Static Website Hosting Practical

**Student:** Manaswi Harmalkar  
**Practical:** Host a static website using Amazon S3  
**AWS Region:** Asia Pacific (Mumbai) — `ap-south-1`  
**S3 Bucket:** `manaswi-static-website-2026`

## Aim
To create and host a simple static HTML website using Amazon S3 and verify that it is accessible through the S3 website endpoint.

## Services and Tools Used
- Amazon S3
- AWS Management Console
- HTML (`index.html`)
- Web browser

## Procedure

1. **Create an S3 bucket**
   - Created the bucket `manaswi-static-website-2026` in the Mumbai region (`ap-south-1`).
   - Kept Object Ownership as **Bucket owner enforced**.

2. **Create and upload the website file**
   - Prepared an `index.html` file containing a welcome message.
   - Uploaded `index.html` to the bucket root.
   - Confirmed that the upload succeeded.

3. **Configure public access for the demonstration**
   - Turned off **Block all public access** for this bucket.
   - This is required for this public S3 website demonstration. Do not store private or sensitive files in this bucket.

4. **Add a bucket policy**
   - Added a policy allowing public `s3:GetObject` access to objects in this bucket.

   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Sid": "PublicReadForStaticWebsite",
         "Effect": "Allow",
         "Principal": "*",
         "Action": "s3:GetObject",
         "Resource": "arn:aws:s3:::manaswi-static-website-2026/*"
       }
     ]
   }
   ```

5. **Enable static website hosting**
   - Opened **Properties → Static website hosting**.
   - Enabled **Host a static website**.
   - Set the index document to `index.html`.
   - Saved the changes.

6. **Test the website**
   - Opened the S3 website endpoint in a browser.
   - Verified that the welcome page loaded successfully.

## Website Endpoint

http://manaswi-static-website-2026.s3-website.ap-south-1.amazonaws.com

> S3 website endpoints use HTTP, so the browser may display “Not secure”. This is expected for the standard S3 static website endpoint. S3 static website hosting does not itself provide HTTPS. For HTTPS, a common architecture uses CloudFront with an appropriate certificate.

## Result
The static website was hosted successfully using Amazon S3. The final browser screenshot is included in the `screenshots/` folder.

## Screenshots

- `screenshots/06-website-live.png` — Final website opened successfully in the browser.

Earlier setup screenshots can be added to this folder if they are required for the submission.

## GitHub Upload Checklist

- [ ] Create a new GitHub repository, for example `aws-s3-static-website-hosting`.
- [ ] Extract this ZIP file.
- [ ] Upload `README.md` and the `screenshots/` folder.
- [ ] If permitted by the assignment, also upload the `index.html` file used in the practical.
- [ ] Check that the screenshot displays correctly in the repository.
- [ ] Copy the repository URL for submission.

## Cleanup and Security Notes

- This demonstration makes website objects publicly readable. Keep private data out of the bucket.
- AWS may charge for S3 storage and requests, depending on the account and usage.
- After the practical is graded, remove public access and delete the test resources if they are no longer needed and you are authorized to do so.
