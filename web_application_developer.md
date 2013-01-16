# HIPAA For Web Application Developers
***
## Administrative Safeguards

### Security Management Process

#### Information System Activity Review (R)
_Implement procedures to regularly review records of information system activity, such as audit logs, access reports, and security incident tracking reports._

The covered entity (CE) should have its own method for tracking security incidents. The web application (WA) should provide methods for generating and reviewing audit logs and access reports. At a minimum the WA should generate logs for logins, logouts, and record access, modification, or deletion.

### Workforce Security
_Implement policies and procedures to ensure that all members of its workforce have appropriate access to electronic protected health information, as provided under [the Information Access Management standard], and to prevent those workforce members who do not have access under [the Information Access Management standard] from obtaining access to electronic protected health information._

The WA should be designed so that access to all electronic protected health information (EPHI) requires authentication. The WA should also allow unique user accounts to be created, modified, and deleted as needed.

#### Authorization and/or Supervision (A)
_Implement procedures for the authorization and/or supervision of workforce members who work with electronic protected health information or in locations where it might be accessed._

The WA should log the access, modification, and removal of all EPHI data.

#### Workforce Clearance Procedure (A)
_Implement procedures to determine that the access of a workforce member to electronic protected health information is appropriate._

The WA should implement user roles with clearly defined access limits, e.g., administrator, backup user, and standard user. 

#### Termination Procedures (A)
_Implement procedures for terminating access to electronic protected health information when the employment of a workforce member ends or as required by determinations made as specified in paragraph (a)(3)(ii)(B) [the Workforce Clearance Procedure] of this section._

The WA should allow unique user accounts to be created, modified, and deleted as needed.

### Information Access Management
_Implement policies and procedures for authorizing access to electronic protected health information that are consistent with the applicable requirements of subpart E of this part [the Privacy Rule]._

#### Access Authorization (A)
_Implement policies and procedures for granting access to a workstation, transaction, program, process, or other mechanism_

The WA should allow unique user accounts to be created, modified, and deleted as needed. Administrators should also have the ability to assign users to specific roles and to modify role assignments.

### Security Awareness and Training
_Implement a security awareness and training program for all members of its workforce (including management)._

#### Log-in Monitoring (A)
_Procedures for monitoring log-in attempts and reporting discrepancies._

The WA should log successful and failed login attempts and provide means for reviewing login attempts.

#### Password Management (A)
_Procedures for creating, changing, and safeguarding passwords._

The WA should provide a secure method for creating and changing passwords. Passwords should be hashed using a strong algorithm designed for password storage.

### Contingency Plan
_Establish (and implement as needed) policies and procedures for responding to an emergency or other occurence (for example, fire, vandalism, system failure, and natural disaster) that damages systems that contain electronic protected health information._

#### Data Backup Plan (R)
_Establish and implement procedures to create and maintain retrievable exact copies of electronic protected health information._

The WA should provide a mechanism to creating backups of all EPHI records and audit logs.

#### Disaster Recovery Plan (R)
_Establish (and implement as needed) procedures to restore any loss of data._

The WA should be designed to easily restore data from backup and to verify the integrity of data restored from backup.

#### Emergency Mode Operation Plan (R)
_Establish (and implement as needed) procedures to enable continuation of critical business processes for protection of the security of electronic protected health information while operating in emergency mode._

All security mechanisms in the WA should continue to function in the event of a fail over.

### Business Associate Contracts and Other Arrangements
_A covered entity, in accordance with [the Security Standards: General Rules], may permit a business associate to create, receive, maintain, or transmit electronic protected health information on the covered entity's behalf only if the covered entity obtains satisfactory assurances, in accordance with [the Organizational Requirements] that the business associate will appropriately safeguard the information._

The WA should only use 'dummy' data during development and testing. If live data is used, the developer is obligated to secure the data in accordance with the HIPAA standards and must agree to this obligation contractually.

## Technical Safeguards

### Access Control
_Implement technical policies and procedures for electronic information systems that maintain electronic protected health information to allow access to only those persons or software programs that have been granted access rights as specified in 164.308(a)(4)[Information Access Management]._

#### Unique User Identification (R)
_Assign a unique name and/or number for identifying and tracking user identity._

The WA should assign each user a unique identifier that can be used to track login attempts and data access, modification, and deletion.

#### Emergency Access Procedure (R)
_Establish (and implement as needed) procedures for obtaining necessary electronic protected health information during an emergency._

The WA should be designed to failover gracefully and to be brought back online quickly after a disaster.

#### Automatic Logoff (A)
_Implement electronic procedures that terminate an electronic session after a predetermined time of inactivity._

The WA should terminate sessions after a period of inactivity.

#### Encryption and Decryption (A)
_Implement a mechanism to encrypt and decrypt electronic protected health information._

The WA should encrypt EPHI to ensure only the receiving party is able to access the data.

### Audit Controls
_Implement hardware, software, and/or procedural mechanisms that record and examine activity in information systems that contain or use electronic protected health information._

### Integrity
_Implement policies and procedures to protect electronic protected health information from improper alteration or destruction._

The WA should provide a mechanism to verify the integrity of records and to prevent them from being modified or destroyed improperly. Particularly, only certain roles should have the ability to destroy records.

#### Mechanism to Authenticate Electronic Protected Health Information (A)
_Implement electronic mechanisms to corroborate that electronic protected health information has not been altered or destroyed in an unauthorized manner._

The WA should routinely check data to ensure it has not been improperly modified.

### Person or Entity Authentication
_Implement procedures to verify that a person or entity seeking access to electronic protected health information is the one claimed._

The WA should authenticate any user attempting to access EPHI records. 

### Transmission Security
_Implement technical security measures to guard against unauthorized access to electronic protected health information that is being transmitted over an electronic communications network._

#### Integrity Controls (A)
_Implement security measures to ensure that electronically transmitted electronic protected health information is not improperly modified without detection until disposed of._

The WA should provide a mechanism to routinely check the integrity of EPHI that is transmitted electronically.

#### Encryption (A)
_Implement a mechanism to encrypt electronic protected health information whenever deemed appropriate._

The WA should encrypt all EPHI data in transit. Particularly, the WA should use SSL3/TLS encryption and should use valid security certificates.

## Physical Safeguards

The physical safeguards should not apply to a WA developer unless the developer is using live data instead of dummy data. If live data is used the developer is obligated to protect the data according to the full HIPAA standard.