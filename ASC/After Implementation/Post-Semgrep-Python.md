# Semgrep Report

Total findings: **58**

## Summary

| Severity | Count |
|----------|------:|
| ERROR | 4 |
| INFO | 1 |
| WARNING | 53 |

---

## Findings

1. [python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host - app.py:483](#finding-1)
2. [python.flask.security.audit.debug-enabled.debug-enabled - app.py:483](#finding-2)
3. [python.cryptography.security.mode-without-authentication.crypto-mode-without-authentication - venv/lib/python3.12/site-packages/cryptography/fernet.py:156](#finding-3)
4. [python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:133](#finding-4)
5. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:134](#finding-5)
6. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:135](#finding-6)
7. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:144](#finding-7)
8. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:153](#finding-8)
9. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/primitives/serialization/ssh.py:1000](#finding-9)
10. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/x509/extensions.py:72](#finding-10)
11. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/face/sinter.py:136](#finding-11)
12. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/flask/sessions.py:285](#finding-12)
13. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/flask_wtf/csrf.py:53](#finding-13)
14. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/flask_wtf/csrf.py:58](#finding-14)
15. [python.flask.security.injection.tainted-url-host.tainted-url-host - venv/lib/python3.12/site-packages/flask_wtf/csrf.py:270](#finding-15)
16. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/google/protobuf/proto_builder.py:68](#finding-16)
17. [python.flask.security.audit.directly-returned-format-string.directly-returned-format-string - venv/lib/python3.12/site-packages/httpcore/_async/connection_pool.py:386](#finding-17)
18. [python.flask.security.audit.directly-returned-format-string.directly-returned-format-string - venv/lib/python3.12/site-packages/httpcore/_sync/connection_pool.py:386](#finding-18)
19. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/httpx/_auth.py:309](#finding-19)
20. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/itsdangerous/signer.py:45](#finding-20)
21. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/bccache.py:156](#finding-21)
22. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/bccache.py:165](#finding-22)
23. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/loaders.py:661](#finding-23)
24. [python.lang.security.audit.subprocess-shell-true.subprocess-shell-true - venv/lib/python3.12/site-packages/mcp/cli/cli.py:48](#finding-24)
25. [python.lang.security.audit.dangerous-os-exec-tainted-env-args.dangerous-os-exec-tainted-env-args - venv/lib/python3.12/site-packages/opentelemetry/instrumentation/auto_instrumentation/__init__.py:123](#finding-25)
26. [python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/peewee.py:3045](#finding-26)
27. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_internal/cache.py:30](#finding-27)
28. [python.lang.security.audit.subprocess-shell-true.subprocess-shell-true - venv/lib/python3.12/site-packages/pip/_internal/commands/configuration.py:247](#finding-28)
29. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:89](#finding-29)
30. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:96](#finding-30)
31. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:356](#finding-31)
32. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:372](#finding-32)
33. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:379](#finding-33)
34. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:392](#finding-34)
35. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:550](#finding-35)
36. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_internal/self_outdated_check.py:49](#finding-36)
37. [python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http - venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/_cmd.py:33](#finding-37)
38. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py:56](#finding-38)
39. [python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py:148](#finding-39)
40. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py:156](#finding-40)
41. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py:205](#finding-41)
42. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py:73](#finding-42)
43. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py:77](#finding-43)
44. [python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/playhouse/migrate.py:178](#finding-44)
45. [python.lang.security.insecure-uuid-version.insecure-uuid-version - venv/lib/python3.12/site-packages/playhouse/postgres_ext.py:492](#finding-45)
46. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py:124](#finding-46)
47. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py:129](#finding-47)
48. [python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/requests/auth.py:148](#finding-48)
49. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/requests/auth.py:156](#finding-49)
50. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/requests/auth.py:205](#finding-50)
51. [python.lang.security.audit.insecure-file-permissions.insecure-file-permissions - venv/lib/python3.12/site-packages/semgrep/commands/install.py:216](#finding-51)
52. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py:73](#finding-52)
53. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py:77](#finding-53)
54. [python.lang.security.audit.insecure-file-permissions.insecure-file-permissions - venv/lib/python3.12/site-packages/uvicorn/config.py:559](#finding-54)
55. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py:44](#finding-55)
56. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py:194](#finding-56)
57. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/http.py:956](#finding-57)
58. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/wtforms/csrf/session.py:47](#finding-58)

---

# Finding 1
<a name='finding-1'></a>

**Rule ID:** `python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host`

**Severity:** WARNING

**Message:** Running flask app with host 0.0.0.0 could expose the server publicly.

## Location

- File: `app.py`
- Start: Line 483, Column 5
- End: Line 483, Column 51

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-668: Exposure of Resource to Wrong Sphere
- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **category:** security
- **technology**
  - flask
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - vuln
- **likelihood:** HIGH
- **impact:** MEDIUM
- **confidence:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Other
- **source:** https://semgrep.dev/r/python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host
- **shortlink:** https://sg.run/eLby

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host",
  "path": "app.py",
  "start": {
    "line": 483,
    "col": 5,
    "offset": 16951
  },
  "end": {
    "line": 483,
    "col": 51,
    "offset": 16997
  },
  "extra": {
    "message": "Running flask app with host 0.0.0.0 could expose the server publicly.",
    "metadata": {
      "cwe": [
        "CWE-668: Exposure of Resource to Wrong Sphere"
      ],
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "HIGH",
      "impact": "MEDIUM",
      "confidence": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Other"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host",
      "shortlink": "https://sg.run/eLby"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 2
<a name='finding-2'></a>

**Rule ID:** `python.flask.security.audit.debug-enabled.debug-enabled`

**Severity:** WARNING

**Message:** Detected Flask app with debug=True. Do not deploy to production with this flag enabled as it will leak sensitive information. Instead, consider using Flask configuration variables or setting 'debug' using system environment variables.

## Location

- File: `app.py`
- Start: Line 483, Column 5
- End: Line 483, Column 51

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-489: Active Debug Code
- **owasp:** A06:2017 - Security Misconfiguration
- **references**
  - https://labs.detectify.com/2015/10/02/how-patreon-got-hacked-publicly-exposed-werkzeug-debugger/
- **category:** security
- **technology**
  - flask
- **subcategory**
  - vuln
- **likelihood:** HIGH
- **impact:** MEDIUM
- **confidence:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Active Debug Code
- **source:** https://semgrep.dev/r/python.flask.security.audit.debug-enabled.debug-enabled
- **shortlink:** https://sg.run/dKrd

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.audit.debug-enabled.debug-enabled",
  "path": "app.py",
  "start": {
    "line": 483,
    "col": 5,
    "offset": 16951
  },
  "end": {
    "line": 483,
    "col": 51,
    "offset": 16997
  },
  "extra": {
    "message": "Detected Flask app with debug=True. Do not deploy to production with this flag enabled as it will leak sensitive information. Instead, consider using Flask configuration variables or setting 'debug' using system environment variables.",
    "metadata": {
      "cwe": [
        "CWE-489: Active Debug Code"
      ],
      "owasp": "A06:2017 - Security Misconfiguration",
      "references": [
        "https://labs.detectify.com/2015/10/02/how-patreon-got-hacked-publicly-exposed-werkzeug-debugger/"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "HIGH",
      "impact": "MEDIUM",
      "confidence": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Active Debug Code"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.audit.debug-enabled.debug-enabled",
      "shortlink": "https://sg.run/dKrd"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 3
<a name='finding-3'></a>

**Rule ID:** `python.cryptography.security.mode-without-authentication.crypto-mode-without-authentication`

**Severity:** ERROR

**Message:** An encryption mode of operation is being used without proper message authentication. This can potentially result in the encrypted content to be decrypted by an attacker. Consider instead use an AEAD mode of operation like GCM. 

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/fernet.py`
- Start: Line 156, Column 21
- End: Line 156, Column 53

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **technology**
  - cryptography
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.mode-without-authentication.crypto-mode-without-authentication
- **shortlink:** https://sg.run/N9JL

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.mode-without-authentication.crypto-mode-without-authentication",
  "path": "venv/lib/python3.12/site-packages/cryptography/fernet.py",
  "start": {
    "line": 156,
    "col": 21,
    "offset": 4803
  },
  "end": {
    "line": 156,
    "col": 53,
    "offset": 4835
  },
  "extra": {
    "message": "An encryption mode of operation is being used without proper message authentication. This can potentially result in the encrypted content to be decrypted by an attacker. Consider instead use an AEAD mode of operation like GCM. ",
    "metadata": {
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.mode-without-authentication.crypto-mode-without-authentication",
      "shortlink": "https://sg.run/N9JL"
    },
    "severity": "ERROR",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 4
<a name='finding-4'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5`

**Severity:** WARNING

**Message:** Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py`
- Start: Line 133, Column 48
- End: Line 133, Column 51

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#md5
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5
- **shortlink:** https://sg.run/eY88

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py",
  "start": {
    "line": 133,
    "col": 48,
    "offset": 6585
  },
  "end": {
    "line": 133,
    "col": 51,
    "offset": 6588
  },
  "extra": {
    "message": "Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#md5",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
      "shortlink": "https://sg.run/eY88"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 5
<a name='finding-5'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py`
- Start: Line 134, Column 49
- End: Line 134, Column 53

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/J9Qy

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py",
  "start": {
    "line": 134,
    "col": 49,
    "offset": 6640
  },
  "end": {
    "line": 134,
    "col": 53,
    "offset": 6644
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/J9Qy"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 6
<a name='finding-6'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py`
- Start: Line 135, Column 50
- End: Line 135, Column 54

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/J9Qy

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py",
  "start": {
    "line": 135,
    "col": 50,
    "offset": 6697
  },
  "end": {
    "line": 135,
    "col": 54,
    "offset": 6701
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/J9Qy"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 7
<a name='finding-7'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py`
- Start: Line 144, Column 51
- End: Line 144, Column 55

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/J9Qy

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py",
  "start": {
    "line": 144,
    "col": 51,
    "offset": 7251
  },
  "end": {
    "line": 144,
    "col": 55,
    "offset": 7255
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/J9Qy"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 8
<a name='finding-8'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py`
- Start: Line 153, Column 49
- End: Line 153, Column 53

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/J9Qy

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py",
  "start": {
    "line": 153,
    "col": 49,
    "offset": 7819
  },
  "end": {
    "line": 153,
    "col": 53,
    "offset": 7823
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/J9Qy"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 9
<a name='finding-9'></a>

**Rule ID:** `python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/hazmat/primitives/serialization/ssh.py`
- Start: Line 1000, Column 35
- End: Line 1000, Column 39

## Proof of Concept

```
requires login
```

## Suggested Fix

```
SHA256
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **references**
  - https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - cryptography
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **functional-categories**
  - crypto::search::symmetric-algorithm::cryptography
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/J9Qy

## Raw Finding JSON

```json
{
  "check_id": "python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/hazmat/primitives/serialization/ssh.py",
  "start": {
    "line": 1000,
    "col": 35,
    "offset": 31155
  },
  "end": {
    "line": 1000,
    "col": 39,
    "offset": 31159
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "SHA256",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "references": [
        "https://cryptography.io/en/latest/hazmat/primitives/cryptographic-hashes/#sha-1",
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "cryptography"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "functional-categories": [
        "crypto::search::symmetric-algorithm::cryptography"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/J9Qy"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 10
<a name='finding-10'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/cryptography/x509/extensions.py`
- Start: Line 72, Column 12
- End: Line 72, Column 30

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(data)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/cryptography/x509/extensions.py",
  "start": {
    "line": 72,
    "col": 12,
    "offset": 2202
  },
  "end": {
    "line": 72,
    "col": 30,
    "offset": 2220
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(data)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 11
<a name='finding-11'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/face/sinter.py`
- Start: Line 136, Column 17
- End: Line 136, Column 54

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(code_str.encode('utf8'))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/face/sinter.py",
  "start": {
    "line": 136,
    "col": 17,
    "offset": 4552
  },
  "end": {
    "line": 136,
    "col": 54,
    "offset": 4589
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(code_str.encode('utf8'))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 12
<a name='finding-12'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/flask/sessions.py`
- Start: Line 285, Column 12
- End: Line 285, Column 32

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(string)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/flask/sessions.py",
  "start": {
    "line": 285,
    "col": 12,
    "offset": 11413
  },
  "end": {
    "line": 285,
    "col": 32,
    "offset": 11433
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(string)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 13
<a name='finding-13'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/flask_wtf/csrf.py`
- Start: Line 53, Column 35
- End: Line 53, Column 63

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(os.urandom(64))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/flask_wtf/csrf.py",
  "start": {
    "line": 53,
    "col": 35,
    "offset": 1659
  },
  "end": {
    "line": 53,
    "col": 63,
    "offset": 1687
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(os.urandom(64))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 14
<a name='finding-14'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/flask_wtf/csrf.py`
- Start: Line 58, Column 35
- End: Line 58, Column 63

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(os.urandom(64))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/flask_wtf/csrf.py",
  "start": {
    "line": 58,
    "col": 35,
    "offset": 1823
  },
  "end": {
    "line": 58,
    "col": 63,
    "offset": 1851
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(os.urandom(64))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 15
<a name='finding-15'></a>

**Rule ID:** `python.flask.security.injection.tainted-url-host.tainted-url-host`

**Severity:** WARNING

**Message:** User data flows into the host portion of this manually-constructed URL. This could allow an attacker to send data to their own server, potentially exposing sensitive data such as cookies or authorization information sent with this request. They could also probe internal servers or other resources that the server running this code can access. (This is called server-side request forgery, or SSRF.) Do not allow arbitrary hosts. Instead, create an allowlist for approved hosts, or hardcode the correct host.

## Location

- File: `venv/lib/python3.12/site-packages/flask_wtf/csrf.py`
- Start: Line 270, Column 29
- End: Line 270, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-918: Server-Side Request Forgery (SSRF)
- **owasp**
  - A10:2021 - Server-Side Request Forgery (SSRF)
  - A01:2025 - Broken Access Control
- **references**
  - https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **impact:** MEDIUM
- **likelihood:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Server-Side Request Forgery (SSRF)
- **source:** https://semgrep.dev/r/python.flask.security.injection.tainted-url-host.tainted-url-host
- **shortlink:** https://sg.run/RXpK

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.injection.tainted-url-host.tainted-url-host",
  "path": "venv/lib/python3.12/site-packages/flask_wtf/csrf.py",
  "start": {
    "line": 270,
    "col": 29,
    "offset": 8609
  },
  "end": {
    "line": 270,
    "col": 55,
    "offset": 8635
  },
  "extra": {
    "message": "User data flows into the host portion of this manually-constructed URL. This could allow an attacker to send data to their own server, potentially exposing sensitive data such as cookies or authorization information sent with this request. They could also probe internal servers or other resources that the server running this code can access. (This is called server-side request forgery, or SSRF.) Do not allow arbitrary hosts. Instead, create an allowlist for approved hosts, or hardcode the correct host.",
    "metadata": {
      "cwe": [
        "CWE-918: Server-Side Request Forgery (SSRF)"
      ],
      "owasp": [
        "A10:2021 - Server-Side Request Forgery (SSRF)",
        "A01:2025 - Broken Access Control"
      ],
      "references": [
        "https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "impact": "MEDIUM",
      "likelihood": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Server-Side Request Forgery (SSRF)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.injection.tainted-url-host.tainted-url-host",
      "shortlink": "https://sg.run/RXpK"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 16
<a name='finding-16'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/google/protobuf/proto_builder.py`
- Start: Line 68, Column 17
- End: Line 68, Column 31

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256()
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/google/protobuf/proto_builder.py",
  "start": {
    "line": 68,
    "col": 17,
    "offset": 2303
  },
  "end": {
    "line": 68,
    "col": 31,
    "offset": 2317
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256()",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 17
<a name='finding-17'></a>

**Rule ID:** `python.flask.security.audit.directly-returned-format-string.directly-returned-format-string`

**Severity:** WARNING

**Message:** Detected Flask route directly returning a formatted string. This is subject to cross-site scripting if user input can reach the string. Consider using the template engine instead and rendering pages with 'render_template()'.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_async/connection_pool.py`
- Start: Line 386, Column 9
- End: Line 386, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')
- **owasp**
  - A07:2017 - Cross-Site Scripting (XSS)
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **technology**
  - flask
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** HIGH
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.audit.directly-returned-format-string.directly-returned-format-string
- **shortlink:** https://sg.run/Zv6o

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.audit.directly-returned-format-string.directly-returned-format-string",
  "path": "venv/lib/python3.12/site-packages/httpcore/_async/connection_pool.py",
  "start": {
    "line": 386,
    "col": 9,
    "offset": 16191
  },
  "end": {
    "line": 386,
    "col": 71,
    "offset": 16253
  },
  "extra": {
    "message": "Detected Flask route directly returning a formatted string. This is subject to cross-site scripting if user input can reach the string. Consider using the template engine instead and rendering pages with 'render_template()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "HIGH",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.audit.directly-returned-format-string.directly-returned-format-string",
      "shortlink": "https://sg.run/Zv6o"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 18
<a name='finding-18'></a>

**Rule ID:** `python.flask.security.audit.directly-returned-format-string.directly-returned-format-string`

**Severity:** WARNING

**Message:** Detected Flask route directly returning a formatted string. This is subject to cross-site scripting if user input can reach the string. Consider using the template engine instead and rendering pages with 'render_template()'.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_sync/connection_pool.py`
- Start: Line 386, Column 9
- End: Line 386, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')
- **owasp**
  - A07:2017 - Cross-Site Scripting (XSS)
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **technology**
  - flask
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** HIGH
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.audit.directly-returned-format-string.directly-returned-format-string
- **shortlink:** https://sg.run/Zv6o

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.audit.directly-returned-format-string.directly-returned-format-string",
  "path": "venv/lib/python3.12/site-packages/httpcore/_sync/connection_pool.py",
  "start": {
    "line": 386,
    "col": 9,
    "offset": 15905
  },
  "end": {
    "line": 386,
    "col": 71,
    "offset": 15967
  },
  "extra": {
    "message": "Detected Flask route directly returning a formatted string. This is subject to cross-site scripting if user input can reach the string. Consider using the template engine instead and rendering pages with 'render_template()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "HIGH",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.audit.directly-returned-format-string.directly-returned-format-string",
      "shortlink": "https://sg.run/Zv6o"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 19
<a name='finding-19'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/httpx/_auth.py`
- Start: Line 309, Column 16
- End: Line 309, Column 31

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(s)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/httpx/_auth.py",
  "start": {
    "line": 309,
    "col": 16,
    "offset": 10620
  },
  "end": {
    "line": 309,
    "col": 31,
    "offset": 10635
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(s)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 20
<a name='finding-20'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/itsdangerous/signer.py`
- Start: Line 45, Column 12
- End: Line 45, Column 32

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(string)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/itsdangerous/signer.py",
  "start": {
    "line": 45,
    "col": 12,
    "offset": 1339
  },
  "end": {
    "line": 45,
    "col": 32,
    "offset": 1359
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(string)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 21
<a name='finding-21'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 156, Column 16
- End: Line 156, Column 42

## Proof of Concept

```
requires login
```

## Suggested Fix

```
sha256(name.encode("utf-8"))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 156,
    "col": 16,
    "offset": 5186
  },
  "end": {
    "line": 156,
    "col": 42,
    "offset": 5212
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "sha256(name.encode(\"utf-8\"))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 22
<a name='finding-22'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 165, Column 16
- End: Line 165, Column 44

## Proof of Concept

```
requires login
```

## Suggested Fix

```
sha256(source.encode("utf-8"))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 165,
    "col": 16,
    "offset": 5449
  },
  "end": {
    "line": 165,
    "col": 44,
    "offset": 5477
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "sha256(source.encode(\"utf-8\"))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 23
<a name='finding-23'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/loaders.py`
- Start: Line 661, Column 26
- End: Line 661, Column 52

## Proof of Concept

```
requires login
```

## Suggested Fix

```
sha256(name.encode("utf-8"))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/jinja2/loaders.py",
  "start": {
    "line": 661,
    "col": 26,
    "offset": 23015
  },
  "end": {
    "line": 661,
    "col": 52,
    "offset": 23041
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "sha256(name.encode(\"utf-8\"))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 24
<a name='finding-24'></a>

**Rule ID:** `python.lang.security.audit.subprocess-shell-true.subprocess-shell-true`

**Severity:** ERROR

**Message:** Found 'subprocess' function 'run' with 'shell=True'. This is dangerous because this call will spawn the command using a shell process. Doing so propagates current shell settings and variables, which makes it much easier for a malicious actor to execute commands. Use 'shell=False' instead.

## Location

- File: `venv/lib/python3.12/site-packages/mcp/cli/cli.py`
- Start: Line 48, Column 91
- End: Line 48, Column 95

## Proof of Concept

```
requires login
```

## Suggested Fix

```
False
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b602_subprocess_popen_with_shell_equals_true.html
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')
- **references**
  - https://stackoverflow.com/questions/3172470/actual-meaning-of-shell-true-in-subprocess
  - https://docs.python.org/3/library/subprocess.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - secure default
- **likelihood:** HIGH
- **impact:** LOW
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Command Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.subprocess-shell-true.subprocess-shell-true
- **shortlink:** https://sg.run/J92w

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.subprocess-shell-true.subprocess-shell-true",
  "path": "venv/lib/python3.12/site-packages/mcp/cli/cli.py",
  "start": {
    "line": 48,
    "col": 91,
    "offset": 1232
  },
  "end": {
    "line": 48,
    "col": 95,
    "offset": 1236
  },
  "extra": {
    "message": "Found 'subprocess' function 'run' with 'shell=True'. This is dangerous because this call will spawn the command using a shell process. Doing so propagates current shell settings and variables, which makes it much easier for a malicious actor to execute commands. Use 'shell=False' instead.",
    "fix": "False",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b602_subprocess_popen_with_shell_equals_true.html",
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/3172470/actual-meaning-of-shell-true-in-subprocess",
        "https://docs.python.org/3/library/subprocess.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "secure default"
      ],
      "likelihood": "HIGH",
      "impact": "LOW",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Command Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.subprocess-shell-true.subprocess-shell-true",
      "shortlink": "https://sg.run/J92w"
    },
    "severity": "ERROR",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 25
<a name='finding-25'></a>

**Rule ID:** `python.lang.security.audit.dangerous-os-exec-tainted-env-args.dangerous-os-exec-tainted-env-args`

**Severity:** ERROR

**Message:** Found user controlled content when spawning a process. This is dangerous because it allows a malicious actor to execute commands.

## Location

- File: `venv/lib/python3.12/site-packages/opentelemetry/instrumentation/auto_instrumentation/__init__.py`
- Start: Line 123, Column 5
- End: Line 123, Column 54

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://semgrep.dev/docs/cheat-sheets/python-command-injection/
- **asvs**
  - control_id: 5.3.8 OS Command Injection
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v53-output-encoding-and-injection-prevention-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **confidence:** MEDIUM
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** MEDIUM
- **impact:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Command Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-os-exec-tainted-env-args.dangerous-os-exec-tainted-env-args
- **shortlink:** https://sg.run/qL6z

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-os-exec-tainted-env-args.dangerous-os-exec-tainted-env-args",
  "path": "venv/lib/python3.12/site-packages/opentelemetry/instrumentation/auto_instrumentation/__init__.py",
  "start": {
    "line": 123,
    "col": 5,
    "offset": 4138
  },
  "end": {
    "line": 123,
    "col": 54,
    "offset": 4187
  },
  "extra": {
    "message": "Found user controlled content when spawning a process. This is dangerous because it allows a malicious actor to execute commands.",
    "metadata": {
      "cwe": [
        "CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://semgrep.dev/docs/cheat-sheets/python-command-injection/"
      ],
      "asvs": {
        "control_id": "5.3.8 OS Command Injection",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v53-output-encoding-and-injection-prevention-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "confidence": "MEDIUM",
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "MEDIUM",
      "impact": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Command Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-os-exec-tainted-env-args.dangerous-os-exec-tainted-env-args",
      "shortlink": "https://sg.run/qL6z"
    },
    "severity": "ERROR",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 26
<a name='finding-26'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5`

**Severity:** WARNING

**Message:** Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 3045, Column 21
- End: Line 3045, Column 60

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5
- **shortlink:** https://sg.run/vYrY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 3045,
    "col": 21,
    "offset": 94618
  },
  "end": {
    "line": 3045,
    "col": 60,
    "offset": 94657
  },
  "extra": {
    "message": "Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
      "shortlink": "https://sg.run/vYrY"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 27
<a name='finding-27'></a>

**Rule ID:** `python.lang.security.audit.sha224-hash.sha224-hash`

**Severity:** WARNING

**Message:** This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/cache.py`
- Start: Line 30, Column 12
- End: Line 30, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **references**
  - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf
  - https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash
- **shortlink:** https://sg.run/Db1Yv

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.sha224-hash.sha224-hash",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/cache.py",
  "start": {
    "line": 30,
    "col": 12,
    "offset": 878
  },
  "end": {
    "line": 30,
    "col": 45,
    "offset": 911
  },
  "extra": {
    "message": "This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.",
    "metadata": {
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "references": [
        "https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf",
        "https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash",
      "shortlink": "https://sg.run/Db1Yv"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 28
<a name='finding-28'></a>

**Rule ID:** `python.lang.security.audit.subprocess-shell-true.subprocess-shell-true`

**Severity:** ERROR

**Message:** Found 'subprocess' function 'check_call' with 'shell=True'. This is dangerous because this call will spawn the command using a shell process. Doing so propagates current shell settings and variables, which makes it much easier for a malicious actor to execute commands. Use 'shell=False' instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/commands/configuration.py`
- Start: Line 247, Column 64
- End: Line 247, Column 68

## Proof of Concept

```
requires login
```

## Suggested Fix

```
False
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b602_subprocess_popen_with_shell_equals_true.html
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')
- **references**
  - https://stackoverflow.com/questions/3172470/actual-meaning-of-shell-true-in-subprocess
  - https://docs.python.org/3/library/subprocess.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - secure default
- **likelihood:** HIGH
- **impact:** LOW
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Command Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.subprocess-shell-true.subprocess-shell-true
- **shortlink:** https://sg.run/J92w

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.subprocess-shell-true.subprocess-shell-true",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/commands/configuration.py",
  "start": {
    "line": 247,
    "col": 64,
    "offset": 8629
  },
  "end": {
    "line": 247,
    "col": 68,
    "offset": 8633
  },
  "extra": {
    "message": "Found 'subprocess' function 'check_call' with 'shell=True'. This is dangerous because this call will spawn the command using a shell process. Doing so propagates current shell settings and variables, which makes it much easier for a malicious actor to execute commands. Use 'shell=False' instead.",
    "fix": "False",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b602_subprocess_popen_with_shell_equals_true.html",
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-78: Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/3172470/actual-meaning-of-shell-true-in-subprocess",
        "https://docs.python.org/3/library/subprocess.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "secure default"
      ],
      "likelihood": "HIGH",
      "impact": "LOW",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Command Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.subprocess-shell-true.subprocess-shell-true",
      "shortlink": "https://sg.run/J92w"
    },
    "severity": "ERROR",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 29
<a name='finding-29'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Getting credentials from keyring for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 89, Column 13
- End: Line 89, Column 73

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 89,
    "col": 13,
    "offset": 2262
  },
  "end": {
    "line": 89,
    "col": 73,
    "offset": 2322
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Getting credentials from keyring for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 30
<a name='finding-30'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Getting password from keyring for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 96, Column 13
- End: Line 96, Column 70

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 96,
    "col": 13,
    "offset": 2540
  },
  "end": {
    "line": 96,
    "col": 70,
    "offset": 2597
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Getting password from keyring for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 31
<a name='finding-31'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Found credentials in url for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 356, Column 13
- End: Line 356, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 356,
    "col": 13,
    "offset": 12037
  },
  "end": {
    "line": 356,
    "col": 68,
    "offset": 12092
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Found credentials in url for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 32
<a name='finding-32'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Found credentials in index url for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 372, Column 17
- End: Line 372, Column 78

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 372,
    "col": 17,
    "offset": 12787
  },
  "end": {
    "line": 372,
    "col": 78,
    "offset": 12848
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Found credentials in index url for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 33
<a name='finding-33'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Found credentials in netrc for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 379, Column 17
- End: Line 379, Column 74

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 379,
    "col": 17,
    "offset": 13077
  },
  "end": {
    "line": 379,
    "col": 74,
    "offset": 13134
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Found credentials in netrc for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 34
<a name='finding-34'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "Found credentials in keyring for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 392, Column 17
- End: Line 392, Column 76

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 392,
    "col": 17,
    "offset": 13589
  },
  "end": {
    "line": 392,
    "col": 76,
    "offset": 13648
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"Found credentials in keyring for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 35
<a name='finding-35'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret "401 Error, Credentials not correct for %s" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/auth.py`
- Start: Line 550, Column 13
- End: Line 553, Column 14

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/auth.py",
  "start": {
    "line": 550,
    "col": 13,
    "offset": 20035
  },
  "end": {
    "line": 553,
    "col": 14,
    "offset": 20159
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret \"401 Error, Credentials not correct for %s\" being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 36
<a name='finding-36'></a>

**Rule ID:** `python.lang.security.audit.sha224-hash.sha224-hash`

**Severity:** WARNING

**Message:** This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/self_outdated_check.py`
- Start: Line 49, Column 12
- End: Line 49, Column 37

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **references**
  - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf
  - https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash
- **shortlink:** https://sg.run/Db1Yv

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.sha224-hash.sha224-hash",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/self_outdated_check.py",
  "start": {
    "line": 49,
    "col": 12,
    "offset": 1425
  },
  "end": {
    "line": 49,
    "col": 37,
    "offset": 1450
  },
  "extra": {
    "message": "This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.",
    "metadata": {
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "references": [
        "https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf",
        "https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash",
      "shortlink": "https://sg.run/Db1Yv"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 37
<a name='finding-37'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http`

**Severity:** INFO

**Message:** Detected a request using 'http://'. This request will be unencrypted. Use 'https://' instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/_cmd.py`
- Start: Line 33, Column 16
- End: Line 33, Column 25

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **asvs**
  - control_id: 9.1.1 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v92-server-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - requests
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http
- **shortlink:** https://sg.run/DoBY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/_cmd.py",
  "start": {
    "line": 33,
    "col": 16,
    "offset": 867
  },
  "end": {
    "line": 33,
    "col": 25,
    "offset": 876
  },
  "extra": {
    "message": "Detected a request using 'http://'. This request will be unencrypted. Use 'https://' instead.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "asvs": {
        "control_id": "9.1.1 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v92-server-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "requests"
      ],
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http",
      "shortlink": "https://sg.run/DoBY"
    },
    "severity": "INFO",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 38
<a name='finding-38'></a>

**Rule ID:** `python.lang.security.audit.sha224-hash.sha224-hash`

**Severity:** WARNING

**Message:** This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py`
- Start: Line 56, Column 16
- End: Line 56, Column 42

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **references**
  - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf
  - https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** HIGH
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash
- **shortlink:** https://sg.run/Db1Yv

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.sha224-hash.sha224-hash",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py",
  "start": {
    "line": 56,
    "col": 16,
    "offset": 1479
  },
  "end": {
    "line": 56,
    "col": 42,
    "offset": 1505
  },
  "extra": {
    "message": "This code uses a 224-bit hash function, which is deprecated or disallowed in some security policies. Consider updating to a stronger hash function such as SHA-384 or higher to ensure compliance and security.",
    "metadata": {
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "references": [
        "https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar3.ipd.pdf",
        "https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-cryptography"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "HIGH",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.sha224-hash.sha224-hash",
      "shortlink": "https://sg.run/Db1Yv"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 39
<a name='finding-39'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5`

**Severity:** WARNING

**Message:** Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py`
- Start: Line 148, Column 24
- End: Line 148, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5
- **shortlink:** https://sg.run/vYrY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py",
  "start": {
    "line": 148,
    "col": 24,
    "offset": 4579
  },
  "end": {
    "line": 148,
    "col": 38,
    "offset": 4593
  },
  "extra": {
    "message": "Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
      "shortlink": "https://sg.run/vYrY"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 40
<a name='finding-40'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py`
- Start: Line 156, Column 24
- End: Line 156, Column 39

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(x)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py",
  "start": {
    "line": 156,
    "col": 24,
    "offset": 4808
  },
  "end": {
    "line": 156,
    "col": 39,
    "offset": 4823
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(x)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 41
<a name='finding-41'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py`
- Start: Line 205, Column 18
- End: Line 205, Column 33

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(s)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py",
  "start": {
    "line": 205,
    "col": 18,
    "offset": 6293
  },
  "end": {
    "line": 205,
    "col": 33,
    "offset": 6308
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(s)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 42
<a name='finding-42'></a>

**Rule ID:** `python.lang.security.audit.weak-ssl-version.weak-ssl-version`

**Severity:** WARNING

**Message:** An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py`
- Start: Line 73, Column 5
- End: Line 73, Column 23

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-326: Inadequate Encryption Strength
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://tools.ietf.org/html/rfc7568
  - https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html
  - https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version
- **shortlink:** https://sg.run/RoZO

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.weak-ssl-version.weak-ssl-version",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py",
  "start": {
    "line": 73,
    "col": 5,
    "offset": 2242
  },
  "end": {
    "line": 73,
    "col": 23,
    "offset": 2260
  },
  "extra": {
    "message": "An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.",
    "metadata": {
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30",
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://tools.ietf.org/html/rfc7568",
        "https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html",
        "https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version",
      "shortlink": "https://sg.run/RoZO"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 43
<a name='finding-43'></a>

**Rule ID:** `python.lang.security.audit.weak-ssl-version.weak-ssl-version`

**Severity:** WARNING

**Message:** An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py`
- Start: Line 77, Column 23
- End: Line 77, Column 43

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-326: Inadequate Encryption Strength
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://tools.ietf.org/html/rfc7568
  - https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html
  - https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version
- **shortlink:** https://sg.run/RoZO

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.weak-ssl-version.weak-ssl-version",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py",
  "start": {
    "line": 77,
    "col": 23,
    "offset": 2393
  },
  "end": {
    "line": 77,
    "col": 43,
    "offset": 2413
  },
  "extra": {
    "message": "An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.",
    "metadata": {
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30",
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://tools.ietf.org/html/rfc7568",
        "https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html",
        "https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version",
      "shortlink": "https://sg.run/RoZO"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 44
<a name='finding-44'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5`

**Severity:** WARNING

**Message:** Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/migrate.py`
- Start: Line 178, Column 22
- End: Line 178, Column 61

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5
- **shortlink:** https://sg.run/vYrY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
  "path": "venv/lib/python3.12/site-packages/playhouse/migrate.py",
  "start": {
    "line": 178,
    "col": 22,
    "offset": 5015
  },
  "end": {
    "line": 178,
    "col": 61,
    "offset": 5054
  },
  "extra": {
    "message": "Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
      "shortlink": "https://sg.run/vYrY"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 45
<a name='finding-45'></a>

**Rule ID:** `python.lang.security.insecure-uuid-version.insecure-uuid-version`

**Severity:** WARNING

**Message:** Using UUID version 1 for UUID generation can lead to predictable UUIDs based on system information (e.g., MAC address, timestamp). This may lead to security risks such as the sandwich attack. Consider using `uuid.uuid4()` instead for better randomness and security.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/postgres_ext.py`
- Start: Line 492, Column 53
- End: Line 492, Column 65

## Proof of Concept

```
requires login
```

## Suggested Fix

```
uuid.uuid4()
```

## Metadata

- **references**
  - https://www.landh.tech/blog/20230811-sandwich-attack/
- **cwe**
  - CWE-330: Use of Insufficiently Random Values
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **asvs**
  - control_id: 6.3.2 Insecure UUID Generation
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v63-random-values
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-uuid-version.insecure-uuid-version
- **shortlink:** https://sg.run/BYBgW

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-uuid-version.insecure-uuid-version",
  "path": "venv/lib/python3.12/site-packages/playhouse/postgres_ext.py",
  "start": {
    "line": 492,
    "col": 53,
    "offset": 14148
  },
  "end": {
    "line": 492,
    "col": 65,
    "offset": 14160
  },
  "extra": {
    "message": "Using UUID version 1 for UUID generation can lead to predictable UUIDs based on system information (e.g., MAC address, timestamp). This may lead to security risks such as the sandwich attack. Consider using `uuid.uuid4()` instead for better randomness and security.",
    "fix": "uuid.uuid4()",
    "metadata": {
      "references": [
        "https://www.landh.tech/blog/20230811-sandwich-attack/"
      ],
      "cwe": [
        "CWE-330: Use of Insufficiently Random Values"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "asvs": {
        "control_id": "6.3.2 Insecure UUID Generation",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v63-random-values",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-uuid-version.insecure-uuid-version",
      "shortlink": "https://sg.run/BYBgW"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 46
<a name='finding-46'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret 'Secret file not found, skipping: %s' being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py`
- Start: Line 124, Column 25
- End: Line 124, Column 113

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py",
  "start": {
    "line": 124,
    "col": 25,
    "offset": 4182
  },
  "end": {
    "line": 124,
    "col": 113,
    "offset": 4270
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret 'Secret file not found, skipping: %s' being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 47
<a name='finding-47'></a>

**Rule ID:** `python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure`

**Severity:** WARNING

**Message:** Detected a python logger call with a potential hardcoded secret 'Loading secret file: %s' being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py`
- Start: Line 129, Column 25
- End: Line 129, Column 80

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-532: Insertion of Sensitive Information into Log File
- **category:** security
- **technology**
  - python
- **owasp**
  - A09:2021 - Security Logging and Monitoring Failures
  - A09:2025 - Security Logging & Alerting Failures
- **references**
  - https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure
- **shortlink:** https://sg.run/ydNx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
  "path": "venv/lib/python3.12/site-packages/pydantic_settings/sources/providers/secrets.py",
  "start": {
    "line": 129,
    "col": 25,
    "offset": 4390
  },
  "end": {
    "line": 129,
    "col": 80,
    "offset": 4445
  },
  "extra": {
    "message": "Detected a python logger call with a potential hardcoded secret 'Loading secret file: %s' being logged. This may lead to secret credentials being exposed. Make sure that the logger is not logging  sensitive information.",
    "metadata": {
      "cwe": [
        "CWE-532: Insertion of Sensitive Information into Log File"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "owasp": [
        "A09:2021 - Security Logging and Monitoring Failures",
        "A09:2025 - Security Logging & Alerting Failures"
      ],
      "references": [
        "https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure",
      "shortlink": "https://sg.run/ydNx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 48
<a name='finding-48'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5`

**Severity:** WARNING

**Message:** Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/requests/auth.py`
- Start: Line 148, Column 24
- End: Line 148, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5
- **shortlink:** https://sg.run/vYrY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
  "path": "venv/lib/python3.12/site-packages/requests/auth.py",
  "start": {
    "line": 148,
    "col": 24,
    "offset": 4595
  },
  "end": {
    "line": 148,
    "col": 38,
    "offset": 4609
  },
  "extra": {
    "message": "Detected MD5 hash algorithm which is considered insecure. MD5 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5",
      "shortlink": "https://sg.run/vYrY"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 49
<a name='finding-49'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/requests/auth.py`
- Start: Line 156, Column 24
- End: Line 156, Column 39

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(x)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/requests/auth.py",
  "start": {
    "line": 156,
    "col": 24,
    "offset": 4824
  },
  "end": {
    "line": 156,
    "col": 39,
    "offset": 4839
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(x)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 50
<a name='finding-50'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/requests/auth.py`
- Start: Line 205, Column 18
- End: Line 205, Column 33

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(s)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/requests/auth.py",
  "start": {
    "line": 205,
    "col": 18,
    "offset": 6309
  },
  "end": {
    "line": 205,
    "col": 33,
    "offset": 6324
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(s)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 51
<a name='finding-51'></a>

**Rule ID:** `python.lang.security.audit.insecure-file-permissions.insecure-file-permissions`

**Severity:** WARNING

**Message:** These permissions `os.stat(semgrep_pro_path_tmp).st_mode
        | stat.S_IEXEC
        | stat.S_IXGRP
        | stat.S_IXOTH` are widely permissive and grant access to more people than may be necessary. A good default is `0o644` which gives read and write access to yourself and read access to everyone else.

## Location

- File: `venv/lib/python3.12/site-packages/semgrep/commands/install.py`
- Start: Line 216, Column 5
- End: Line 222, Column 6

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-276: Incorrect Default Permissions
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-file-permissions.insecure-file-permissions
- **shortlink:** https://sg.run/AXY4

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-file-permissions.insecure-file-permissions",
  "path": "venv/lib/python3.12/site-packages/semgrep/commands/install.py",
  "start": {
    "line": 216,
    "col": 5,
    "offset": 8554
  },
  "end": {
    "line": 222,
    "col": 6,
    "offset": 8715
  },
  "extra": {
    "message": "These permissions `os.stat(semgrep_pro_path_tmp).st_mode\n        | stat.S_IEXEC\n        | stat.S_IXGRP\n        | stat.S_IXOTH` are widely permissive and grant access to more people than may be necessary. A good default is `0o644` which gives read and write access to yourself and read access to everyone else.",
    "metadata": {
      "category": "security",
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-276: Incorrect Default Permissions"
      ],
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-file-permissions.insecure-file-permissions",
      "shortlink": "https://sg.run/AXY4"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 52
<a name='finding-52'></a>

**Rule ID:** `python.lang.security.audit.weak-ssl-version.weak-ssl-version`

**Severity:** WARNING

**Message:** An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.

## Location

- File: `venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py`
- Start: Line 73, Column 5
- End: Line 73, Column 23

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-326: Inadequate Encryption Strength
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://tools.ietf.org/html/rfc7568
  - https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html
  - https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version
- **shortlink:** https://sg.run/RoZO

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.weak-ssl-version.weak-ssl-version",
  "path": "venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py",
  "start": {
    "line": 73,
    "col": 5,
    "offset": 2233
  },
  "end": {
    "line": 73,
    "col": 23,
    "offset": 2251
  },
  "extra": {
    "message": "An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.",
    "metadata": {
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30",
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://tools.ietf.org/html/rfc7568",
        "https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html",
        "https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version",
      "shortlink": "https://sg.run/RoZO"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 53
<a name='finding-53'></a>

**Rule ID:** `python.lang.security.audit.weak-ssl-version.weak-ssl-version`

**Severity:** WARNING

**Message:** An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.

## Location

- File: `venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py`
- Start: Line 77, Column 23
- End: Line 77, Column 43

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-326: Inadequate Encryption Strength
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://tools.ietf.org/html/rfc7568
  - https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html
  - https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version
- **shortlink:** https://sg.run/RoZO

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.weak-ssl-version.weak-ssl-version",
  "path": "venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py",
  "start": {
    "line": 77,
    "col": 23,
    "offset": 2384
  },
  "end": {
    "line": 77,
    "col": 43,
    "offset": 2404
  },
  "extra": {
    "message": "An insecure SSL version was detected. TLS versions 1.0, 1.1, and all SSL versions are considered weak encryption and are deprecated. Use 'ssl.PROTOCOL_TLSv1_2' or higher.",
    "metadata": {
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/plugins/insecure_ssl_tls.py#L30",
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://tools.ietf.org/html/rfc7568",
        "https://tools.ietf.org/id/draft-ietf-tls-oldversions-deprecate-02.html",
        "https://docs.python.org/3/library/ssl.html#ssl.PROTOCOL_TLSv1_2"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.weak-ssl-version.weak-ssl-version",
      "shortlink": "https://sg.run/RoZO"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 54
<a name='finding-54'></a>

**Rule ID:** `python.lang.security.audit.insecure-file-permissions.insecure-file-permissions`

**Severity:** WARNING

**Message:** These permissions `uds_perms` are widely permissive and grant access to more people than may be necessary. A good default is `0o644` which gives read and write access to yourself and read access to everyone else.

## Location

- File: `venv/lib/python3.12/site-packages/uvicorn/config.py`
- Start: Line 559, Column 17
- End: Line 559, Column 46

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-276: Incorrect Default Permissions
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-file-permissions.insecure-file-permissions
- **shortlink:** https://sg.run/AXY4

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-file-permissions.insecure-file-permissions",
  "path": "venv/lib/python3.12/site-packages/uvicorn/config.py",
  "start": {
    "line": 559,
    "col": 17,
    "offset": 22537
  },
  "end": {
    "line": 559,
    "col": 46,
    "offset": 22566
  },
  "extra": {
    "message": "These permissions `uds_perms` are widely permissive and grant access to more people than may be necessary. A good default is `0o644` which gives read and write access to yourself and read access to everyone else.",
    "metadata": {
      "category": "security",
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-276: Incorrect Default Permissions"
      ],
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-file-permissions.insecure-file-permissions",
      "shortlink": "https://sg.run/AXY4"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 55
<a name='finding-55'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py`
- Start: Line 44, Column 12
- End: Line 44, Column 72

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256(f"{pin} added salt".encode("utf-8", "replace"))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py",
  "start": {
    "line": 44,
    "col": 12,
    "offset": 1037
  },
  "end": {
    "line": 44,
    "col": 72,
    "offset": 1097
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256(f\"{pin} added salt\".encode(\"utf-8\", \"replace\"))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 56
<a name='finding-56'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py`
- Start: Line 194, Column 9
- End: Line 194, Column 23

## Proof of Concept

```
requires login
```

## Suggested Fix

```
hashlib.sha256()
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py",
  "start": {
    "line": 194,
    "col": 9,
    "offset": 5695
  },
  "end": {
    "line": 194,
    "col": 23,
    "offset": 5709
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "hashlib.sha256()",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 57
<a name='finding-57'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/http.py`
- Start: Line 956, Column 12
- End: Line 956, Column 22

## Proof of Concept

```
requires login
```

## Suggested Fix

```
sha256(data)
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/werkzeug/http.py",
  "start": {
    "line": 956,
    "col": 12,
    "offset": 29138
  },
  "end": {
    "line": 956,
    "col": 22,
    "offset": 29148
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "sha256(data)",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---

# Finding 58
<a name='finding-58'></a>

**Rule ID:** `python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1`

**Severity:** WARNING

**Message:** Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.

## Location

- File: `venv/lib/python3.12/site-packages/wtforms/csrf/session.py`
- Start: Line 47, Column 31
- End: Line 47, Column 51

## Proof of Concept

```
requires login
```

## Suggested Fix

```
sha256(os.urandom(64))
```

## Metadata

- **source-rule-url:** https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59
- **cwe**
  - CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **bandit-code:** B303
- **asvs**
  - control_id: 6.2.2 Insecure Custom Algorithm
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms
  - section: V6 Stored Cryptography Verification Requirements
  - version: 4
- **references**
  - https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html
  - https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability
  - http://2012.sharcs.org/slides/stevens.pdf
  - https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html
- **category:** security
- **technology**
  - python
- **subcategory**
  - vuln
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1
- **shortlink:** https://sg.run/ydYx

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
  "path": "venv/lib/python3.12/site-packages/wtforms/csrf/session.py",
  "start": {
    "line": 47,
    "col": 31,
    "offset": 1487
  },
  "end": {
    "line": 47,
    "col": 51,
    "offset": 1507
  },
  "extra": {
    "message": "Detected SHA1 hash algorithm which is considered insecure. SHA1 is not collision resistant and is therefore not suitable as a cryptographic signature. Use SHA256 or SHA3 instead.",
    "fix": "sha256(os.urandom(64))",
    "metadata": {
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/d5f8fa0d89d7b11442fc6ec80ca42953974354c8/bandit/blacklists/calls.py#L59",
      "cwe": [
        "CWE-327: Use of a Broken or Risky Cryptographic Algorithm"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "bandit-code": "B303",
      "asvs": {
        "control_id": "6.2.2 Insecure Custom Algorithm",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms",
        "section": "V6 Stored Cryptography Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://www.schneier.com/blog/archives/2012/10/when_will_we_se.html",
        "https://www.trendmicro.com/vinfo/us/security/news/vulnerabilities-and-exploits/sha-1-collision-signals-the-end-of-the-algorithm-s-viability",
        "http://2012.sharcs.org/slides/stevens.pdf",
        "https://pycryptodome.readthedocs.io/en/latest/src/hash/sha3_256.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "vuln"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1",
      "shortlink": "https://sg.run/ydYx"
    },
    "severity": "WARNING",
    "fingerprint": "requires login",
    "lines": "requires login",
    "validation_state": "NO_VALIDATOR",
    "engine_kind": "OSS"
  }
}
```

---
