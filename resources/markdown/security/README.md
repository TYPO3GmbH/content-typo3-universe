# Security related resources

## security.txt

The [`security.txt`](security.txt) file describes how security researchers and reporters
can contact the TYPO3 Security Team about vulnerabilities in TYPO3 Core and third-party
extensions. It follows the standards described in [RFC 9116](https://www.rfc-editor.org/info/rfc9116/).

For additional thrustworthiness, it is signed with the GPG key of the Security Team. The
signature is stored detached in the file [`security.txt.asc`](security.txt.asc). It must
be updated once the contents in `security.txt` change or a new key is issued.

### How to use

Both files should be placed at the following locations:

* `typo3.community/.well-known/security.txt`
* `typo3.community/.well-known/security.txt.asc`

In addition, the following redirects should be in place:

* `/security.txt -> /.well-known/security.txt`
* `/security.txt.asc -> /.well-known/security.txt.asc`

Next to the main `typo3.community` domain, all TYPO3-related domains such as `typo3.org`
or `typo3.com` should have redirects in place, for example:

* `typo3.org/.well-known/security.txt -> typo3.community/.well-known/security.txt`
* `typo3.org/.well-known/security.txt.asc -> typo3.community/.well-known/security.txt.asc`
* `typo3.org/security.txt -> typo3.community/security.txt`
* `typo3.org/security.txt.asc -> typo3.community/security.txt.asc`

This follows best practices regarding a single canonical URL for the `security.txt` file.
