Retest Result – Verbose Error Messages (12-August-2025)

The Verbose Error Messages vulnerability was retested on 12-August-2025 and found to be not remediated. During the retest, it was observed that the application continues to expose detailed error information when invalid or unexpected input is supplied.

The responses still display Java stack traces, Tomcat error details, and Hibernate Query Language (HQL) parsing exceptions, revealing internal class names, file paths, and partial query structures. Such verbose error output provides valuable insights into the backend technologies, frameworks, and database structure, which could be leveraged by attackers to identify potential weaknesses.

This confirms that the application has not implemented proper error handling or generic error responses, and sensitive debug information remains exposed.

Status: Not Remediated
Retest Result – User Input Reflected (12-August-2025)

The User Input Reflected vulnerability was retested on 12-August-2025 and found to be not remediated. During the retest, it was observed that the application continues to reflect user-supplied input in the response without proper sanitization or encoding.

Payloads inserted into input fields or parameters are still being reflected in the HTML response, confirming that user input is echoed back to the browser. Although no direct HTML or script execution was observed, this behavior could still aid an attacker in reconnaissance activities or serve as a vector for further exploitation under certain conditions.

This indicates that the application does not yet implement adequate input validation or output encoding to prevent reflection of user-controlled data.

Status: Not Remediated

Retest Result – Exposure of Internal Documentation via Help Page (12-August-2025)

The Exposure of Internal Documentation via Help Page vulnerability was retested on 12-August-2025 and found to be not remediated. During the retest, it was observed that the internal help or documentation page remains accessible to unauthenticated users.

Unauthenticated access to this page still reveals internal configuration details, operational guidance, and system-related information that could assist an attacker in understanding the application’s architecture or internal environment. This exposure continues to pose an information disclosure risk and could potentially aid in further targeted attacks.

This confirms that the application has not yet implemented proper authentication or access restrictions to limit access to internal documentation pages.

Status: Not Remediated


Retest Result – Verbose Error Messages (12-August-2025)

The Verbose Error Messages vulnerability was retested on 12-August-2025 and found to be partially remediated. During the retest, it was observed that the application no longer exposes Java stack traces or Tomcat error details, indicating that these issues have been successfully mitigated.

However, Hibernate Query Language (HQL) error details are still being displayed when invalid or unexpected input is provided. These error messages continue to reveal internal query structures, which could potentially assist an attacker in understanding database relationships and query logic.

This confirms that while the remediation efforts have addressed some aspects of verbose error handling, further action is required to suppress or sanitize HQL parsing errors to prevent information disclosure.

Status: Partially Remediated
