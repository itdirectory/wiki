# Privacy Policy

Effective Date: June 20th 2026
Last Updated: November 2nd 2026

Ido Homri Software ("we," "us," or "our") operates IT Directory, a SaaS platform for IT inventory, asset management, employee directory management, software asset and license tracking, network inventory, domain monitoring, connector integrations, an employee self-service portal, electronic equipment handover forms, reporting, reminders, and related organizational administration (the "Services").

This Privacy Policy explains how we collect, use, disclose, retain, and protect personal information and organizational information when the Services are used. IT Directory is a business-to-business service. Much of the data in the Services is processed on behalf of a customer organization, such as an employer, managed service provider, or IT service provider.

IT Directory is not intended for highly sensitive data. Inventory, employee directory, device, network, domain, software, license, cost, signature, and operational metadata may still be personal data, confidential business information, or security-sensitive operational data.

***

### 1. Scope and Key Terms

This Privacy Policy applies to:

* The IT Directory web application, employee portal, APIs, documentation, transactional emails, reminders, reports, generated PDFs, and related service components.
* Account holders, administrators, technicians, and other users with administrative login accounts ("Authorized Users").
* Employees and other people whom a Customer enables to sign in to the employee portal ("Portal Users").
* Employees, contractors, clients, and other people whose information is entered into or imported into the Services by a customer organization ("Managed Persons"). Portal Users are also Managed Persons.
* Customer organizations and managed service providers that use the Services ("Customers").

"Customer Data" means information uploaded to, generated in, or imported into the Services by or on behalf of a Customer, including employee records, device records, software asset and license records, network records, domain records, connector data, handover and return records, uploaded branding, notes, reports, reminder settings, and organizational metadata.

"Handover Records" means records created when a Customer issues equipment to, or records the return of equipment from, a Managed Person through the Services, including signature requests, signed handover forms, return receipts, and the related PDFs.

"Account Data" means information we process for our own account administration, security, billing, service operation, communications, and legal compliance.

#### 1.1 The Employee Portal

A Customer may enable an employee portal. When it is enabled, Portal Users can sign in to view the items assigned to them, the domains for which they are recorded as responsible, and forms the Customer has issued to them, and can sign handover forms and access their Handover Records.

The Customer controls the portal: whether it is enabled, which people can sign in, what records exist about them, the declaration wording on handover forms, and when access is disabled. Portal Users do not create a commercial relationship with us by using the portal, and do not accept our Terms of Use on behalf of the Customer. Questions about why information is held, or requests to correct or delete it, should be directed to the Customer (see Section 11).

***

### 2. Controller and Processor Roles

Our privacy role depends on the data and the context.

We are generally the **controller** for Account Data, including information used to create and manage user accounts, authenticate users, operate the website, communicate with users, administer trials or paid accounts, protect the Services, maintain service logs, and comply with legal obligations.

We are generally a **processor** acting on behalf of the Customer for Customer Data, including employee records, device and inventory data, software asset and license data, network data, domain data, asset assignments, Portal User access, Handover Records, uploaded branding, customer notes, report content, reminder configuration, and information imported through Customer-authorized integrations. For that data, the Customer is generally the controller and is responsible for determining the lawful basis, notices, permissions, and internal approvals required for the processing.

Where required, Customer Data processing may also be governed by a Data Processing Addendum, order form, or other written agreement. If there is a conflict between this Privacy Policy and a signed written agreement, the signed agreement controls for that Customer.

***

### 3. Information We Collect

#### 3.1 Account, Portal, and Authentication Information

We collect information used to create, secure, and administer user accounts and portal access, including:

