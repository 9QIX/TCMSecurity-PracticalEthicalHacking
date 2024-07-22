# Using Breach Pass for Credential Gathering

## Introduction to Breach Pass

- A tool created by the instructor (H Maverick Adams)
- Available on GitHub: github.com/HMaverickAdams/breach-pass
- Uses a large database of breached credentials (44GB extracted)

## How Breach Pass Works

1. Searches through compiled breach data
2. Finds email addresses and passwords for a specified domain
3. Outputs results in three files: master, users, and passwords

## Using Breach Pass (Example with Tesla)

1. Run the tool: `./breach-pass @tesla.com tesla.txt`
2. Tool searches for @tesla.com email addresses in the breach data
3. Results are saved in tesla_master.txt, tesla_users.txt, and tesla_passwords.txt

## Analyzing the Results

- Look for patterns in email formats (e.g., first.last@tesla.com, first_initial.last@tesla.com)
- Identify repeat offenders (users with multiple breached passwords)
- Analyze password patterns and complexities

## Utilizing the Information

1. Credential Stuffing: Use found email/password combinations on target systems
2. Password Spraying: Use common passwords (e.g., fall2019) with known email addresses
3. Create variations of found passwords for additional attempts

## Importance in Penetration Testing

- Critical part of information gathering phase
- Helps identify potential vulnerabilities in user credentials
- Can lead to successful system access during later stages of testing

## Ethical Considerations

- This information should only be used for authorized penetration testing
- Always follow legal and ethical guidelines when performing security assessments

Remember: The instructor emphasizes that you don't need to download or run this tool yourself, as the video is for demonstration purposes only.
