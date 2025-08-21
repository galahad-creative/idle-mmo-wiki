# Public API

The Public API is a RESTful service that allows authenticated access to various game endpoints. Whether you're building a personal tracker, or a guild management tool, the API provides the foundation for extending IdleMMO beyond the main interface.

### Getting Started

API keys can be generated from your [account settings](/settings/api). Each key can be configured with specific scopes to limit access to only the data you need. Full documentation of available endpoints, request formats, and response structures can be found on the API settings page.

>!banner The API uses Bearer token authentication. Include your API key in the Authorization header of all requests.

---

## Using API Keys in Third-Party Software

>!!banner <strong>Note:</strong> If you are creating a software that will be used by other players by yourself, this is a requirement. Failure to follow this will result in account suspension.

If you're developing software that will be used by other players, you **must** do the following:

- Disclose to the user how their data is being handled.
- Send all requests to the API using a custom user agent.

### Required Disclosures

Any application that accepts IdleMMO API keys from users must clearly display the following information before requesting access:

#### Data Storage and Retention

- **How is data obtained from the API stored?** 
  - Specify whether data is stored locally on the user's device, in a database, or not stored at all
  - If using cloud storage, indicate the provider and region

- **How is the API key itself stored?**
  - Detail your storage method (e.g., encrypted local storage, secure database, session-only memory)
  - If not stored, explain how authentication persists between sessions

- **How long is data retained?**
  - Define retention periods (e.g., until session close, 30 days, until account deletion)
  - Explain any automatic cleanup processes

#### Access and Privacy

- **Who can access the data besides the end user?**
  - List all parties with potential access (e.g., "Only the user", "Application developers for debugging", "Public leaderboards")
  - Specify any analytics or monitoring services used

- **What is the purpose of storing the data?**
  - Provide clear use cases (e.g., "Statistical analysis of drop rates", "Offline progress tracking", "Guild performance metrics")
  - Explain any secondary uses of the data

- **How can users request deletion of their data?**
  - Provide a clear process for data deletion requests
  - Include expected timeframe for deletion completion

#### Required Scopes

- **List all API scopes your application requires**
  - Explain why each scope is necessary
  - Indicate any optional scopes and their benefits

>!banner If your application does not have a UI (such as a Discord bot), you can list this disclosure using a third party application, such as GitHub gists.


### User Agent Requirements

>!!banner Applications intended for multiple users **must** set a custom User-Agent header identifying your application. This helps prevent service disruptions if multiple users access the API from the same server IP address.

Format: `ApplicationName/Version (Contact: your-email@example.com)`

Example: `IdleMMO-Tracker/1.2.3 (Contact: dev@tracker.app)`

---

## Terms and Conditions

**These API Terms supplement the main IdleMMO Terms of Service. By using the API, you agree to both sets of terms.**

### Rate Limiting

You **must** respect the rate limits imposed on your API key. Rate limits are enforced to ensure fair access for all users and maintain service stability.

- Standard rate limit: 20 requests per minute
- Upgraded rate limit: Manually set by IdleMMO administration upon request
- Exceeding rate limits will result in temporary blocks
- **Persistent violations will result in permanent revocation of API access**

>!!banner Excessive API calls that consistently hit rate limits will be investigated and may result in immediate suspension of API privileges.

### Authorized Endpoints Only

**You may only access endpoints that are publicly documented and begin with `/v1/`.**

- Only use endpoints listed in the official API documentation
- All authorized endpoints begin with `/v1/` (e.g., `/v1/auth/check`)
- **Accessing any other API endpoints is strictly forbidden**
- Attempting to access internal or undocumented endpoints will result in:
  - Immediate suspension of API access
  - Potential account suspension
  - IP address blocking

>!!banner Any attempt to access non-public API endpoints is considered a breach of service and will be dealt with severely.

### Account Restrictions

**Creating multiple accounts to bypass API limitations is strictly prohibited.**

- Each player is allowed **one** account only
- Creating additional accounts for API access will result in:
  - Permanent suspension of **all** associated accounts
  - Complete loss of game access (not just API access)
  - **No exceptions will be made**

>!!banner This is a zero-tolerance policy. Violations will result in immediate and permanent account termination.

### Fair Usage Policy

The API must be used in a manner that maintains game balance and fairness for all players.

- **Do not** use the API to gain unfair advantages over other players
- **Do not** automate gameplay beyond what the API explicitly allows
- **Do not** use the API to exploit game mechanics or bugs
- **Do not** create tools that negatively impact other players' experiences

### Monitoring and Enforcement

Your API usage is subject to routine monitoring to ensure compliance with these terms.

- Automated systems check for unusual patterns and potential abuse
- Manual reviews are conducted for suspicious activity
- Violations may result in:
  - Warning notifications
  - Temporary API suspension
  - Permanent API revocation
  - Full account suspension
  - IP address blocking

### Right to Refuse Service

**We reserve the absolute right to revoke API access at any time, for any reason.**

This includes but is not limited to:
- Violation of any terms listed here
- Activities deemed harmful to the game or community
- Use by specific applications or services we determine to be problematic
- Changes to game design or business requirements

### Liability and Warranty

The API is provided "as is" without any warranties or guarantees.

- We are not responsible for any losses due to API changes or downtime
- API endpoints may change or be removed without notice
- Rate limits and access restrictions may be modified at any time

---

### Additional Notes

>!banner API access is a privilege, not a right. Respect the service and your fellow players.

>!banner When in doubt about acceptable use, contact support at [idlemmo@galahadcreative.com](mailto:idlemmo@galahadcreative.com) before proceeding.

>!banner Commercial use of the API requires explicit written permission from Galahad Creative Ltd.