* Name, email address, role, organization, company access scope, account status, email verification status, and account creation date.
* For Portal Users, the employee record the Customer has linked to portal access and the Customer's portal settings.
* Passwords for credentials-based accounts. Passwords are stored as hashes, not in plaintext.
* Password reset and email verification token metadata.
* One-time sign-in codes sent by email, used to sign in to the employee portal and, where applicable, as an additional verification step for other sign-ins. Codes are stored as hashes, not in plaintext, together with the related email address, expiry time, and a counter of failed attempts used to limit guessing.
* Trusted-browser records, which allow a browser that has completed verification to skip the emailed code for a limited period (see Section 13).
* Single sign-on account information, such as email address, name, and identity claims received from the Customer's identity provider.
* Security settings, SSO invitations, and user administration actions performed by Customer administrators.

#### 3.2 Organization, Branding, Billing, and Administration Information

We collect and process organization-level information, including:

* Organization name, slug, parent/sub-organization relationships, user roles, and company access settings.
* Company logos and other branding uploaded by the Customer. Logos are stored by the Services and displayed in the employee portal, on generated PDFs such as Handover Records, and in branded emails. See Section 8.1 regarding the public availability of portal logos.
* Trial status, paid/suspended status, asset and sub-organization limits, entitlement records, and related account administration details.
* System notification acknowledgments, report recipient allowlists, reminder recipients, portal settings, and configuration settings.

#### 3.3 Customer-Provided Employee and Inventory Data

Customers may enter, upload, import, or generate information including:

* Employee records: name, business email, phone number, job title, department, start date, notes, external IDs, asset assignments, and software license assignments.
* Hardware records: device name, hardware type, brand, model, serial number, asset tag, status, assigned employee, purchase date, warranty expiry, purchase price, vendor, notes, external IDs, and related lifecycle information.
* Software asset records: name, vendor, license or service type, encrypted license key where applicable, version, plan, website URL, billing cycle, cost, seat counts, assigned seats, owner, purchase date, expiry date, and notes.
* Network inventory records: VLAN IDs, subnets, gateways, DHCP configuration, locations, public IP address allocations, network and internet service providers, descriptions, and status.
* Domain records: domain names, registrable domains, registrar, registration and expiry dates, registrant organization where available, DNS records, TLS/SSL certificate information, discovered subdomains, hostnames, associated IP addresses, and the employees recorded as responsible for each domain.
* Reports and exports: report rows, CSV/PDF-style output, emailed report content, recipient email addresses, and report send audit metadata. Depending on the report, this may include cost and financial figures linked to departments or individual employees, such as department costs, costs allocated to individual employees, software spending, renewal forecasts, and license utilization.
* Free-text notes. Notes fields may contain personal or confidential information entered by Customer users, even though the Services are not intended for highly sensitive content.

#### 3.4 Electronic Handover Forms and Return Receipts

When a Customer uses handover forms, the Services create and store Handover Records. When a Portal User signs a handover form, we store:

* The signature the signer draws on screen, stored as an image, and the name the signer types.
* The signer's email address and the date and time of signing.
* The IP address and browser information (user-agent) of the device used to sign.
* The authentication method used to access the form.
* A snapshot of the assigned items at the time of signing (for example, device names, models, serial numbers, and asset tags).
* The declaration text the signer was shown and agreed to, as configured by the Customer.
* A cryptographic hash of the signed document, used to help detect later changes to the record.

The drawn signature is stored only as an image of the mark made on screen. The Services do not analyze signatures, compare them with other signatures, or use them to identify or verify the signer, and do not perform biometric identity verification.

Return receipts are recorded by the Customer's Authorized Users when equipment is returned. They record which items were returned and when. Employees do not sign return receipts.

Handover Records and their PDFs are available to the Portal User they concern and to the Customer's Authorized Users according to their roles and company access scopes.

#### 3.5 Information from Third-Party Connectors

When a Customer enables an integration, we access and import information from third-party systems as configured and authorized by the Customer.

Microsoft Entra ID employee sync may import directory user fields such as ID, display name, email, user principal name, job title, department, mobile phone, business phone, and user type.

Microsoft Intune device sync may import managed device fields such as device ID, device name, manufacturer, model, serial number, operating system, operating system version, Azure AD device ID, enrollment date, last sync date, assigned user ID, assigned user display name, assigned user principal name, and device ownership type. Personally owned devices may be skipped depending on connector logic.

