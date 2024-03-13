Answers to Self-Review Questionnaire: Security and Privacy: Adding Cross-Site Ancestor Chain Bit to Partitioned Cookies.
Source of questions: https://www.w3.org/TR/security-privacy-questionnaire/

2.1 What information might this feature expose to Web sites or other parties, and for what purposes is that exposure necessary?

>This feature will expose if the Cookie was set in a cross-site context. It is necessary to include the value in partitioned cookies so that access to partitioned cookies can take into account the cookie’s cross site context when determining access.

2.2 Do features in your specification expose the minimum amount of information necessary to enable their intended uses?
>Yes, the only value that is exposed is the value of the bit.

2.3. How do the features in your specification deal with personal information, personally-identifiable information (PII), or information derived from them?
>There is no personal information or PII that can be derived from the value of the bit.

2.4. How do the features in your specification deal with sensitive information?

>There is no sensitive information that can be derived from the value of the bit.

2.5 Do the features in your specification introduce new state for an origin that persists across browsing sessions?

>Yes, this is a change to the CookieParitionKey and so it will be persisted across any browser sessions that Cookies can persist across already.

2.6. Do the features in your specification expose information about the underlying platform to origins?
>No, the value of the bit is not dependent on the the information of the underlying platform.

2.7. Does this specification allow an origin to send data to the underlying platform?

>No.

2.8. Do features in this specification enable access to device sensors?

>No.

2.9. Do features in this specification enable new script execution/loading mechanisms?

>No.

2.10. Do features in this specification allow an origin to access other devices?

No.

2.11. Do features in this specification allow an origin some measure of control over a user agent’s native UI?
>No.

2.12. What temporary identifiers do the features in this specification create or expose to the web?

>N/A

2.13. How does this specification distinguish between behavior in first-party and third-party contexts?

>The value of the bit can only be set in a first party context when the partitioned cookie is created. Third party contexts can read the value present by accessing the CookiePartitionKey.

2.14. How do the features in this specification work in the context of a browser’s Private Browsing or Incognito mode?
>The behavior is unchanged from the browser’s normal state.

2.15. Does this specification have both "Security Considerations" and "Privacy Considerations" sections?
>Yes, the specification does. https://github.com/explainers-by-googlers/CHIPS-spec/blob/main/draft-cutler-httpbis-partitioned-cookies.md

2.16. Do features in your specification enable origins to downgrade default security protections?
>No

2.17. How does your feature handle non-"fully active" documents?
>The status of a document being “full active” does not affect this feature
