Export All Users with More Than 2 MFA Authentication Methods Script

Overview

This PowerShell script exports a list of all users in the Entra ID (formerly Azure AD) tenant with more than 2 registered MFA authentication methods. The script outputs a CSV file containing the users' UPNs, MFA method types, and method IDs.

Requirements
PowerShell 5.1 or later
Microsoft Graph PowerShell module (Microsoft.Graph.Users and Microsoft.Graph.Identity.SignIns)
Entra ID (formerly Azure AD) tenant with necessary permissions

Usage
Install the Microsoft Graph PowerShell module if you haven't already:
PowerShell
Install-Module Microsoft.Graph
Update the script with the path to the output CSV file.
Run the script in PowerShell.

Script Parameters
$outputCsvPath: Path to the output CSV file.

Output
The output CSV file will contain the following columns:
UserPrincipalName: The user's UPN.

MethodType: The type of MFA authentication method.

MethodId: The ID of the MFA authentication method.

Permissions
The script requires the following permissions in Entra ID:
User.Read.All
UserAuthenticationMethod.Read.All

Troubleshooting
Make sure you have the necessary permissions in Entra ID.
Check the output CSV file for errors.
Verify that the script has completed successfully.

Disclaimer
This script is provided as-is without warranty. Use at your own risk. Make sure to test the script in a development environment before running it in production.

Notes
The script may take some time to run depending on the number of users in your tenant.
Make sure to run the script with an account that has the necessary permissions to read user data and authentication methods.