Microsoft 365 license sync may import the Customer's subscribed products and SKUs, license quantities (purchased, assigned, and available), subscription and license status, and the license assignments of individual Microsoft 365 users, which the Services match to employee records.

Microsoft Entra ID SSO may use OAuth/OpenID Connect to authenticate users and provision invited users based on identity claims received from the Customer's tenant.

Cloudflare sync may import zones, domain names, DNS records, discovered subdomains, and related metadata from the Customer's Cloudflare account.

Domain monitoring may involve WHOIS/RDAP, DNS, TLS/SSL, certificate transparency, passive DNS, or similar lookups against public or third-party infrastructure sources. Subdomain discovery queries certificate-transparency and passive-DNS services, currently crt.sh and Cert Spotter (SSLMate), and, where configured, AlienVault OTX. These lookups send the domain name being checked to those services and return publicly observed hostnames, certificates, and related records. WHOIS/RDAP data can sometimes include personal registrant information, although it is often redacted.

Warranty lookup components may use device brand, model, and serial number to retrieve warranty status from vendor sources.

The exact data imported depends on the connector, the Customer's configuration, the permissions granted by the Customer, and third-party API responses.

#### 3.6 Credentials and Supported Secrets

The Services are designed to store a limited set of operational secrets needed for supported features, such as:

* Customer-provided Microsoft Entra ID client secrets.
* Customer-provided Cloudflare API tokens.
* Software license keys entered by Customers.

These values are encrypted at rest where supported by the application. Customers should not use the Services to store unrelated passwords, production credentials, private keys, source code, recovery codes, personal secrets, or other unsupported sensitive secrets.

#### 3.7 Automatically Collected Information

We may collect technical and usage information, including:

* Cookies and browser storage used for sign-in, security, and preferences, as described in Section 13.
* IP address or proxy-provided client IP, request metadata, browser type, device information, operating system, referrer, pages visited, feature usage, and performance data.
* Rate-limit records, sign-in attempt records, security logs, connector activity logs, report send audit logs, email send records, administrative action logs, system event logs, and error logs.

If Google Analytics is enabled by the deployment operator, Google Analytics may collect page view, session, browser, device, approximate location, and client identifier data through Google scripts and cookies. If Google Analytics is disabled, the Google Analytics script is not loaded by the application.

#### 3.8 Communications and Support

We collect information contained in messages sent to us, including support requests, security reports, sales inquiries, legal requests, and related communications.

***

### 4. How We Use Information

We use information to:

* Provide, operate, maintain, and secure the Services.
* Authenticate users and Portal Users, send and verify sign-in codes, manage sessions and trusted browsers, enforce roles and company access scopes, and support SSO.
* Maintain employee directories, hardware inventory, software assets and licenses, network inventory, domain records and responsible employees, assignments, reports, reminders, and organizational metadata.
* Operate the employee portal, show Portal Users the items, domains, and forms that relate to them, and display Customer branding.
* Create, present, sign, store, and generate PDFs of Handover Records, and record return receipts.
* Run Customer-authorized connector syncs and domain, warranty, and reminder service components.
* Generate, preview, export, and email reports at the direction of Customer users.
* Send transactional emails, including verification emails, password reset emails, sign-in code emails, portal sign-in emails, handover signature requests (including requests sent automatically when the Customer assigns items, where the Customer has enabled this), recurring reminders about unsigned handover forms, report emails, and reminder emails.
* Manage trials, billing status, capacity limits, entitlements, support, and customer administration.
* Detect, prevent, investigate, and respond to security, abuse, availability, integration, and support issues.
* Maintain audit trails and operational logs.
* Analyze Account Data, usage data, and aggregated or de-identified information to improve the Services.
* Respond to user, Customer, regulator, law enforcement, and legal requests.
* Comply with applicable law and enforce our agreements.

We do not use Customer Data to serve advertising. We do not sell personal information. We do not use Customer Data to train machine learning models.

***

### 5. Customer Responsibilities

Customers are responsible for:

* Having a lawful basis and authority to upload, import, sync, store, and process Customer Data through the Services.
* Providing legally required notices to employees, contractors, clients, Portal Users, and other Managed Persons, including notice of the information recorded when a handover form is signed.
* Obtaining legally required consents, approvals, works council approvals, internal authorizations, or third-party permissions.
* Deciding whether to enable the employee portal and handover forms, which people may use them, and when their access should be disabled.
* The wording of handover declarations, and whether an electronic handover form is suitable and legally sufficient for the Customer's purposes and jurisdictions.
* Ensuring that a Portal User's agreement to a handover declaration is not presented or relied on as consent to unrelated processing of personal data.
* Configuring connectors with appropriate permissions and limiting sync scope where possible.
* Managing user access, roles, company scopes, report recipients, reminder recipients, and external recipients, including for reports that contain employee-linked cost figures.
* Having the right to upload and display any logos or branding provided to the Services.
* Exporting any Handover Records or other Customer Data it needs to keep before deleting employees or the organization (see Section 10).
* Ensuring that Customer users do not enter prohibited sensitive data into notes, imports, asset records, network records, domain records, declarations, reports, or other free-text fields.
* Responding to rights requests from Managed Persons where the Customer is the controller.

If a Managed Person contacts us directly about Customer Data, we may direct the request to the relevant Customer unless applicable law requires otherwise.

***

### 6. Sensitive Data and Prohibited Content

Unless we expressly agree in writing, Customers must not upload, import, sync, store, or otherwise process:

* Sensitive personal data, special category data, biometric data, health data, medical data, regulated financial data, payment card data, government identifiers, criminal records, or children's data.
* Passwords, private keys, recovery phrases, API keys unrelated to supported features, production credentials, source code, trade secret repositories, or highly confidential business documents.
* Data that the Customer is not legally permitted to process through the Services.

This restriction does not prohibit use of supported fields for their intended purpose, such as encrypted software license keys, Microsoft Entra ID client secrets, Cloudflare API tokens, and drawn signature images on handover forms. Drawn signatures are stored as images and are not processed for biometric identification (see Section 3.4); Customers must not use them for that purpose.

***

### 7. Legal Bases for Processing

For Account Data we process as controller, our legal bases may include:

* Contractual necessity, to provide the Services and administer user accounts.
* Legitimate interests, such as security, fraud prevention, service reliability, product improvement, support, and business administration.
* Legal obligation, such as responding to lawful requests and maintaining required records.
* Consent, where required by applicable law, such as for certain optional analytics or communications.

For Customer Data we process as processor, including Handover Records and Portal User data, we process personal data on the Customer's instructions and for the purposes described in our agreements, this Privacy Policy, and the Services. The Customer is responsible for identifying the applicable legal basis for its processing. Signing a handover declaration records the signer's acknowledgment of the declaration; it is not, by itself, consent to the processing of personal data.

***

### 8. Sharing and Disclosure

We may disclose information to:

* Authorized Users within the Customer's organization, according to assigned roles, company access scopes, and permissions. This includes access to Handover Records and their PDFs.
* Portal Users, who can see the items assigned to them, the domains for which they are recorded as responsible, and their own Handover Records and PDFs.
* Customer-approved recipients, including report recipients, reminder recipients, same-domain recipients, employees, users, auditors, MSPs, external IT providers, or other addresses approved by Customer administrators. Exported or emailed reports may contain employee-linked financial figures, such as allocated costs.
* Service providers and subprocessors that help us host, operate, secure, monitor, email, analyze, support, or administer the Services, subject to appropriate confidentiality and data protection obligations. Transactional emails, including sign-in codes, portal sign-in emails, signature requests, unsigned-form reminders, reports, and reminders, are delivered through Amazon Web Services (Amazon SES).
* Service components operated by or for us, including connector sync workers, domain monitoring workers, reminder workers, warranty lookup workers, and administrative backoffice tools.
* Third-party connector providers, such as Microsoft and Cloudflare, where the Customer authorizes a connection. We generally retrieve data from these providers or use them for authentication; their services remain subject to their own terms and privacy practices.
* Public lookup and threat-intelligence services used for domain monitoring, including crt.sh, Cert Spotter (SSLMate), and, where configured, AlienVault OTX, which receive the domain names being checked. These services operate independently and are subject to their own terms and privacy practices.
* Professional advisers, insurers, auditors, and legal, tax, compliance, or security advisers.
* Regulators, courts, law enforcement, government authorities, or other parties when required by law, lawful request, subpoena, court order, or to protect rights, safety, security, or service integrity.
* Successors or potential successors in connection with a merger, acquisition, financing, reorganization, sale of assets, bankruptcy, or similar transaction, subject to appropriate confidentiality protections.

We do not sell personal information. We do not share personal information for cross-context behavioral advertising.

A list of subprocessors may be published on our website or made available upon request.

#### 8.1 Publicly Accessible Portal Logos

While a Customer's employee portal is enabled, the Customer's portal logo is served from a web address that does not require sign-in and that browsers and intermediate caches may store. Anyone with that address can view the logo. Disabling the portal stops the Services from serving the logo at that address, but copies already cached by browsers or networks may persist for some time. Customers should upload only logos they are content to make publicly viewable. Other Customer Data is not made public in this way.

***

### 9. Security

We use reasonable administrative, technical, and organizational safeguards designed to protect Customer Data and Account Data, including:

* Role-based access controls and tenant scoping.
* Authentication, email verification, password reset controls, session controls, and rate limiting.
* Emailed one-time sign-in codes that are stored as hashes, expire after a short period, and are limited by failed-attempt counters, together with trusted-browser controls that expire.
* Encryption in transit where HTTPS/TLS is properly configured.
* Encryption at rest for supported operational secrets such as connector secrets and software license keys.
* Hashes of signed Handover Records to help detect later changes.
* Security headers and application-level access checks.
* Operational logging for security, connector, report, email, and administrative events.
* Restricted internal access based on service operation, support, security, billing, or legal needs.

No transmission or storage system is completely secure. Customers are responsible for securing their own users, endpoints, identity providers, email systems, connector credentials, and third-party systems.

***

### 10. Retention and Deletion

We retain information for as long as reasonably necessary to provide the Services, comply with legal obligations, resolve disputes, enforce agreements, maintain security, and support legitimate business needs.

Customer Data is generally retained while the Customer account remains active or as otherwise instructed by the Customer. Customer administrators may delete certain records directly in the Services. Root organization deletion, where available, removes live Customer records from the production database after confirmation, subject to backups, logs, third-party records, and legal retention needs.

#### 10.1 Handover Records

Handover Records are stored as part of the related employee record. They are not archived separately or retained independently of that record:

* **Deleting an employee** in the Services also deletes that employee's Handover Records, including signed forms, return receipts, and related PDFs.
* **Deleting the organization** deletes all of its Handover Records.
* **Disabling the employee portal** or a Portal User's access prevents portal sign-in but does not, by itself, delete Handover Records. They remain available to Authorized Users until the employee or the organization is deleted.

Customers that need to keep signed forms, for example for audit or employment purposes, should download or export them before deleting the employee or the organization.

#### 10.2 Sign-In Codes and Trusted Browsers

Emailed sign-in codes stop working ten minutes after they are issued, or earlier once used. The expired code record is a separate matter: a background process periodically deletes code records that expired more than one day earlier. Trusted-browser cookies expire as described in Section 13.

#### 10.3 General Retention

Upon verified account termination or written deletion request, we will delete or de-identify Customer Data from active systems within 90 days unless a longer period is required by law, necessary for legal, security, fraud prevention, dispute resolution, backup integrity, or compliance purposes, or agreed in writing.

Backup copies may remain for a limited period according to the applicable backup retention cycle and are overwritten or deleted in the ordinary course of backup operations.

Security logs, report send audits, billing/account records, email delivery records, rate-limit records, backoffice audit records, system notification acknowledgments, and worker ledger records may be retained for longer where needed for security, compliance, accountability, support, or legal purposes.

Data held by third-party services, such as email providers, analytics providers, Microsoft, Cloudflare, domain lookup services, hosting providers, or Customer-connected systems, is subject to the retention practices of those providers and the Customer's own configuration. Copies of portal logos cached by browsers or networks may persist after the portal is disabled (see Section 8.1).

***

### 11. Privacy Rights

Depending on your jurisdiction, you may have rights to:

* Access personal information.
* Correct inaccurate personal information.
* Delete personal information.
* Restrict or object to processing.
* Receive personal information in a portable format.
* Withdraw consent where processing is based on consent.
* Appeal or complain to a regulator.
* Opt out of sale, sharing, targeted advertising, or certain profiling where applicable.

We do not sell personal information or share it for cross-context behavioral advertising.

If you are a Managed Person or Portal User whose data is processed on behalf of a Customer, including your Handover Records, please direct your request to that Customer, usually your employer or its IT provider. We will assist the Customer where required by law or agreement.

To exercise rights for Account Data that we control, contact us at info@itdirectory.app.

***

### 12. International Data Transfers

Your information may be processed in countries where we, our infrastructure providers, service providers, subprocessors, email delivery providers, domain lookup services, or Customer-authorized third-party services operate. These countries may have privacy laws different from those in your jurisdiction.

Where required, we rely on appropriate transfer mechanisms, such as adequacy decisions, Standard Contractual Clauses, equivalent contractual safeguards, or other lawful transfer mechanisms.

***

### 13. Cookies and Similar Technologies

We use cookies and similar technologies for the following purposes:

**Required cookies (sign-in and security)**

* Authentication session cookies that keep Authorized Users signed in to the web application.
* Employee portal session cookies that keep Portal Users signed in to the portal.
* A temporary organization-selection cookie used during portal sign-in to select the relevant organization.
* A short-lived SSO state cookie that protects the Microsoft Entra ID login flow.
* A trusted-browser cookie, lasting up to 30 days, that lets a browser that has completed emailed-code verification skip that step until it expires.

**Preference cookies and browser storage**

* A company-selection preference cookie, lasting up to one year, that remembers which company or sub-organization a user last selected.
* Browser local storage for non-sensitive interface preferences and state, such as the selected color theme (light or dark), which table columns are shown, and whether a browser has signed in before.

**Optional analytics**

* Google Analytics cookies and identifiers, if analytics is enabled by the deployment operator.

Google Analytics, when enabled, may set first-party cookies such as `_ga` and `_ga_<container-id>` to distinguish users and sessions and may collect usage, browser, device, approximate location, and session data.

You can control cookies through your browser settings. Blocking required cookies may prevent the Services or the employee portal from functioning. Clearing preference cookies or local storage resets those preferences. Where required by law, we will provide additional notice or obtain consent for optional analytics cookies.

***

### 14. Children's Privacy

The Services are intended for business use and are not directed to children. We do not knowingly collect personal information directly from children. Customers must not use the Services to process children's data, or enable the employee portal for children, unless expressly agreed in writing and legally permitted.

***

### 15. Vulnerability Reporting

If you discover a vulnerability or security issue affecting the Services, please report it to security@itdirectory.app. If that mailbox is unavailable, contact info@itdirectory.app.

***

### 16. Changes to This Policy

We may update this Privacy Policy from time to time. Material changes may be notified by email, platform banner, website notice, or other reasonable means. The updated policy will be effective when posted unless a later date is stated.

***

### 17. Contact Us

If you have questions, requests, or complaints about this Privacy Policy or our data practices, contact:

Email: info@itdirectory.app \
Security: security@itdirectory.app \
Website: https://itdirectory.app
