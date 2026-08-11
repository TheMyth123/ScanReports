# Semgrep Report

Total findings: **256**

## Summary

| Severity | Count |
|----------|------:|
| ERROR | 52 |
| INFO | 7 |
| WARNING | 197 |

---

## Findings

1. [generic.secrets.security.detected-jwt-token.detected-jwt-token - .cache/pip/http-v2/8/0/6/3/6/806366e41f528c7b7fbd8d56ea0250ba9ebcf4270a1af519a9bb79da.body:76](#finding-1)
2. [generic.secrets.security.detected-jwt-token.detected-jwt-token - .cache/pip/http-v2/d/6/a/5/d/d6a5d0856a7e93554e8be85cae6a61e3c3d38bd36521d22d8c0dc50e.body:44](#finding-2)
3. [python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute - app.py:108](#finding-3)
4. [python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute - app.py:109](#finding-4)
5. [python.django.security.injection.tainted-sql-string.tainted-sql-string - app.py:112](#finding-5)
6. [python.flask.security.injection.tainted-sql-string.tainted-sql-string - app.py:112](#finding-6)
7. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - app.py:117](#finding-7)
8. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - app.py:117](#finding-8)
9. [python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute - app.py:173](#finding-9)
10. [python.django.security.injection.tainted-sql-string.tainted-sql-string - app.py:179](#finding-10)
11. [python.flask.security.injection.tainted-sql-string.tainted-sql-string - app.py:179](#finding-11)
12. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - app.py:442](#finding-12)
13. [python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host - app.py:447](#finding-13)
14. [python.flask.security.audit.debug-enabled.debug-enabled - app.py:447](#finding-14)
15. [generic.secrets.security.detected-jwt-token.detected-jwt-token - semgrep-report-auto.json:13](#finding-15)
16. [generic.secrets.security.detected-jwt-token.detected-jwt-token - semgrep-report-auto.json:22](#finding-16)
17. [generic.secrets.security.detected-jwt-token.detected-jwt-token - semgrep-report-auto.json:712](#finding-17)
18. [generic.secrets.security.detected-jwt-token.detected-jwt-token - semgrep-report-auto.json:1842](#finding-18)
19. [javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket - semgrep-report-auto.json:1957](#finding-19)
20. [javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket - semgrep-report-auto.json:2098](#finding-20)
21. [html.security.audit.missing-integrity.missing-integrity - templates/base.html:7](#finding-21)
22. [html.security.audit.missing-integrity.missing-integrity - templates/base.html:45](#finding-22)
23. [python.django.security.django-no-csrf-token.django-no-csrf-token - templates/donor_detail.html:26](#finding-23)
24. [python.django.security.django-no-csrf-token.django-no-csrf-token - templates/donor_detail.html:41](#finding-24)
25. [python.django.security.django-no-csrf-token.django-no-csrf-token - templates/donor_detail.html:52](#finding-25)
26. [python.django.security.django-no-csrf-token.django-no-csrf-token - templates/donor_register.html:8](#finding-26)
27. [python.django.security.django-no-csrf-token.django-no-csrf-token - templates/staff_login.html:8](#finding-27)
28. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/anyio/_core/_eventloop.py:206](#finding-28)
29. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/anyio/streams/tls.py:264](#finding-29)
30. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_interpreter.py:121](#finding-30)
31. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_interpreter.py:130](#finding-31)
32. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:95](#finding-32)
33. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:104](#finding-33)
34. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:168](#finding-34)
35. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:220](#finding-35)
36. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:251](#finding-36)
37. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:254](#finding-37)
38. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/anyio/to_process.py:258](#finding-38)
39. [python.lang.security.audit.eval-detected.eval-detected - venv/lib/python3.12/site-packages/attr/_make.py:227](#finding-39)
40. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/attr/_make.py:3140](#finding-40)
41. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/attr/_make.py:3393](#finding-41)
42. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/attr/_make.py:3402](#finding-42)
43. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/attr/converters.py:54](#finding-43)
44. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/attr/converters.py:58](#finding-44)
45. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/boltons/funcutils.py:1035](#finding-45)
46. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/boltons/namedutils.py:68](#finding-46)
47. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/certifi/core.py:16](#finding-47)
48. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/certifi/core.py:51](#finding-48)
49. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/cffi/_cffi_gen_src.py:53](#finding-49)
50. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/cffi/cffi_opcode.py:180](#finding-50)
51. [python.lang.security.audit.eval-detected.eval-detected - venv/lib/python3.12/site-packages/cffi/recompiler.py:80](#finding-51)
52. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/cffi/setuptools_ext.py:26](#finding-52)
53. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/charset_normalizer/cd.py:38](#finding-53)
54. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/charset_normalizer/utils.py:281](#finding-54)
55. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/charset_normalizer/utils.py:329](#finding-55)
56. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/charset_normalizer/utils.py:330](#finding-56)
57. [python.lang.compatibility.python36.python36-compatibility-Popen1 - venv/lib/python3.12/site-packages/click/_termui_impl.py:531](#finding-57)
58. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/click/parser.py:520](#finding-58)
59. [python.cryptography.security.insecure-hash-algorithms-md5.insecure-hash-algorithm-md5 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:133](#finding-59)
60. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:134](#finding-60)
61. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:135](#finding-61)
62. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:144](#finding-62)
63. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/_oid.py:153](#finding-63)
64. [python.cryptography.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/hazmat/primitives/serialization/ssh.py:1000](#finding-64)
65. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/cryptography/x509/extensions.py:72](#finding-65)
66. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/face/sinter.py:136](#finding-66)
67. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/face/sinter.py:142](#finding-67)
68. [python.lang.security.audit.eval-detected.eval-detected - venv/lib/python3.12/site-packages/flask/cli.py:1005](#finding-68)
69. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/flask/config.py:212](#finding-69)
70. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/flask/json/tag.py:188](#finding-70)
71. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/flask/sessions.py:285](#finding-71)
72. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/glom/cli.py:239](#finding-72)
73. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/google/protobuf/internal/api_implementation.py:43](#finding-73)
74. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/google/protobuf/proto_builder.py:68](#finding-74)
75. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/httpcore/__init__.py:141](#finding-75)
76. [python.flask.security.audit.directly-returned-format-string.directly-returned-format-string - venv/lib/python3.12/site-packages/httpcore/_async/connection_pool.py:386](#finding-76)
77. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py:84](#finding-77)
78. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py:86](#finding-78)
79. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py:88](#finding-79)
80. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py:90](#finding-80)
81. [python.django.security.audit.query-set-extra.avoid-query-set-extra - venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py:92](#finding-81)
82. [python.flask.security.audit.directly-returned-format-string.directly-returned-format-string - venv/lib/python3.12/site-packages/httpcore/_sync/connection_pool.py:386](#finding-82)
83. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/httpx/__init__.py:105](#finding-83)
84. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/httpx/_auth.py:309](#finding-84)
85. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/importlib_metadata/__init__.py:221](#finding-85)
86. [generic.secrets.security.detected-jwt-token.detected-jwt-token - venv/lib/python3.12/site-packages/itsdangerous-2.2.0.dist-info/METADATA:44](#finding-86)
87. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/itsdangerous/signer.py:45](#finding-87)
88. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/jinja2/bccache.py:41](#finding-88)
89. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/jinja2/bccache.py:42](#finding-89)
90. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/jinja2/bccache.py:73](#finding-90)
91. [python.lang.security.audit.marshal.marshal-usage - venv/lib/python3.12/site-packages/jinja2/bccache.py:79](#finding-91)
92. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/jinja2/bccache.py:89](#finding-92)
93. [python.lang.security.audit.marshal.marshal-usage - venv/lib/python3.12/site-packages/jinja2/bccache.py:90](#finding-93)
94. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/bccache.py:156](#finding-94)
95. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/bccache.py:165](#finding-95)
96. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/jinja2/debug.py:145](#finding-96)
97. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/jinja2/environment.py:1228](#finding-97)
98. [python.django.security.audit.xss.html-magic-method.html-magic-method - venv/lib/python3.12/site-packages/jinja2/environment.py:1543](#finding-98)
99. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/environment.py:1544](#finding-99)
100. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/ext.py:176](#finding-100)
101. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/ext.py:197](#finding-101)
102. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/ext.py:213](#finding-102)
103. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/ext.py:238](#finding-103)
104. [python.django.security.audit.xss.html-magic-method.html-magic-method - venv/lib/python3.12/site-packages/jinja2/filters.py:40](#finding-104)
105. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/filters.py:316](#finding-105)
106. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/filters.py:820](#finding-106)
107. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/filters.py:851](#finding-107)
108. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/filters.py:1056](#finding-108)
109. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/filters.py:1377](#finding-109)
110. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/jinja2/loaders.py:323](#finding-110)
111. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/jinja2/loaders.py:661](#finding-111)
112. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/nodes.py:619](#finding-112)
113. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/nodes.py:1091](#finding-113)
114. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/nodes.py:1112](#finding-114)
115. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/runtime.py:375](#finding-115)
116. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/runtime.py:389](#finding-116)
117. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/runtime.py:776](#finding-117)
118. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/runtime.py:787](#finding-118)
119. [python.django.security.audit.xss.html-magic-method.html-magic-method - venv/lib/python3.12/site-packages/jinja2/runtime.py:988](#finding-119)
120. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/utils.py:403](#finding-120)
121. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/jinja2/utils.py:668](#finding-121)
122. [python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected - venv/lib/python3.12/site-packages/jsonschema/validators.py:113](#finding-122)
123. [python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected - venv/lib/python3.12/site-packages/jsonschema/validators.py:1228](#finding-123)
124. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/jsonschema_specifications/_core.py:8](#finding-124)
125. [python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected - venv/lib/python3.12/site-packages/jwt/jwks_client.py:118](#finding-125)
126. [python.django.security.audit.xss.html-magic-method.html-magic-method - venv/lib/python3.12/site-packages/markupsafe/__init__.py:17](#finding-126)
127. [python.django.security.audit.xss.html-magic-method.html-magic-method - venv/lib/python3.12/site-packages/markupsafe/__init__.py:133](#finding-127)
128. [python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup - venv/lib/python3.12/site-packages/markupsafe/__init__.py:228](#finding-128)
129. [python.lang.security.audit.subprocess-shell-true.subprocess-shell-true - venv/lib/python3.12/site-packages/mcp/cli/cli.py:48](#finding-129)
130. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/mcp/cli/cli.py:186](#finding-130)
131. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/opentelemetry/instrumentation/utils.py:102](#finding-131)
132. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/peewee.py:3632](#finding-132)
133. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/peewee.py:3632](#finding-133)
134. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/peewee.py:3638](#finding-134)
135. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/peewee.py:3638](#finding-135)
136. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/peewee.py:4279](#finding-136)
137. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/peewee.py:4279](#finding-137)
138. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_internal/cache.py:30](#finding-138)
139. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pip/_internal/commands/__init__.py:121](#finding-139)
140. [python.lang.security.audit.subprocess-shell-true.subprocess-shell-true - venv/lib/python3.12/site-packages/pip/_internal/commands/configuration.py:247](#finding-140)
141. [python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc - venv/lib/python3.12/site-packages/pip/_internal/commands/search.py:7](#finding-141)
142. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:89](#finding-142)
143. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:96](#finding-143)
144. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:356](#finding-144)
145. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:372](#finding-145)
146. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:379](#finding-146)
147. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:392](#finding-147)
148. [python.lang.security.audit.logging.logger-credential-leak.python-logger-credential-disclosure - venv/lib/python3.12/site-packages/pip/_internal/network/auth.py:550](#finding-148)
149. [python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc - venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py:5](#finding-149)
150. [python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc - venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py:13](#finding-150)
151. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_internal/self_outdated_check.py:49](#finding-151)
152. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/pip/_internal/utils/compat.py:4](#finding-152)
153. [python.lang.compatibility.python36.python36-compatibility-Popen1 - venv/lib/python3.12/site-packages/pip/_internal/utils/subprocess.py:129](#finding-153)
154. [trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal - venv/lib/python3.12/site-packages/pip/_internal/utils/unpacking.py:180](#finding-154)
155. [python.lang.security.audit.insecure-transport.requests.request-session-with-http.request-session-with-http - venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/_cmd.py:33](#finding-155)
156. [python.lang.security.audit.sha224-hash.sha224-hash - venv/lib/python3.12/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py:56](#finding-156)
157. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py:16](#finding-157)
158. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py:51](#finding-158)
159. [python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc - venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py:42](#finding-159)
160. [python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc - venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py:81](#finding-160)
161. [python.lang.security.audit.httpsconnection-detected.httpsconnection-detected - venv/lib/python3.12/site-packages/pip/_vendor/distlib/util.py:1572](#finding-161)
162. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:168](#finding-162)
163. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:168](#finding-163)
164. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:175](#finding-164)
165. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:175](#finding-165)
166. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:1714](#finding-166)
167. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:1725](#finding-167)
168. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py:2468](#finding-168)
169. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pip/_vendor/pygments/formatters/__init__.py:103](#finding-169)
170. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pip/_vendor/pygments/lexers/__init__.py:154](#finding-170)
171. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py:83](#finding-171)
172. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py:90](#finding-172)
173. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py:7](#finding-173)
174. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py:70](#finding-174)
175. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py:367](#finding-175)
176. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py:156](#finding-176)
177. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/pip/_vendor/requests/auth.py:205](#finding-177)
178. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py:196](#finding-178)
179. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py:247](#finding-179)
180. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py:471](#finding-180)
181. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py:747](#finding-181)
182. [python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers - venv/lib/python3.12/site-packages/pip/_vendor/truststore/_api.py:186](#finding-182)
183. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/emscripten/fetch.py:42](#finding-183)
184. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py:73](#finding-184)
185. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py:77](#finding-185)
186. [python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers - venv/lib/python3.12/site-packages/pip/_vendor/urllib3/util/ssl_.py:311](#finding-186)
187. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/playhouse/apsw_ext.py:112](#finding-187)
188. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/playhouse/apsw_ext.py:112](#finding-188)
189. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/playhouse/cockroachdb.py:153](#finding-189)
190. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/playhouse/cockroachdb.py:153](#finding-190)
191. [python.lang.security.deserialization.pickle.avoid-cPickle - venv/lib/python3.12/site-packages/playhouse/fields.py:55](#finding-191)
192. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/playhouse/fields.py:55](#finding-192)
193. [python.lang.security.deserialization.pickle.avoid-cPickle - venv/lib/python3.12/site-packages/playhouse/fields.py:59](#finding-193)
194. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/playhouse/fields.py:59](#finding-194)
195. [python.lang.security.insecure-uuid-version.insecure-uuid-version - venv/lib/python3.12/site-packages/playhouse/postgres_ext.py:492](#finding-195)
196. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/playhouse/reflection.py:388](#finding-196)
197. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/playhouse/reflection.py:388](#finding-197)
198. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py:77](#finding-198)
199. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py:77](#finding-199)
200. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/_json.py:187](#finding-200)
201. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:553](#finding-201)
202. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:553](#finding-202)
203. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:559](#finding-203)
204. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:559](#finding-204)
205. [python.lang.security.audit.formatted-sql-query.formatted-sql-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:907](#finding-205)
206. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:907](#finding-206)
207. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:1086](#finding-207)
208. [python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query - venv/lib/python3.12/site-packages/psycopg2/extras.py:1111](#finding-208)
209. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pydantic/__init__.py:442](#finding-209)
210. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pydantic/__init__.py:446](#finding-210)
211. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pydantic/_internal/_validators.py:110](#finding-211)
212. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pydantic/deprecated/parse.py:54](#finding-212)
213. [python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage - venv/lib/python3.12/site-packages/pydantic/v1/generics.py:400](#finding-213)
214. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/pydantic/v1/parse.py:42](#finding-214)
215. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pydantic/v1/utils.py:134](#finding-215)
216. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/pydantic/v1/version.py:25](#finding-216)
217. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pygments/formatters/__init__.py:103](#finding-217)
218. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/pygments/lexers/__init__.py:154](#finding-218)
219. [python.lang.security.audit.insecure-transport.urllib.insecure-urlopen.insecure-urlopen - venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py:225](#finding-219)
220. [python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected - venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py:233](#finding-220)
221. [trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal - venv/lib/python3.12/site-packages/pygments/lexers/_php_builtins.py:3300](#finding-221)
222. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pygments/unistring.py:83](#finding-222)
223. [python.lang.security.dangerous-globals-use.dangerous-globals-use - venv/lib/python3.12/site-packages/pygments/unistring.py:90](#finding-223)
224. [generic.secrets.security.detected-jwt-token.detected-jwt-token - venv/lib/python3.12/site-packages/pyjwt-2.13.0.dist-info/METADATA:76](#finding-224)
225. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/requests/auth.py:156](#finding-225)
226. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/requests/auth.py:205](#finding-226)
227. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/requests/compat.py:24](#finding-227)
228. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/rich/_unicode_data/__init__.py:90](#finding-228)
229. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/rich/style.py:200](#finding-229)
230. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/rich/style.py:251](#finding-230)
231. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/rich/style.py:475](#finding-231)
232. [python.lang.security.deserialization.pickle.avoid-pickle - venv/lib/python3.12/site-packages/rich/style.py:751](#finding-232)
233. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/ruamel/yaml/main.py:87](#finding-233)
234. [python.lang.security.audit.insecure-file-permissions.insecure-file-permissions - venv/lib/python3.12/site-packages/semgrep/commands/install.py:216](#finding-234)
235. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/semgrep/console_scripts/entrypoint.py:30](#finding-235)
236. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/semgrep/semgrep_core.py:13](#finding-236)
237. [python.flask.security.xss.audit.direct-use-of-jinja2.direct-use-of-jinja2 - venv/lib/python3.12/site-packages/starlette/templating.py:95](#finding-237)
238. [javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket - venv/lib/python3.12/site-packages/starlette/testclient.py:661](#finding-238)
239. [python.lang.security.audit.eval-detected.eval-detected - venv/lib/python3.12/site-packages/typing_extensions.py:4172](#finding-239)
240. [python.lang.security.audit.eval-detected.eval-detected - venv/lib/python3.12/site-packages/typing_extensions.py:4254](#finding-240)
241. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py:101](#finding-241)
242. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py:133](#finding-242)
243. [python.lang.compatibility.python37.python37-compatibility-importlib2 - venv/lib/python3.12/site-packages/urllib3/contrib/emscripten/fetch.py:42](#finding-243)
244. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py:73](#finding-244)
245. [python.lang.security.audit.weak-ssl-version.weak-ssl-version - venv/lib/python3.12/site-packages/urllib3/contrib/pyopenssl.py:77](#finding-245)
246. [python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers - venv/lib/python3.12/site-packages/urllib3/util/ssl_.py:311](#finding-246)
247. [python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers - venv/lib/python3.12/site-packages/uvicorn/config.py:134](#finding-247)
248. [python.lang.security.audit.insecure-file-permissions.insecure-file-permissions - venv/lib/python3.12/site-packages/uvicorn/config.py:559](#finding-248)
249. [python.lang.security.audit.non-literal-import.non-literal-import - venv/lib/python3.12/site-packages/uvicorn/importer.py:19](#finding-249)
250. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py:44](#finding-250)
251. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/debug/__init__.py:194](#finding-251)
252. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/werkzeug/debug/console.py:177](#finding-252)
253. [python.lang.security.insecure-hash-algorithms.insecure-hash-algorithm-sha1 - venv/lib/python3.12/site-packages/werkzeug/http.py:956](#finding-253)
254. [python.lang.security.audit.httpsconnection-detected.httpsconnection-detected - venv/lib/python3.12/site-packages/werkzeug/middleware/http_proxy.py:151](#finding-254)
255. [javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket - venv/lib/python3.12/site-packages/werkzeug/routing/rules.py:427](#finding-255)
256. [python.lang.security.audit.exec-detected.exec-detected - venv/lib/python3.12/site-packages/werkzeug/routing/rules.py:727](#finding-256)

---

# Finding 1
<a name='finding-1'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `.cache/pip/http-v2/8/0/6/3/6/806366e41f528c7b7fbd8d56ea0250ba9ebcf4270a1af519a9bb79da.body`
- Start: Line 76, Column 5
- End: Line 76, Column 67

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": ".cache/pip/http-v2/8/0/6/3/6/806366e41f528c7b7fbd8d56ea0250ba9ebcf4270a1af519a9bb79da.body",
  "start": {
    "line": 76,
    "col": 5,
    "offset": 3049
  },
  "end": {
    "line": 76,
    "col": 67,
    "offset": 3111
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 2
<a name='finding-2'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `.cache/pip/http-v2/d/6/a/5/d/d6a5d0856a7e93554e8be85cae6a61e3c3d38bd36521d22d8c0dc50e.body`
- Start: Line 44, Column 3
- End: Line 44, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": ".cache/pip/http-v2/d/6/a/5/d/d6a5d0856a7e93554e8be85cae6a61e3c3d38bd36521d22d8c0dc50e.body",
  "start": {
    "line": 44,
    "col": 3,
    "offset": 1481
  },
  "end": {
    "line": 44,
    "col": 71,
    "offset": 1549
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 3
<a name='finding-3'></a>

**Rule ID:** `python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute`

**Severity:** WARNING

**Message:** User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.

## Location

- File: `app.py`
- Start: Line 108, Column 9
- End: Line 124, Column 25

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** MEDIUM
- **impact:** HIGH
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute
- **shortlink:** https://sg.run/qx7y

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
  "path": "app.py",
  "start": {
    "line": 108,
    "col": 9,
    "offset": 3192
  },
  "end": {
    "line": 124,
    "col": 25,
    "offset": 3877
  },
  "extra": {
    "message": "User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "MEDIUM",
      "impact": "HIGH",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
      "shortlink": "https://sg.run/qx7y"
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

# Finding 4
<a name='finding-4'></a>

**Rule ID:** `python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute`

**Severity:** WARNING

**Message:** User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.

## Location

- File: `app.py`
- Start: Line 109, Column 9
- End: Line 124, Column 25

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** MEDIUM
- **impact:** HIGH
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute
- **shortlink:** https://sg.run/qx7y

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
  "path": "app.py",
  "start": {
    "line": 109,
    "col": 9,
    "offset": 3244
  },
  "end": {
    "line": 124,
    "col": 25,
    "offset": 3877
  },
  "extra": {
    "message": "User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "MEDIUM",
      "impact": "HIGH",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
      "shortlink": "https://sg.run/qx7y"
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

**Rule ID:** `python.django.security.injection.tainted-sql-string.tainted-sql-string`

**Severity:** ERROR

**Message:** Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using the Django object-relational mappers (ORM) instead of raw SQL queries.

## Location

- File: `app.py`
- Start: Line 112, Column 17
- End: Line 112, Column 133

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-915: Improperly Controlled Modification of Dynamically-Determined Object Attributes
- **owasp**
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **references**
  - https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection
- **category:** security
- **technology**
  - django
- **subcategory**
  - audit
- **impact:** LOW
- **likelihood:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mass Assignment
- **source:** https://semgrep.dev/r/python.django.security.injection.tainted-sql-string.tainted-sql-string
- **shortlink:** https://sg.run/PbZp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.injection.tainted-sql-string.tainted-sql-string",
  "path": "app.py",
  "start": {
    "line": 112,
    "col": 17,
    "offset": 3381
  },
  "end": {
    "line": 112,
    "col": 133,
    "offset": 3497
  },
  "extra": {
    "message": "Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using the Django object-relational mappers (ORM) instead of raw SQL queries.",
    "metadata": {
      "cwe": [
        "CWE-915: Improperly Controlled Modification of Dynamically-Determined Object Attributes"
      ],
      "owasp": [
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "subcategory": [
        "audit"
      ],
      "impact": "LOW",
      "likelihood": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mass Assignment"
      ],
      "source": "https://semgrep.dev/r/python.django.security.injection.tainted-sql-string.tainted-sql-string",
      "shortlink": "https://sg.run/PbZp"
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

# Finding 6
<a name='finding-6'></a>

**Rule ID:** `python.flask.security.injection.tainted-sql-string.tainted-sql-string`

**Severity:** ERROR

**Message:** Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using an object-relational mapper (ORM) such as SQLAlchemy which will protect your queries.

## Location

- File: `app.py`
- Start: Line 112, Column 17
- End: Line 112, Column 133

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-704: Incorrect Type Conversion or Cast
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
  - flask
- **subcategory**
  - vuln
- **impact:** MEDIUM
- **likelihood:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Validation
- **source:** https://semgrep.dev/r/python.flask.security.injection.tainted-sql-string.tainted-sql-string
- **shortlink:** https://sg.run/JxZj

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.injection.tainted-sql-string.tainted-sql-string",
  "path": "app.py",
  "start": {
    "line": 112,
    "col": 17,
    "offset": 3381
  },
  "end": {
    "line": 112,
    "col": 133,
    "offset": 3497
  },
  "extra": {
    "message": "Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using an object-relational mapper (ORM) such as SQLAlchemy which will protect your queries.",
    "metadata": {
      "cwe": [
        "CWE-704: Incorrect Type Conversion or Cast"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy",
        "flask"
      ],
      "subcategory": [
        "vuln"
      ],
      "impact": "MEDIUM",
      "likelihood": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Validation"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.injection.tainted-sql-string.tainted-sql-string",
      "shortlink": "https://sg.run/JxZj"
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

# Finding 7
<a name='finding-7'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `app.py`
- Start: Line 117, Column 13
- End: Line 117, Column 31

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "app.py",
  "start": {
    "line": 117,
    "col": 13,
    "offset": 3578
  },
  "end": {
    "line": 117,
    "col": 31,
    "offset": 3596
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `app.py`
- Start: Line 117, Column 13
- End: Line 117, Column 31

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "app.py",
  "start": {
    "line": 117,
    "col": 13,
    "offset": 3578
  },
  "end": {
    "line": 117,
    "col": 31,
    "offset": 3596
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 9
<a name='finding-9'></a>

**Rule ID:** `python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute`

**Severity:** WARNING

**Message:** User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.

## Location

- File: `app.py`
- Start: Line 173, Column 5
- End: Line 190, Column 21

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - vuln
- **likelihood:** MEDIUM
- **impact:** HIGH
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute
- **shortlink:** https://sg.run/qx7y

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
  "path": "app.py",
  "start": {
    "line": 173,
    "col": 5,
    "offset": 5237
  },
  "end": {
    "line": 190,
    "col": 21,
    "offset": 5822
  },
  "extra": {
    "message": "User-controlled data from a request is passed to 'execute()'. This could lead to a SQL injection and therefore protected information could be leaked. Instead, use django's QuerySets, which are built with query parameterization and therefore not vulnerable to sql injection. For example, you could use `Entry.objects.filter(date=2006)`.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "vuln"
      ],
      "likelihood": "MEDIUM",
      "impact": "HIGH",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.injection.sql.sql-injection-using-db-cursor-execute.sql-injection-db-cursor-execute",
      "shortlink": "https://sg.run/qx7y"
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

**Rule ID:** `python.django.security.injection.tainted-sql-string.tainted-sql-string`

**Severity:** ERROR

**Message:** Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using the Django object-relational mappers (ORM) instead of raw SQL queries.

## Location

- File: `app.py`
- Start: Line 179, Column 17
- End: Line 179, Column 126

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-915: Improperly Controlled Modification of Dynamically-Determined Object Attributes
- **owasp**
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **references**
  - https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection
- **category:** security
- **technology**
  - django
- **subcategory**
  - audit
- **impact:** LOW
- **likelihood:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mass Assignment
- **source:** https://semgrep.dev/r/python.django.security.injection.tainted-sql-string.tainted-sql-string
- **shortlink:** https://sg.run/PbZp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.injection.tainted-sql-string.tainted-sql-string",
  "path": "app.py",
  "start": {
    "line": 179,
    "col": 17,
    "offset": 5420
  },
  "end": {
    "line": 179,
    "col": 126,
    "offset": 5529
  },
  "extra": {
    "message": "Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using the Django object-relational mappers (ORM) instead of raw SQL queries.",
    "metadata": {
      "cwe": [
        "CWE-915: Improperly Controlled Modification of Dynamically-Determined Object Attributes"
      ],
      "owasp": [
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/topics/security/#sql-injection-protection"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "subcategory": [
        "audit"
      ],
      "impact": "LOW",
      "likelihood": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mass Assignment"
      ],
      "source": "https://semgrep.dev/r/python.django.security.injection.tainted-sql-string.tainted-sql-string",
      "shortlink": "https://sg.run/PbZp"
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

# Finding 11
<a name='finding-11'></a>

**Rule ID:** `python.flask.security.injection.tainted-sql-string.tainted-sql-string`

**Severity:** ERROR

**Message:** Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using an object-relational mapper (ORM) such as SQLAlchemy which will protect your queries.

## Location

- File: `app.py`
- Start: Line 179, Column 17
- End: Line 179, Column 126

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-704: Incorrect Type Conversion or Cast
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
  - flask
- **subcategory**
  - vuln
- **impact:** MEDIUM
- **likelihood:** MEDIUM
- **confidence:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Validation
- **source:** https://semgrep.dev/r/python.flask.security.injection.tainted-sql-string.tainted-sql-string
- **shortlink:** https://sg.run/JxZj

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.injection.tainted-sql-string.tainted-sql-string",
  "path": "app.py",
  "start": {
    "line": 179,
    "col": 17,
    "offset": 5420
  },
  "end": {
    "line": 179,
    "col": 126,
    "offset": 5529
  },
  "extra": {
    "message": "Detected user input used to manually construct a SQL string. This is usually bad practice because manual construction could accidentally result in a SQL injection. An attacker could use a SQL injection to steal or modify contents of the database. Instead, use a parameterized query which is available by default in most database engines. Alternatively, consider using an object-relational mapper (ORM) such as SQLAlchemy which will protect your queries.",
    "metadata": {
      "cwe": [
        "CWE-704: Incorrect Type Conversion or Cast"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy",
        "flask"
      ],
      "subcategory": [
        "vuln"
      ],
      "impact": "MEDIUM",
      "likelihood": "MEDIUM",
      "confidence": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Validation"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.injection.tainted-sql-string.tainted-sql-string",
      "shortlink": "https://sg.run/JxZj"
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

# Finding 12
<a name='finding-12'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `app.py`
- Start: Line 442, Column 12
- End: Line 442, Column 31

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "app.py",
  "start": {
    "line": 442,
    "col": 12,
    "offset": 15058
  },
  "end": {
    "line": 442,
    "col": 31,
    "offset": 15077
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

**Rule ID:** `python.flask.security.audit.app-run-param-config.avoid_app_run_with_bad_host`

**Severity:** WARNING

**Message:** Running flask app with host 0.0.0.0 could expose the server publicly.

## Location

- File: `app.py`
- Start: Line 447, Column 5
- End: Line 447, Column 51

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
    "line": 447,
    "col": 5,
    "offset": 15171
  },
  "end": {
    "line": 447,
    "col": 51,
    "offset": 15217
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

# Finding 14
<a name='finding-14'></a>

**Rule ID:** `python.flask.security.audit.debug-enabled.debug-enabled`

**Severity:** WARNING

**Message:** Detected Flask app with debug=True. Do not deploy to production with this flag enabled as it will leak sensitive information. Instead, consider using Flask configuration variables or setting 'debug' using system environment variables.

## Location

- File: `app.py`
- Start: Line 447, Column 5
- End: Line 447, Column 51

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
    "line": 447,
    "col": 5,
    "offset": 15171
  },
  "end": {
    "line": 447,
    "col": 51,
    "offset": 15217
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

# Finding 15
<a name='finding-15'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `semgrep-report-auto.json`
- Start: Line 13, Column 18
- End: Line 13, Column 80

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 13,
    "col": 18,
    "offset": 691
  },
  "end": {
    "line": 13,
    "col": 80,
    "offset": 753
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 16
<a name='finding-16'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `semgrep-report-auto.json`
- Start: Line 22, Column 20
- End: Line 22, Column 88

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 22,
    "col": 20,
    "offset": 1385
  },
  "end": {
    "line": 22,
    "col": 88,
    "offset": 1453
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 17
<a name='finding-17'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `semgrep-report-auto.json`
- Start: Line 712, Column 20
- End: Line 712, Column 88

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 712,
    "col": 20,
    "offset": 58811
  },
  "end": {
    "line": 712,
    "col": 88,
    "offset": 58879
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 18
<a name='finding-18'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `semgrep-report-auto.json`
- Start: Line 1842, Column 18
- End: Line 1842, Column 80

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 1842,
    "col": 18,
    "offset": 152707
  },
  "end": {
    "line": 1842,
    "col": 80,
    "offset": 152769
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 19
<a name='finding-19'></a>

**Rule ID:** `javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket`

**Severity:** ERROR

**Message:** Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.

## Location

- File: `semgrep-report-auto.json`
- Start: Line 1957, Column 33
- End: Line 1957, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **asvs**
  - control_id: 13.5.1 Insecure WebSocket
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements
  - section: V13: API and Web Service Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - regex
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket
- **shortlink:** https://sg.run/GWyz

## Raw Finding JSON

```json
{
  "check_id": "javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 1957,
    "col": 33,
    "offset": 162541
  },
  "end": {
    "line": 1957,
    "col": 38,
    "offset": 162546
  },
  "extra": {
    "message": "Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.",
    "metadata": {
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "asvs": {
        "control_id": "13.5.1 Insecure WebSocket",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements",
        "section": "V13: API and Web Service Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "regex"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
      "shortlink": "https://sg.run/GWyz"
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

# Finding 20
<a name='finding-20'></a>

**Rule ID:** `javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket`

**Severity:** ERROR

**Message:** Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.

## Location

- File: `semgrep-report-auto.json`
- Start: Line 2098, Column 74
- End: Line 2098, Column 79

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **asvs**
  - control_id: 13.5.1 Insecure WebSocket
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements
  - section: V13: API and Web Service Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - regex
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket
- **shortlink:** https://sg.run/GWyz

## Raw Finding JSON

```json
{
  "check_id": "javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
  "path": "semgrep-report-auto.json",
  "start": {
    "line": 2098,
    "col": 74,
    "offset": 174577
  },
  "end": {
    "line": 2098,
    "col": 79,
    "offset": 174582
  },
  "extra": {
    "message": "Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.",
    "metadata": {
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "asvs": {
        "control_id": "13.5.1 Insecure WebSocket",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements",
        "section": "V13: API and Web Service Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "regex"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
      "shortlink": "https://sg.run/GWyz"
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

# Finding 21
<a name='finding-21'></a>

**Rule ID:** `html.security.audit.missing-integrity.missing-integrity`

**Severity:** WARNING

**Message:** This tag is missing an 'integrity' subresource integrity attribute. The 'integrity' attribute allows for the browser to verify that externally hosted files (for example from a CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker can modify the externally hosted resource, this could lead to XSS and other types of attacks. To prevent this, include the base64-encoded cryptographic hash of the resource (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally hosted files.

## Location

- File: `templates/base.html`
- Start: Line 7, Column 3
- End: Line 7, Column 105

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **technology**
  - html
- **cwe**
  - CWE-353: Missing Support for Integrity Check
- **owasp**
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/html.security.audit.missing-integrity.missing-integrity
- **shortlink:** https://sg.run/krXA

## Raw Finding JSON

```json
{
  "check_id": "html.security.audit.missing-integrity.missing-integrity",
  "path": "templates/base.html",
  "start": {
    "line": 7,
    "col": 3,
    "offset": 194
  },
  "end": {
    "line": 7,
    "col": 105,
    "offset": 296
  },
  "extra": {
    "message": "This tag is missing an 'integrity' subresource integrity attribute. The 'integrity' attribute allows for the browser to verify that externally hosted files (for example from a CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker can modify the externally hosted resource, this could lead to XSS and other types of attacks. To prevent this, include the base64-encoded cryptographic hash of the resource (file) you\u2019re telling the browser to fetch in the 'integrity' attribute for all externally hosted files.",
    "metadata": {
      "category": "security",
      "technology": [
        "html"
      ],
      "cwe": [
        "CWE-353: Missing Support for Integrity Check"
      ],
      "owasp": [
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/html.security.audit.missing-integrity.missing-integrity",
      "shortlink": "https://sg.run/krXA"
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

**Rule ID:** `html.security.audit.missing-integrity.missing-integrity`

**Severity:** WARNING

**Message:** This tag is missing an 'integrity' subresource integrity attribute. The 'integrity' attribute allows for the browser to verify that externally hosted files (for example from a CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker can modify the externally hosted resource, this could lead to XSS and other types of attacks. To prevent this, include the base64-encoded cryptographic hash of the resource (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally hosted files.

## Location

- File: `templates/base.html`
- Start: Line 45, Column 1
- End: Line 45, Column 101

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **technology**
  - html
- **cwe**
  - CWE-353: Missing Support for Integrity Check
- **owasp**
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/html.security.audit.missing-integrity.missing-integrity
- **shortlink:** https://sg.run/krXA

## Raw Finding JSON

```json
{
  "check_id": "html.security.audit.missing-integrity.missing-integrity",
  "path": "templates/base.html",
  "start": {
    "line": 45,
    "col": 1,
    "offset": 2192
  },
  "end": {
    "line": 45,
    "col": 101,
    "offset": 2292
  },
  "extra": {
    "message": "This tag is missing an 'integrity' subresource integrity attribute. The 'integrity' attribute allows for the browser to verify that externally hosted files (for example from a CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker can modify the externally hosted resource, this could lead to XSS and other types of attacks. To prevent this, include the base64-encoded cryptographic hash of the resource (file) you\u2019re telling the browser to fetch in the 'integrity' attribute for all externally hosted files.",
    "metadata": {
      "category": "security",
      "technology": [
        "html"
      ],
      "cwe": [
        "CWE-353: Missing Support for Integrity Check"
      ],
      "owasp": [
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/html.security.audit.missing-integrity.missing-integrity",
      "shortlink": "https://sg.run/krXA"
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

**Rule ID:** `python.django.security.django-no-csrf-token.django-no-csrf-token`

**Severity:** WARNING

**Message:** Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.

## Location

- File: `templates/donor_detail.html`
- Start: Line 26, Column 7
- End: Line 36, Column 14

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-352: Cross-Site Request Forgery (CSRF)
- **references**
  - https://docs.djangoproject.com/en/4.2/howto/csrf/
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **subcategory**
  - audit
- **technology**
  - django
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site Request Forgery (CSRF)
- **source:** https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token
- **shortlink:** https://sg.run/N0Bp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.django-no-csrf-token.django-no-csrf-token",
  "path": "templates/donor_detail.html",
  "start": {
    "line": 26,
    "col": 7,
    "offset": 1098
  },
  "end": {
    "line": 36,
    "col": 14,
    "offset": 2416
  },
  "extra": {
    "message": "Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.",
    "metadata": {
      "category": "security",
      "cwe": "CWE-352: Cross-Site Request Forgery (CSRF)",
      "references": [
        "https://docs.djangoproject.com/en/4.2/howto/csrf/"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "subcategory": [
        "audit"
      ],
      "technology": [
        "django"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site Request Forgery (CSRF)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token",
      "shortlink": "https://sg.run/N0Bp"
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

**Rule ID:** `python.django.security.django-no-csrf-token.django-no-csrf-token`

**Severity:** WARNING

**Message:** Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.

## Location

- File: `templates/donor_detail.html`
- Start: Line 41, Column 7
- End: Line 47, Column 14

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-352: Cross-Site Request Forgery (CSRF)
- **references**
  - https://docs.djangoproject.com/en/4.2/howto/csrf/
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **subcategory**
  - audit
- **technology**
  - django
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site Request Forgery (CSRF)
- **source:** https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token
- **shortlink:** https://sg.run/N0Bp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.django-no-csrf-token.django-no-csrf-token",
  "path": "templates/donor_detail.html",
  "start": {
    "line": 41,
    "col": 7,
    "offset": 2549
  },
  "end": {
    "line": 47,
    "col": 14,
    "offset": 3161
  },
  "extra": {
    "message": "Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.",
    "metadata": {
      "category": "security",
      "cwe": "CWE-352: Cross-Site Request Forgery (CSRF)",
      "references": [
        "https://docs.djangoproject.com/en/4.2/howto/csrf/"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "subcategory": [
        "audit"
      ],
      "technology": [
        "django"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site Request Forgery (CSRF)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token",
      "shortlink": "https://sg.run/N0Bp"
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

# Finding 25
<a name='finding-25'></a>

**Rule ID:** `python.django.security.django-no-csrf-token.django-no-csrf-token`

**Severity:** WARNING

**Message:** Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.

## Location

- File: `templates/donor_detail.html`
- Start: Line 52, Column 7
- End: Line 60, Column 14

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-352: Cross-Site Request Forgery (CSRF)
- **references**
  - https://docs.djangoproject.com/en/4.2/howto/csrf/
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **subcategory**
  - audit
- **technology**
  - django
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site Request Forgery (CSRF)
- **source:** https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token
- **shortlink:** https://sg.run/N0Bp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.django-no-csrf-token.django-no-csrf-token",
  "path": "templates/donor_detail.html",
  "start": {
    "line": 52,
    "col": 7,
    "offset": 3310
  },
  "end": {
    "line": 60,
    "col": 14,
    "offset": 4358
  },
  "extra": {
    "message": "Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.",
    "metadata": {
      "category": "security",
      "cwe": "CWE-352: Cross-Site Request Forgery (CSRF)",
      "references": [
        "https://docs.djangoproject.com/en/4.2/howto/csrf/"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "subcategory": [
        "audit"
      ],
      "technology": [
        "django"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site Request Forgery (CSRF)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token",
      "shortlink": "https://sg.run/N0Bp"
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

# Finding 26
<a name='finding-26'></a>

**Rule ID:** `python.django.security.django-no-csrf-token.django-no-csrf-token`

**Severity:** WARNING

**Message:** Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.

## Location

- File: `templates/donor_register.html`
- Start: Line 8, Column 9
- End: Line 19, Column 16

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-352: Cross-Site Request Forgery (CSRF)
- **references**
  - https://docs.djangoproject.com/en/4.2/howto/csrf/
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **subcategory**
  - audit
- **technology**
  - django
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site Request Forgery (CSRF)
- **source:** https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token
- **shortlink:** https://sg.run/N0Bp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.django-no-csrf-token.django-no-csrf-token",
  "path": "templates/donor_register.html",
  "start": {
    "line": 8,
    "col": 9,
    "offset": 279
  },
  "end": {
    "line": 19,
    "col": 16,
    "offset": 1443
  },
  "extra": {
    "message": "Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.",
    "metadata": {
      "category": "security",
      "cwe": "CWE-352: Cross-Site Request Forgery (CSRF)",
      "references": [
        "https://docs.djangoproject.com/en/4.2/howto/csrf/"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "subcategory": [
        "audit"
      ],
      "technology": [
        "django"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site Request Forgery (CSRF)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token",
      "shortlink": "https://sg.run/N0Bp"
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

**Rule ID:** `python.django.security.django-no-csrf-token.django-no-csrf-token`

**Severity:** WARNING

**Message:** Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.

## Location

- File: `templates/staff_login.html`
- Start: Line 8, Column 9
- End: Line 12, Column 16

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-352: Cross-Site Request Forgery (CSRF)
- **references**
  - https://docs.djangoproject.com/en/4.2/howto/csrf/
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **subcategory**
  - audit
- **technology**
  - django
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site Request Forgery (CSRF)
- **source:** https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token
- **shortlink:** https://sg.run/N0Bp

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.django-no-csrf-token.django-no-csrf-token",
  "path": "templates/staff_login.html",
  "start": {
    "line": 8,
    "col": 9,
    "offset": 280
  },
  "end": {
    "line": 12,
    "col": 16,
    "offset": 654
  },
  "extra": {
    "message": "Manually-created forms in django templates should specify a csrf_token to prevent CSRF attacks.",
    "metadata": {
      "category": "security",
      "cwe": "CWE-352: Cross-Site Request Forgery (CSRF)",
      "references": [
        "https://docs.djangoproject.com/en/4.2/howto/csrf/"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "subcategory": [
        "audit"
      ],
      "technology": [
        "django"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site Request Forgery (CSRF)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.django-no-csrf-token.django-no-csrf-token",
      "shortlink": "https://sg.run/N0Bp"
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

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/_core/_eventloop.py`
- Start: Line 206, Column 18
- End: Line 206, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/anyio/_core/_eventloop.py",
  "start": {
    "line": 206,
    "col": 18,
    "offset": 5670
  },
  "end": {
    "line": 206,
    "col": 68,
    "offset": 5720
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 29
<a name='finding-29'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/streams/tls.py`
- Start: Line 264, Column 23
- End: Line 264, Column 59

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/anyio/streams/tls.py",
  "start": {
    "line": 264,
    "col": 23,
    "offset": 9156
  },
  "end": {
    "line": 264,
    "col": 59,
    "offset": 9192
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_interpreter.py`
- Start: Line 121, Column 20
- End: Line 121, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_interpreter.py",
  "start": {
    "line": 121,
    "col": 20,
    "offset": 3261
  },
  "end": {
    "line": 121,
    "col": 71,
    "offset": 3312
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_interpreter.py`
- Start: Line 130, Column 23
- End: Line 130, Column 40

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_interpreter.py",
  "start": {
    "line": 130,
    "col": 23,
    "offset": 3698
  },
  "end": {
    "line": 130,
    "col": 40,
    "offset": 3715
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 95, Column 18
- End: Line 95, Column 48

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 95,
    "col": 18,
    "offset": 3275
  },
  "end": {
    "line": 95,
    "col": 48,
    "offset": 3305
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 104, Column 15
- End: Line 104, Column 82

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 104,
    "col": 15,
    "offset": 3583
  },
  "end": {
    "line": 104,
    "col": 82,
    "offset": 3650
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 168, Column 27
- End: Line 171, Column 18

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 168,
    "col": 27,
    "offset": 6248
  },
  "end": {
    "line": 171,
    "col": 18,
    "offset": 6391
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 220, Column 30
- End: Line 220, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 220,
    "col": 30,
    "offset": 7900
  },
  "end": {
    "line": 220,
    "col": 55,
    "offset": 7925
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 251, Column 27
- End: Line 251, Column 75

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 251,
    "col": 27,
    "offset": 9256
  },
  "end": {
    "line": 251,
    "col": 75,
    "offset": 9304
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 254, Column 27
- End: Line 254, Column 72

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 254,
    "col": 27,
    "offset": 9384
  },
  "end": {
    "line": 254,
    "col": 72,
    "offset": 9429
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 38
<a name='finding-38'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/anyio/to_process.py`
- Start: Line 258, Column 23
- End: Line 258, Column 65

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/anyio/to_process.py",
  "start": {
    "line": 258,
    "col": 23,
    "offset": 9551
  },
  "end": {
    "line": 258,
    "col": 65,
    "offset": 9593
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

**Rule ID:** `python.lang.security.audit.eval-detected.eval-detected`

**Severity:** WARNING

**Message:** Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/attr/_make.py`
- Start: Line 227, Column 5
- End: Line 227, Column 32

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected
- **shortlink:** https://sg.run/ZvrD

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.eval-detected.eval-detected",
  "path": "venv/lib/python3.12/site-packages/attr/_make.py",
  "start": {
    "line": 227,
    "col": 5,
    "offset": 6274
  },
  "end": {
    "line": 227,
    "col": 32,
    "offset": 6301
  },
  "extra": {
    "message": "Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected",
      "shortlink": "https://sg.run/ZvrD"
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

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/attr/_make.py`
- Start: Line 3140, Column 13
- End: Line 3140, Column 57

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/attr/_make.py",
  "start": {
    "line": 3140,
    "col": 13,
    "offset": 98000
  },
  "end": {
    "line": 3140,
    "col": 57,
    "offset": 98044
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 41
<a name='finding-41'></a>

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/attr/_make.py`
- Start: Line 3393, Column 13
- End: Line 3393, Column 54

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/attr/_make.py",
  "start": {
    "line": 3393,
    "col": 13,
    "offset": 105656
  },
  "end": {
    "line": 3393,
    "col": 54,
    "offset": 105697
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 42
<a name='finding-42'></a>

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/attr/_make.py`
- Start: Line 3402, Column 13
- End: Line 3402, Column 58

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/attr/_make.py",
  "start": {
    "line": 3402,
    "col": 13,
    "offset": 105956
  },
  "end": {
    "line": 3402,
    "col": 58,
    "offset": 106001
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 43
<a name='finding-43'></a>

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/attr/converters.py`
- Start: Line 54, Column 9
- End: Line 54, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/attr/converters.py",
  "start": {
    "line": 54,
    "col": 9,
    "offset": 1082
  },
  "end": {
    "line": 54,
    "col": 71,
    "offset": 1144
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 44
<a name='finding-44'></a>

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/attr/converters.py`
- Start: Line 58, Column 9
- End: Line 58, Column 75

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/attr/converters.py",
  "start": {
    "line": 58,
    "col": 9,
    "offset": 1196
  },
  "end": {
    "line": 58,
    "col": 75,
    "offset": 1262
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 45
<a name='finding-45'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/boltons/funcutils.py`
- Start: Line 1035, Column 13
- End: Line 1035, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/boltons/funcutils.py",
  "start": {
    "line": 1035,
    "col": 13,
    "offset": 39050
  },
  "end": {
    "line": 1035,
    "col": 33,
    "offset": 39070
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/boltons/namedutils.py`
- Start: Line 68, Column 9
- End: Line 68, Column 31

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/boltons/namedutils.py",
  "start": {
    "line": 68,
    "col": 9,
    "offset": 2807
  },
  "end": {
    "line": 68,
    "col": 31,
    "offset": 2829
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/certifi/core.py`
- Start: Line 16, Column 5
- End: Line 16, Column 51

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/certifi/core.py",
  "start": {
    "line": 16,
    "col": 5,
    "offset": 275
  },
  "end": {
    "line": 16,
    "col": 51,
    "offset": 321
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 48
<a name='finding-48'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/certifi/core.py`
- Start: Line 51, Column 5
- End: Line 51, Column 64

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/certifi/core.py",
  "start": {
    "line": 51,
    "col": 5,
    "offset": 1842
  },
  "end": {
    "line": 51,
    "col": 64,
    "offset": 1901
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 49
<a name='finding-49'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/cffi/_cffi_gen_src.py`
- Start: Line 53, Column 5
- End: Line 53, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/cffi/_cffi_gen_src.py",
  "start": {
    "line": 53,
    "col": 5,
    "offset": 1970
  },
  "end": {
    "line": 53,
    "col": 33,
    "offset": 1998
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/cffi/cffi_opcode.py`
- Start: Line 180, Column 35
- End: Line 180, Column 50

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/cffi/cffi_opcode.py",
  "start": {
    "line": 180,
    "col": 35,
    "offset": 5417
  },
  "end": {
    "line": 180,
    "col": 50,
    "offset": 5432
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

**Rule ID:** `python.lang.security.audit.eval-detected.eval-detected`

**Severity:** WARNING

**Message:** Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/cffi/recompiler.py`
- Start: Line 80, Column 17
- End: Line 80, Column 42

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected
- **shortlink:** https://sg.run/ZvrD

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.eval-detected.eval-detected",
  "path": "venv/lib/python3.12/site-packages/cffi/recompiler.py",
  "start": {
    "line": 80,
    "col": 17,
    "offset": 2956
  },
  "end": {
    "line": 80,
    "col": 42,
    "offset": 2981
  },
  "extra": {
    "message": "Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected",
      "shortlink": "https://sg.run/ZvrD"
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

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/cffi/setuptools_ext.py`
- Start: Line 26, Column 5
- End: Line 26, Column 27

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/cffi/setuptools_ext.py",
  "start": {
    "line": 26,
    "col": 5,
    "offset": 689
  },
  "end": {
    "line": 26,
    "col": 27,
    "offset": 711
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/charset_normalizer/cd.py`
- Start: Line 38, Column 15
- End: Line 38, Column 64

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/charset_normalizer/cd.py",
  "start": {
    "line": 38,
    "col": 15,
    "offset": 895
  },
  "end": {
    "line": 38,
    "col": 64,
    "offset": 944
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/charset_normalizer/utils.py`
- Start: Line 281, Column 9
- End: Line 281, Column 53

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/charset_normalizer/utils.py",
  "start": {
    "line": 281,
    "col": 9,
    "offset": 7764
  },
  "end": {
    "line": 281,
    "col": 53,
    "offset": 7808
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/charset_normalizer/utils.py`
- Start: Line 329, Column 17
- End: Line 329, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/charset_normalizer/utils.py",
  "start": {
    "line": 329,
    "col": 17,
    "offset": 9122
  },
  "end": {
    "line": 329,
    "col": 68,
    "offset": 9173
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/charset_normalizer/utils.py`
- Start: Line 330, Column 17
- End: Line 330, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/charset_normalizer/utils.py",
  "start": {
    "line": 330,
    "col": 17,
    "offset": 9209
  },
  "end": {
    "line": 330,
    "col": 68,
    "offset": 9260
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

**Rule ID:** `python.lang.compatibility.python36.python36-compatibility-Popen1`

**Severity:** ERROR

**Message:** the `errors` argument to Popen is only available on Python 3.6+

## Location

- File: `venv/lib/python3.12/site-packages/click/_termui_impl.py`
- Start: Line 531, Column 9
- End: Line 538, Column 6

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python36.python36-compatibility-Popen1
- **shortlink:** https://sg.run/weBP

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python36.python36-compatibility-Popen1",
  "path": "venv/lib/python3.12/site-packages/click/_termui_impl.py",
  "start": {
    "line": 531,
    "col": 9,
    "offset": 18032
  },
  "end": {
    "line": 538,
    "col": 6,
    "offset": 18207
  },
  "extra": {
    "message": "the `errors` argument to Popen is only available on Python 3.6+",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python36.python36-compatibility-Popen1",
      "shortlink": "https://sg.run/weBP"
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

# Finding 58
<a name='finding-58'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/click/parser.py`
- Start: Line 520, Column 16
- End: Line 520, Column 37

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/click/parser.py",
  "start": {
    "line": 520,
    "col": 16,
    "offset": 18640
  },
  "end": {
    "line": 520,
    "col": 37,
    "offset": 18661
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 59
<a name='finding-59'></a>

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

# Finding 60
<a name='finding-60'></a>

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

# Finding 61
<a name='finding-61'></a>

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

# Finding 62
<a name='finding-62'></a>

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

# Finding 63
<a name='finding-63'></a>

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

# Finding 64
<a name='finding-64'></a>

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

# Finding 65
<a name='finding-65'></a>

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

# Finding 66
<a name='finding-66'></a>

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

# Finding 67
<a name='finding-67'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/face/sinter.py`
- Start: Line 142, Column 5
- End: Line 142, Column 20

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/face/sinter.py",
  "start": {
    "line": 142,
    "col": 5,
    "offset": 4791
  },
  "end": {
    "line": 142,
    "col": 20,
    "offset": 4806
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 68
<a name='finding-68'></a>

**Rule ID:** `python.lang.security.audit.eval-detected.eval-detected`

**Severity:** WARNING

**Message:** Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/flask/cli.py`
- Start: Line 1005, Column 13
- End: Line 1005, Column 58

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected
- **shortlink:** https://sg.run/ZvrD

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.eval-detected.eval-detected",
  "path": "venv/lib/python3.12/site-packages/flask/cli.py",
  "start": {
    "line": 1005,
    "col": 13,
    "offset": 32820
  },
  "end": {
    "line": 1005,
    "col": 58,
    "offset": 32865
  },
  "extra": {
    "message": "Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected",
      "shortlink": "https://sg.run/ZvrD"
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

# Finding 69
<a name='finding-69'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/flask/config.py`
- Start: Line 212, Column 17
- End: Line 212, Column 80

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/flask/config.py",
  "start": {
    "line": 212,
    "col": 17,
    "offset": 7315
  },
  "end": {
    "line": 212,
    "col": 80,
    "offset": 7378
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 70
<a name='finding-70'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/flask/json/tag.py`
- Start: Line 188, Column 16
- End: Line 188, Column 29

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/flask/json/tag.py",
  "start": {
    "line": 188,
    "col": 16,
    "offset": 5292
  },
  "end": {
    "line": 188,
    "col": 29,
    "offset": 5305
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 71
<a name='finding-71'></a>

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

# Finding 72
<a name='finding-72'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/glom/cli.py`
- Start: Line 239, Column 5
- End: Line 239, Column 20

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/glom/cli.py",
  "start": {
    "line": 239,
    "col": 5,
    "offset": 8068
  },
  "end": {
    "line": 239,
    "col": 20,
    "offset": 8083
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 73
<a name='finding-73'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/google/protobuf/internal/api_implementation.py`
- Start: Line 43, Column 11
- End: Line 43, Column 44

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/google/protobuf/internal/api_implementation.py",
  "start": {
    "line": 43,
    "col": 11,
    "offset": 1169
  },
  "end": {
    "line": 43,
    "col": 44,
    "offset": 1202
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 74
<a name='finding-74'></a>

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

# Finding 75
<a name='finding-75'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/__init__.py`
- Start: Line 141, Column 17
- End: Line 141, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/httpcore/__init__.py",
  "start": {
    "line": 141,
    "col": 17,
    "offset": 3393
  },
  "end": {
    "line": 141,
    "col": 33,
    "offset": 3409
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 76
<a name='finding-76'></a>

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

# Finding 77
<a name='finding-77'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py`
- Start: Line 84, Column 20
- End: Line 84, Column 87

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py",
  "start": {
    "line": 84,
    "col": 20,
    "offset": 2635
  },
  "end": {
    "line": 84,
    "col": 87,
    "offset": 2702
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

# Finding 78
<a name='finding-78'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py`
- Start: Line 86, Column 20
- End: Line 86, Column 85

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py",
  "start": {
    "line": 86,
    "col": 20,
    "offset": 2756
  },
  "end": {
    "line": 86,
    "col": 85,
    "offset": 2821
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

# Finding 79
<a name='finding-79'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py`
- Start: Line 88, Column 20
- End: Line 88, Column 86

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py",
  "start": {
    "line": 88,
    "col": 20,
    "offset": 2875
  },
  "end": {
    "line": 88,
    "col": 86,
    "offset": 2941
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

# Finding 80
<a name='finding-80'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py`
- Start: Line 90, Column 20
- End: Line 90, Column 82

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py",
  "start": {
    "line": 90,
    "col": 20,
    "offset": 2990
  },
  "end": {
    "line": 90,
    "col": 82,
    "offset": 3052
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

# Finding 81
<a name='finding-81'></a>

**Rule ID:** `python.django.security.audit.query-set-extra.avoid-query-set-extra`

**Severity:** WARNING

**Message:** QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.

## Location

- File: `venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py`
- Start: Line 92, Column 20
- End: Line 92, Column 82

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra
  - https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra
- **shortlink:** https://sg.run/kXZP

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.query-set-extra.avoid-query-set-extra",
  "path": "venv/lib/python3.12/site-packages/httpcore/_backends/anyio.py",
  "start": {
    "line": 92,
    "col": 20,
    "offset": 3106
  },
  "end": {
    "line": 92,
    "col": 82,
    "offset": 3168
  },
  "extra": {
    "message": "QuerySet.extra' does not provide safeguards against SQL injection and requires very careful use. SQL injection can lead to critical data being stolen by attackers. Instead of using '.extra', use the Django ORM and parameterized queries such as `People.objects.get(name='Bob')`.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b610_django_extra_used.html",
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/ref/models/querysets/#django.db.models.query.QuerySet.extra",
        "https://semgrep.dev/blog/2020/preventing-sql-injection-a-django-authors-perspective/"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.query-set-extra.avoid-query-set-extra",
      "shortlink": "https://sg.run/kXZP"
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

# Finding 82
<a name='finding-82'></a>

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

# Finding 83
<a name='finding-83'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/httpx/__init__.py`
- Start: Line 105, Column 17
- End: Line 105, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/httpx/__init__.py",
  "start": {
    "line": 105,
    "col": 17,
    "offset": 2122
  },
  "end": {
    "line": 105,
    "col": 33,
    "offset": 2138
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 84
<a name='finding-84'></a>

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

# Finding 85
<a name='finding-85'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/importlib_metadata/__init__.py`
- Start: Line 221, Column 18
- End: Line 221, Column 44

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/importlib_metadata/__init__.py",
  "start": {
    "line": 221,
    "col": 18,
    "offset": 5663
  },
  "end": {
    "line": 221,
    "col": 44,
    "offset": 5689
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 86
<a name='finding-86'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `venv/lib/python3.12/site-packages/itsdangerous-2.2.0.dist-info/METADATA`
- Start: Line 44, Column 3
- End: Line 44, Column 71

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "venv/lib/python3.12/site-packages/itsdangerous-2.2.0.dist-info/METADATA",
  "start": {
    "line": 44,
    "col": 3,
    "offset": 1481
  },
  "end": {
    "line": 44,
    "col": 71,
    "offset": 1549
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 87
<a name='finding-87'></a>

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

# Finding 88
<a name='finding-88'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 41, Column 7
- End: Line 41, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 41,
    "col": 7,
    "offset": 1026
  },
  "end": {
    "line": 41,
    "col": 34,
    "offset": 1053
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 89
<a name='finding-89'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 42, Column 7
- End: Line 42, Column 73

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 42,
    "col": 7,
    "offset": 1060
  },
  "end": {
    "line": 42,
    "col": 73,
    "offset": 1126
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 90
<a name='finding-90'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 73, Column 20
- End: Line 73, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 73,
    "col": 20,
    "offset": 2223
  },
  "end": {
    "line": 73,
    "col": 34,
    "offset": 2237
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 91
<a name='finding-91'></a>

**Rule ID:** `python.lang.security.audit.marshal.marshal-usage`

**Severity:** WARNING

**Message:** The marshal module is not intended to be secure against erroneous or maliciously constructed data. Never unmarshal data received from an untrusted or unauthenticated source. See more details: https://docs.python.org/3/library/marshal.html?highlight=security

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 79, Column 25
- End: Line 79, Column 40

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **references**
  - https://docs.python.org/3/library/marshal.html?highlight=security
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.audit.marshal.marshal-usage
- **shortlink:** https://sg.run/3xor

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.marshal.marshal-usage",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 79,
    "col": 25,
    "offset": 2412
  },
  "end": {
    "line": 79,
    "col": 40,
    "offset": 2427
  },
  "extra": {
    "message": "The marshal module is not intended to be secure against erroneous or maliciously constructed data. Never unmarshal data received from an untrusted or unauthenticated source. See more details: https://docs.python.org/3/library/marshal.html?highlight=security",
    "metadata": {
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "references": [
        "https://docs.python.org/3/library/marshal.html?highlight=security"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.marshal.marshal-usage",
      "shortlink": "https://sg.run/3xor"
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

# Finding 92
<a name='finding-92'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 89, Column 9
- End: Line 89, Column 41

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 89,
    "col": 9,
    "offset": 2771
  },
  "end": {
    "line": 89,
    "col": 41,
    "offset": 2803
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 93
<a name='finding-93'></a>

**Rule ID:** `python.lang.security.audit.marshal.marshal-usage`

**Severity:** WARNING

**Message:** The marshal module is not intended to be secure against erroneous or maliciously constructed data. Never unmarshal data received from an untrusted or unauthenticated source. See more details: https://docs.python.org/3/library/marshal.html?highlight=security

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/bccache.py`
- Start: Line 90, Column 9
- End: Line 90, Column 35

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **references**
  - https://docs.python.org/3/library/marshal.html?highlight=security
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.audit.marshal.marshal-usage
- **shortlink:** https://sg.run/3xor

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.marshal.marshal-usage",
  "path": "venv/lib/python3.12/site-packages/jinja2/bccache.py",
  "start": {
    "line": 90,
    "col": 9,
    "offset": 2812
  },
  "end": {
    "line": 90,
    "col": 35,
    "offset": 2838
  },
  "extra": {
    "message": "The marshal module is not intended to be secure against erroneous or maliciously constructed data. Never unmarshal data received from an untrusted or unauthenticated source. See more details: https://docs.python.org/3/library/marshal.html?highlight=security",
    "metadata": {
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "references": [
        "https://docs.python.org/3/library/marshal.html?highlight=security"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.marshal.marshal-usage",
      "shortlink": "https://sg.run/3xor"
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

# Finding 94
<a name='finding-94'></a>

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

# Finding 95
<a name='finding-95'></a>

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

# Finding 96
<a name='finding-96'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/debug.py`
- Start: Line 145, Column 9
- End: Line 145, Column 36

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/jinja2/debug.py",
  "start": {
    "line": 145,
    "col": 9,
    "offset": 4780
  },
  "end": {
    "line": 145,
    "col": 36,
    "offset": 4807
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 97
<a name='finding-97'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/environment.py`
- Start: Line 1228, Column 9
- End: Line 1228, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/jinja2/environment.py",
  "start": {
    "line": 1228,
    "col": 9,
    "offset": 46141
  },
  "end": {
    "line": 1228,
    "col": 30,
    "offset": 46162
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 98
<a name='finding-98'></a>

**Rule ID:** `python.django.security.audit.xss.html-magic-method.html-magic-method`

**Severity:** WARNING

**Message:** The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/environment.py`
- Start: Line 1543, Column 5
- End: Line 1544, Column 49

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
- **references**
  - https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape
  - https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method
- **shortlink:** https://sg.run/8y9N

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.xss.html-magic-method.html-magic-method",
  "path": "venv/lib/python3.12/site-packages/jinja2/environment.py",
  "start": {
    "line": 1543,
    "col": 5,
    "offset": 57308
  },
  "end": {
    "line": 1544,
    "col": 49,
    "offset": 57386
  },
  "extra": {
    "message": "The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape",
        "https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method",
      "shortlink": "https://sg.run/8y9N"
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

# Finding 99
<a name='finding-99'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/environment.py`
- Start: Line 1544, Column 16
- End: Line 1544, Column 49

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/environment.py",
  "start": {
    "line": 1544,
    "col": 16,
    "offset": 57353
  },
  "end": {
    "line": 1544,
    "col": 49,
    "offset": 57386
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 100
<a name='finding-100'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/ext.py`
- Start: Line 176, Column 18
- End: Line 176, Column 28

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/ext.py",
  "start": {
    "line": 176,
    "col": 18,
    "offset": 6171
  },
  "end": {
    "line": 176,
    "col": 28,
    "offset": 6181
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 101
<a name='finding-101'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/ext.py`
- Start: Line 197, Column 18
- End: Line 197, Column 28

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/ext.py",
  "start": {
    "line": 197,
    "col": 18,
    "offset": 6859
  },
  "end": {
    "line": 197,
    "col": 28,
    "offset": 6869
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 102
<a name='finding-102'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/ext.py`
- Start: Line 213, Column 18
- End: Line 213, Column 28

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/ext.py",
  "start": {
    "line": 213,
    "col": 18,
    "offset": 7395
  },
  "end": {
    "line": 213,
    "col": 28,
    "offset": 7405
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 103
<a name='finding-103'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/ext.py`
- Start: Line 238, Column 18
- End: Line 238, Column 28

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/ext.py",
  "start": {
    "line": 238,
    "col": 18,
    "offset": 8083
  },
  "end": {
    "line": 238,
    "col": 28,
    "offset": 8093
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 104
<a name='finding-104'></a>

**Rule ID:** `python.django.security.audit.xss.html-magic-method.html-magic-method`

**Severity:** WARNING

**Message:** The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 40, Column 9
- End: Line 41, Column 17

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
- **references**
  - https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape
  - https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method
- **shortlink:** https://sg.run/8y9N

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.xss.html-magic-method.html-magic-method",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 40,
    "col": 9,
    "offset": 1064
  },
  "end": {
    "line": 41,
    "col": 17,
    "offset": 1107
  },
  "extra": {
    "message": "The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape",
        "https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method",
      "shortlink": "https://sg.run/8y9N"
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

# Finding 105
<a name='finding-105'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 316, Column 14
- End: Line 316, Column 24

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 316,
    "col": 14,
    "offset": 9214
  },
  "end": {
    "line": 316,
    "col": 24,
    "offset": 9224
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 106
<a name='finding-106'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 820, Column 14
- End: Line 820, Column 24

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 820,
    "col": 14,
    "offset": 24382
  },
  "end": {
    "line": 820,
    "col": 24,
    "offset": 24392
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 107
<a name='finding-107'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 851, Column 21
- End: Line 851, Column 38

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 851,
    "col": 21,
    "offset": 25205
  },
  "end": {
    "line": 851,
    "col": 38,
    "offset": 25222
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 108
<a name='finding-108'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 1056, Column 12
- End: Line 1056, Column 30

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 1056,
    "col": 12,
    "offset": 31589
  },
  "end": {
    "line": 1056,
    "col": 30,
    "offset": 31607
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 109
<a name='finding-109'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/filters.py`
- Start: Line 1377, Column 12
- End: Line 1377, Column 25

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/filters.py",
  "start": {
    "line": 1377,
    "col": 12,
    "offset": 41325
  },
  "end": {
    "line": 1377,
    "col": 25,
    "offset": 41338
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 110
<a name='finding-110'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/loaders.py`
- Start: Line 323, Column 9
- End: Line 323, Column 36

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/jinja2/loaders.py",
  "start": {
    "line": 323,
    "col": 9,
    "offset": 11395
  },
  "end": {
    "line": 323,
    "col": 36,
    "offset": 11422
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 111
<a name='finding-111'></a>

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

# Finding 112
<a name='finding-112'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/nodes.py`
- Start: Line 619, Column 20
- End: Line 619, Column 37

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/nodes.py",
  "start": {
    "line": 619,
    "col": 20,
    "offset": 18815
  },
  "end": {
    "line": 619,
    "col": 37,
    "offset": 18832
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 113
<a name='finding-113'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/nodes.py`
- Start: Line 1091, Column 16
- End: Line 1091, Column 52

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/nodes.py",
  "start": {
    "line": 1091,
    "col": 16,
    "offset": 31439
  },
  "end": {
    "line": 1091,
    "col": 52,
    "offset": 31475
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 114
<a name='finding-114'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/nodes.py`
- Start: Line 1112, Column 20
- End: Line 1112, Column 32

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/nodes.py",
  "start": {
    "line": 1112,
    "col": 20,
    "offset": 32006
  },
  "end": {
    "line": 1112,
    "col": 32,
    "offset": 32018
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 115
<a name='finding-115'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/runtime.py`
- Start: Line 375, Column 20
- End: Line 375, Column 30

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/runtime.py",
  "start": {
    "line": 375,
    "col": 20,
    "offset": 12189
  },
  "end": {
    "line": 375,
    "col": 30,
    "offset": 12199
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 116
<a name='finding-116'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/runtime.py`
- Start: Line 389, Column 20
- End: Line 389, Column 30

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/runtime.py",
  "start": {
    "line": 389,
    "col": 20,
    "offset": 12562
  },
  "end": {
    "line": 389,
    "col": 30,
    "offset": 12572
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 117
<a name='finding-117'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/runtime.py`
- Start: Line 776, Column 20
- End: Line 776, Column 30

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/runtime.py",
  "start": {
    "line": 776,
    "col": 20,
    "offset": 25253
  },
  "end": {
    "line": 776,
    "col": 30,
    "offset": 25263
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 118
<a name='finding-118'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/runtime.py`
- Start: Line 787, Column 18
- End: Line 787, Column 28

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/runtime.py",
  "start": {
    "line": 787,
    "col": 18,
    "offset": 25568
  },
  "end": {
    "line": 787,
    "col": 28,
    "offset": 25578
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 119
<a name='finding-119'></a>

**Rule ID:** `python.django.security.audit.xss.html-magic-method.html-magic-method`

**Severity:** WARNING

**Message:** The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/runtime.py`
- Start: Line 988, Column 5
- End: Line 989, Column 25

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
- **references**
  - https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape
  - https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method
- **shortlink:** https://sg.run/8y9N

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.xss.html-magic-method.html-magic-method",
  "path": "venv/lib/python3.12/site-packages/jinja2/runtime.py",
  "start": {
    "line": 988,
    "col": 5,
    "offset": 31723
  },
  "end": {
    "line": 989,
    "col": 25,
    "offset": 31774
  },
  "extra": {
    "message": "The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape",
        "https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method",
      "shortlink": "https://sg.run/8y9N"
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

# Finding 120
<a name='finding-120'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/utils.py`
- Start: Line 403, Column 12
- End: Line 405, Column 6

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/utils.py",
  "start": {
    "line": 403,
    "col": 12,
    "offset": 12380
  },
  "end": {
    "line": 405,
    "col": 6,
    "offset": 12472
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 121
<a name='finding-121'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/jinja2/utils.py`
- Start: Line 668, Column 12
- End: Line 674, Column 6

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/jinja2/utils.py",
  "start": {
    "line": 668,
    "col": 12,
    "offset": 21182
  },
  "end": {
    "line": 674,
    "col": 6,
    "offset": 21367
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 122
<a name='finding-122'></a>

**Rule ID:** `python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected`

**Severity:** WARNING

**Message:** Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.

## Location

- File: `venv/lib/python3.12/site-packages/jsonschema/validators.py`
- Start: Line 113, Column 10
- End: Line 113, Column 26

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-939: Improper Authorization in Handler for Custom URL Scheme
- **owasp:** A01:2017 - Injection
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163
- **bandit-code:** B310
- **asvs**
  - control_id: 5.2.4 Dynamic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://cwe.mitre.org/data/definitions/939.html
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected
- **shortlink:** https://sg.run/dKZZ

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
  "path": "venv/lib/python3.12/site-packages/jsonschema/validators.py",
  "start": {
    "line": 113,
    "col": 10,
    "offset": 3104
  },
  "end": {
    "line": 113,
    "col": 26,
    "offset": 3120
  },
  "extra": {
    "message": "Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.",
    "metadata": {
      "cwe": [
        "CWE-939: Improper Authorization in Handler for Custom URL Scheme"
      ],
      "owasp": "A01:2017 - Injection",
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163",
      "bandit-code": "B310",
      "asvs": {
        "control_id": "5.2.4 Dynamic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://cwe.mitre.org/data/definitions/939.html"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
      "shortlink": "https://sg.run/dKZZ"
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

# Finding 123
<a name='finding-123'></a>

**Rule ID:** `python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected`

**Severity:** WARNING

**Message:** Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.

## Location

- File: `venv/lib/python3.12/site-packages/jsonschema/validators.py`
- Start: Line 1228, Column 18
- End: Line 1228, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-939: Improper Authorization in Handler for Custom URL Scheme
- **owasp:** A01:2017 - Injection
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163
- **bandit-code:** B310
- **asvs**
  - control_id: 5.2.4 Dynamic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://cwe.mitre.org/data/definitions/939.html
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected
- **shortlink:** https://sg.run/dKZZ

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
  "path": "venv/lib/python3.12/site-packages/jsonschema/validators.py",
  "start": {
    "line": 1228,
    "col": 18,
    "offset": 41689
  },
  "end": {
    "line": 1228,
    "col": 30,
    "offset": 41701
  },
  "extra": {
    "message": "Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.",
    "metadata": {
      "cwe": [
        "CWE-939: Improper Authorization in Handler for Custom URL Scheme"
      ],
      "owasp": "A01:2017 - Injection",
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163",
      "bandit-code": "B310",
      "asvs": {
        "control_id": "5.2.4 Dynamic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://cwe.mitre.org/data/definitions/939.html"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
      "shortlink": "https://sg.run/dKZZ"
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

# Finding 124
<a name='finding-124'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/jsonschema_specifications/_core.py`
- Start: Line 8, Column 5
- End: Line 8, Column 42

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/jsonschema_specifications/_core.py",
  "start": {
    "line": 8,
    "col": 5,
    "offset": 90
  },
  "end": {
    "line": 8,
    "col": 42,
    "offset": 127
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 125
<a name='finding-125'></a>

**Rule ID:** `python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected`

**Severity:** WARNING

**Message:** Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.

## Location

- File: `venv/lib/python3.12/site-packages/jwt/jwks_client.py`
- Start: Line 118, Column 18
- End: Line 120, Column 14

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-939: Improper Authorization in Handler for Custom URL Scheme
- **owasp:** A01:2017 - Injection
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163
- **bandit-code:** B310
- **asvs**
  - control_id: 5.2.4 Dynamic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://cwe.mitre.org/data/definitions/939.html
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected
- **shortlink:** https://sg.run/dKZZ

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
  "path": "venv/lib/python3.12/site-packages/jwt/jwks_client.py",
  "start": {
    "line": 118,
    "col": 18,
    "offset": 4751
  },
  "end": {
    "line": 120,
    "col": 14,
    "offset": 4854
  },
  "extra": {
    "message": "Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.",
    "metadata": {
      "cwe": [
        "CWE-939: Improper Authorization in Handler for Custom URL Scheme"
      ],
      "owasp": "A01:2017 - Injection",
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163",
      "bandit-code": "B310",
      "asvs": {
        "control_id": "5.2.4 Dynamic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://cwe.mitre.org/data/definitions/939.html"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
      "shortlink": "https://sg.run/dKZZ"
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

# Finding 126
<a name='finding-126'></a>

**Rule ID:** `python.django.security.audit.xss.html-magic-method.html-magic-method`

**Severity:** WARNING

**Message:** The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.

## Location

- File: `venv/lib/python3.12/site-packages/markupsafe/__init__.py`
- Start: Line 17, Column 5
- End: Line 17, Column 38

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
- **references**
  - https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape
  - https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method
- **shortlink:** https://sg.run/8y9N

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.xss.html-magic-method.html-magic-method",
  "path": "venv/lib/python3.12/site-packages/markupsafe/__init__.py",
  "start": {
    "line": 17,
    "col": 5,
    "offset": 296
  },
  "end": {
    "line": 17,
    "col": 38,
    "offset": 329
  },
  "extra": {
    "message": "The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape",
        "https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method",
      "shortlink": "https://sg.run/8y9N"
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

# Finding 127
<a name='finding-127'></a>

**Rule ID:** `python.django.security.audit.xss.html-magic-method.html-magic-method`

**Severity:** WARNING

**Message:** The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.

## Location

- File: `venv/lib/python3.12/site-packages/markupsafe/__init__.py`
- Start: Line 133, Column 5
- End: Line 134, Column 20

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
- **references**
  - https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape
  - https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5
- **category:** security
- **technology**
  - django
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method
- **shortlink:** https://sg.run/8y9N

## Raw Finding JSON

```json
{
  "check_id": "python.django.security.audit.xss.html-magic-method.html-magic-method",
  "path": "venv/lib/python3.12/site-packages/markupsafe/__init__.py",
  "start": {
    "line": 133,
    "col": 5,
    "offset": 3849
  },
  "end": {
    "line": 134,
    "col": 20,
    "offset": 3902
  },
  "extra": {
    "message": "The `__html__` method indicates to the Django template engine that the value is 'safe' for rendering. This means that normal HTML escaping will not be applied to the return value. This exposes your application to cross-site scripting (XSS) vulnerabilities. If you need to render raw HTML, consider instead using `mark_safe()` which more clearly marks the intent to render raw HTML than a class with a magic method.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.djangoproject.com/en/3.0/_modules/django/utils/html/#conditional_escape",
        "https://gist.github.com/minusworld/7885d8a81dba3ea2d1e4b8fd3c218ef5"
      ],
      "category": "security",
      "technology": [
        "django"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.django.security.audit.xss.html-magic-method.html-magic-method",
      "shortlink": "https://sg.run/8y9N"
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

# Finding 128
<a name='finding-128'></a>

**Rule ID:** `python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup`

**Severity:** WARNING

**Message:** Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.

## Location

- File: `venv/lib/python3.12/site-packages/markupsafe/__init__.py`
- Start: Line 228, Column 16
- End: Line 228, Column 48

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
- **references**
  - https://tedboy.github.io/flask/generated/generated/flask.Markup.html
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup
- **shortlink:** https://sg.run/AvZ8

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
  "path": "venv/lib/python3.12/site-packages/markupsafe/__init__.py",
  "start": {
    "line": 228,
    "col": 16,
    "offset": 7410
  },
  "end": {
    "line": 228,
    "col": 48,
    "offset": 7442
  },
  "extra": {
    "message": "Detected explicitly unescaped content using 'Markup()'. This permits the unescaped data to include unescaped HTML which could result in cross-site scripting. Ensure this data is not externally controlled, or consider rewriting to not use 'Markup()'.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://tedboy.github.io/flask/generated/generated/flask.Markup.html"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.explicit-unescape-with-markup.explicit-unescape-with-markup",
      "shortlink": "https://sg.run/AvZ8"
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

# Finding 129
<a name='finding-129'></a>

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

# Finding 130
<a name='finding-130'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/mcp/cli/cli.py`
- Start: Line 186, Column 29
- End: Line 186, Column 65

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/mcp/cli/cli.py",
  "start": {
    "line": 186,
    "col": 29,
    "offset": 6093
  },
  "end": {
    "line": 186,
    "col": 65,
    "offset": 6129
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 131
<a name='finding-131'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/opentelemetry/instrumentation/utils.py`
- Start: Line 102, Column 18
- End: Line 102, Column 44

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/opentelemetry/instrumentation/utils.py",
  "start": {
    "line": 102,
    "col": 18,
    "offset": 3282
  },
  "end": {
    "line": 102,
    "col": 44,
    "offset": 3308
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 132
<a name='finding-132'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 3632, Column 13
- End: Line 3632, Column 64

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 3632,
    "col": 13,
    "offset": 114458
  },
  "end": {
    "line": 3632,
    "col": 64,
    "offset": 114509
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 133
<a name='finding-133'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 3632, Column 13
- End: Line 3632, Column 64

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 3632,
    "col": 13,
    "offset": 114458
  },
  "end": {
    "line": 3632,
    "col": 64,
    "offset": 114509
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 134
<a name='finding-134'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 3638, Column 13
- End: Line 3638, Column 72

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 3638,
    "col": 13,
    "offset": 114664
  },
  "end": {
    "line": 3638,
    "col": 72,
    "offset": 114723
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 135
<a name='finding-135'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 3638, Column 13
- End: Line 3638, Column 72

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 3638,
    "col": 13,
    "offset": 114664
  },
  "end": {
    "line": 3638,
    "col": 72,
    "offset": 114723
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 136
<a name='finding-136'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 4279, Column 17
- End: Line 4280, Column 46

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 4279,
    "col": 17,
    "offset": 139357
  },
  "end": {
    "line": 4280,
    "col": 46,
    "offset": 139454
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 137
<a name='finding-137'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/peewee.py`
- Start: Line 4279, Column 17
- End: Line 4280, Column 46

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/peewee.py",
  "start": {
    "line": 4279,
    "col": 17,
    "offset": 139357
  },
  "end": {
    "line": 4280,
    "col": 46,
    "offset": 139454
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 138
<a name='finding-138'></a>

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

# Finding 139
<a name='finding-139'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/commands/__init__.py`
- Start: Line 121, Column 14
- End: Line 121, Column 50

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/commands/__init__.py",
  "start": {
    "line": 121,
    "col": 14,
    "offset": 3543
  },
  "end": {
    "line": 121,
    "col": 50,
    "offset": 3579
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 140
<a name='finding-140'></a>

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

# Finding 141
<a name='finding-141'></a>

**Rule ID:** `python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc`

**Severity:** ERROR

**Message:** Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/commands/search.py`
- Start: Line 7, Column 1
- End: Line 7, Column 21

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')
- **owasp**
  - A04:2017 - XML External Entities (XXE)
  - A05:2021 - Security Misconfiguration
  - A02:2025 - Security Misconfiguration
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160
- **references**
  - https://pypi.org/project/defusedxml/
  - https://docs.python.org/3/library/xml.html#xml-vulnerabilities
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - XML Injection
- **source:** https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc
- **shortlink:** https://sg.run/weqY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/commands/search.py",
  "start": {
    "line": 7,
    "col": 1,
    "offset": 92
  },
  "end": {
    "line": 7,
    "col": 21,
    "offset": 112
  },
  "extra": {
    "message": "Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.",
    "metadata": {
      "cwe": [
        "CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')"
      ],
      "owasp": [
        "A04:2017 - XML External Entities (XXE)",
        "A05:2021 - Security Misconfiguration",
        "A02:2025 - Security Misconfiguration"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160",
      "references": [
        "https://pypi.org/project/defusedxml/",
        "https://docs.python.org/3/library/xml.html#xml-vulnerabilities"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "XML Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
      "shortlink": "https://sg.run/weqY"
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

# Finding 142
<a name='finding-142'></a>

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

# Finding 143
<a name='finding-143'></a>

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

# Finding 144
<a name='finding-144'></a>

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

# Finding 145
<a name='finding-145'></a>

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

# Finding 146
<a name='finding-146'></a>

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

# Finding 147
<a name='finding-147'></a>

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

# Finding 148
<a name='finding-148'></a>

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

# Finding 149
<a name='finding-149'></a>

**Rule ID:** `python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc`

**Severity:** ERROR

**Message:** Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py`
- Start: Line 5, Column 1
- End: Line 5, Column 21

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')
- **owasp**
  - A04:2017 - XML External Entities (XXE)
  - A05:2021 - Security Misconfiguration
  - A02:2025 - Security Misconfiguration
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160
- **references**
  - https://pypi.org/project/defusedxml/
  - https://docs.python.org/3/library/xml.html#xml-vulnerabilities
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - XML Injection
- **source:** https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc
- **shortlink:** https://sg.run/weqY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py",
  "start": {
    "line": 5,
    "col": 1,
    "offset": 77
  },
  "end": {
    "line": 5,
    "col": 21,
    "offset": 97
  },
  "extra": {
    "message": "Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.",
    "metadata": {
      "cwe": [
        "CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')"
      ],
      "owasp": [
        "A04:2017 - XML External Entities (XXE)",
        "A05:2021 - Security Misconfiguration",
        "A02:2025 - Security Misconfiguration"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160",
      "references": [
        "https://pypi.org/project/defusedxml/",
        "https://docs.python.org/3/library/xml.html#xml-vulnerabilities"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "XML Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
      "shortlink": "https://sg.run/weqY"
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

# Finding 150
<a name='finding-150'></a>

**Rule ID:** `python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc`

**Severity:** ERROR

**Message:** Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py`
- Start: Line 13, Column 5
- End: Line 13, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')
- **owasp**
  - A04:2017 - XML External Entities (XXE)
  - A05:2021 - Security Misconfiguration
  - A02:2025 - Security Misconfiguration
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160
- **references**
  - https://pypi.org/project/defusedxml/
  - https://docs.python.org/3/library/xml.html#xml-vulnerabilities
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - XML Injection
- **source:** https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc
- **shortlink:** https://sg.run/weqY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/network/xmlrpc.py",
  "start": {
    "line": 13,
    "col": 5,
    "offset": 325
  },
  "end": {
    "line": 13,
    "col": 55,
    "offset": 375
  },
  "extra": {
    "message": "Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.",
    "metadata": {
      "cwe": [
        "CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')"
      ],
      "owasp": [
        "A04:2017 - XML External Entities (XXE)",
        "A05:2021 - Security Misconfiguration",
        "A02:2025 - Security Misconfiguration"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160",
      "references": [
        "https://pypi.org/project/defusedxml/",
        "https://docs.python.org/3/library/xml.html#xml-vulnerabilities"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "XML Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
      "shortlink": "https://sg.run/weqY"
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

# Finding 151
<a name='finding-151'></a>

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

# Finding 152
<a name='finding-152'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/utils/compat.py`
- Start: Line 4, Column 1
- End: Line 4, Column 27

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/utils/compat.py",
  "start": {
    "line": 4,
    "col": 1,
    "offset": 83
  },
  "end": {
    "line": 4,
    "col": 27,
    "offset": 109
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 153
<a name='finding-153'></a>

**Rule ID:** `python.lang.compatibility.python36.python36-compatibility-Popen1`

**Severity:** ERROR

**Message:** the `errors` argument to Popen is only available on Python 3.6+

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/utils/subprocess.py`
- Start: Line 129, Column 16
- End: Line 138, Column 10

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python36.python36-compatibility-Popen1
- **shortlink:** https://sg.run/weBP

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python36.python36-compatibility-Popen1",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/utils/subprocess.py",
  "start": {
    "line": 129,
    "col": 16,
    "offset": 4960
  },
  "end": {
    "line": 138,
    "col": 10,
    "offset": 5319
  },
  "extra": {
    "message": "the `errors` argument to Popen is only available on Python 3.6+",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python36.python36-compatibility-Popen1",
      "shortlink": "https://sg.run/weBP"
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

# Finding 154
<a name='finding-154'></a>

**Rule ID:** `trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal`

**Severity:** ERROR

**Message:** Possible path traversal through `tarfile.open($PATH).extractall()` if the source tar is controlled by an attacker

## Location

- File: `venv/lib/python3.12/site-packages/pip/_internal/utils/unpacking.py`
- Start: Line 180, Column 5
- End: Line 248, Column 20

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')
- **subcategory**
  - vuln
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **technology**
  - --no-technology--
- **description:** Potential path traversal in call to `extractall` for a `tarfile`
- **references**
  - https://docs.python.org/3/library/tarfile.html#tarfile.TarFile.extractall
- **license:** AGPL-3.0 license
- **vulnerability_class**
  - Path Traversal
- **source:** https://semgrep.dev/r/trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal
- **shortlink:** https://sg.run/2RLD

## Raw Finding JSON

```json
{
  "check_id": "trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal",
  "path": "venv/lib/python3.12/site-packages/pip/_internal/utils/unpacking.py",
  "start": {
    "line": 180,
    "col": 5,
    "offset": 5650
  },
  "end": {
    "line": 248,
    "col": 20,
    "offset": 8836
  },
  "extra": {
    "message": "Possible path traversal through `tarfile.open($PATH).extractall()` if the source tar is controlled by an attacker",
    "metadata": {
      "category": "security",
      "cwe": "CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')",
      "subcategory": [
        "vuln"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "technology": [
        "--no-technology--"
      ],
      "description": "Potential path traversal in call to `extractall` for a `tarfile`",
      "references": [
        "https://docs.python.org/3/library/tarfile.html#tarfile.TarFile.extractall"
      ],
      "license": "AGPL-3.0 license",
      "vulnerability_class": [
        "Path Traversal"
      ],
      "source": "https://semgrep.dev/r/trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal",
      "shortlink": "https://sg.run/2RLD"
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

# Finding 155
<a name='finding-155'></a>

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

# Finding 156
<a name='finding-156'></a>

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

# Finding 157
<a name='finding-157'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py`
- Start: Line 16, Column 5
- End: Line 16, Column 51

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py",
  "start": {
    "line": 16,
    "col": 5,
    "offset": 275
  },
  "end": {
    "line": 16,
    "col": 51,
    "offset": 321
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 158
<a name='finding-158'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py`
- Start: Line 51, Column 5
- End: Line 51, Column 64

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/certifi/core.py",
  "start": {
    "line": 51,
    "col": 5,
    "offset": 1866
  },
  "end": {
    "line": 51,
    "col": 64,
    "offset": 1925
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 159
<a name='finding-159'></a>

**Rule ID:** `python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc`

**Severity:** ERROR

**Message:** Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py`
- Start: Line 42, Column 5
- End: Line 42, Column 21

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')
- **owasp**
  - A04:2017 - XML External Entities (XXE)
  - A05:2021 - Security Misconfiguration
  - A02:2025 - Security Misconfiguration
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160
- **references**
  - https://pypi.org/project/defusedxml/
  - https://docs.python.org/3/library/xml.html#xml-vulnerabilities
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - XML Injection
- **source:** https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc
- **shortlink:** https://sg.run/weqY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py",
  "start": {
    "line": 42,
    "col": 5,
    "offset": 1236
  },
  "end": {
    "line": 42,
    "col": 21,
    "offset": 1252
  },
  "extra": {
    "message": "Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.",
    "metadata": {
      "cwe": [
        "CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')"
      ],
      "owasp": [
        "A04:2017 - XML External Entities (XXE)",
        "A05:2021 - Security Misconfiguration",
        "A02:2025 - Security Misconfiguration"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160",
      "references": [
        "https://pypi.org/project/defusedxml/",
        "https://docs.python.org/3/library/xml.html#xml-vulnerabilities"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "XML Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
      "shortlink": "https://sg.run/weqY"
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

# Finding 160
<a name='finding-160'></a>

**Rule ID:** `python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc`

**Severity:** ERROR

**Message:** Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py`
- Start: Line 81, Column 5
- End: Line 81, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')
- **owasp**
  - A04:2017 - XML External Entities (XXE)
  - A05:2021 - Security Misconfiguration
  - A02:2025 - Security Misconfiguration
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160
- **references**
  - https://pypi.org/project/defusedxml/
  - https://docs.python.org/3/library/xml.html#xml-vulnerabilities
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - XML Injection
- **source:** https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc
- **shortlink:** https://sg.run/weqY

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/distlib/compat.py",
  "start": {
    "line": 81,
    "col": 5,
    "offset": 2704
  },
  "end": {
    "line": 81,
    "col": 38,
    "offset": 2737
  },
  "extra": {
    "message": "Detected use of xmlrpc. xmlrpc is not inherently safe from vulnerabilities. Use defusedxml.xmlrpc instead.",
    "metadata": {
      "cwe": [
        "CWE-776: Improper Restriction of Recursive Entity References in DTDs ('XML Entity Expansion')"
      ],
      "owasp": [
        "A04:2017 - XML External Entities (XXE)",
        "A05:2021 - Security Misconfiguration",
        "A02:2025 - Security Misconfiguration"
      ],
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/07f84cb5f5e7c1055e6feaa0fe93afa471de0ac3/bandit/blacklists/imports.py#L160",
      "references": [
        "https://pypi.org/project/defusedxml/",
        "https://docs.python.org/3/library/xml.html#xml-vulnerabilities"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "XML Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.use-defused-xmlrpc.use-defused-xmlrpc",
      "shortlink": "https://sg.run/weqY"
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

# Finding 161
<a name='finding-161'></a>

**Rule ID:** `python.lang.security.audit.httpsconnection-detected.httpsconnection-detected`

**Severity:** WARNING

**Message:** The HTTPSConnection API has changed frequently with minor releases of Python. Ensure you are using the API for your version of Python securely. For example, Python 3 versions prior to 3.4.3 will not verify SSL certificates by default. See https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection for more information.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/distlib/util.py`
- Start: Line 1572, Column 42
- End: Line 1572, Column 84

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A07:2021 - Identification and Authentication Failures
  - A07:2025 - Authentication Failures
- **cwe**
  - CWE-295: Improper Certificate Validation
- **references**
  - https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authentication
- **source:** https://semgrep.dev/r/python.lang.security.audit.httpsconnection-detected.httpsconnection-detected
- **shortlink:** https://sg.run/8yby

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.httpsconnection-detected.httpsconnection-detected",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/distlib/util.py",
  "start": {
    "line": 1572,
    "col": 42,
    "offset": 52883
  },
  "end": {
    "line": 1572,
    "col": 84,
    "offset": 52925
  },
  "extra": {
    "message": "The HTTPSConnection API has changed frequently with minor releases of Python. Ensure you are using the API for your version of Python securely. For example, Python 3 versions prior to 3.4.3 will not verify SSL certificates by default. See https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection for more information.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A07:2021 - Identification and Authentication Failures",
        "A07:2025 - Authentication Failures"
      ],
      "cwe": [
        "CWE-295: Improper Certificate Validation"
      ],
      "references": [
        "https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authentication"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.httpsconnection-detected.httpsconnection-detected",
      "shortlink": "https://sg.run/8yby"
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

# Finding 162
<a name='finding-162'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 168, Column 20
- End: Line 168, Column 35

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 168,
    "col": 20,
    "offset": 4884
  },
  "end": {
    "line": 168,
    "col": 35,
    "offset": 4899
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 163
<a name='finding-163'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 168, Column 36
- End: Line 168, Column 40

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 168,
    "col": 36,
    "offset": 4900
  },
  "end": {
    "line": 168,
    "col": 40,
    "offset": 4904
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 164
<a name='finding-164'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 175, Column 9
- End: Line 175, Column 37

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 175,
    "col": 9,
    "offset": 5041
  },
  "end": {
    "line": 175,
    "col": 37,
    "offset": 5069
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 165
<a name='finding-165'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 175, Column 41
- End: Line 175, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 175,
    "col": 41,
    "offset": 5073
  },
  "end": {
    "line": 175,
    "col": 45,
    "offset": 5077
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 166
<a name='finding-166'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 1714, Column 13
- End: Line 1714, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 1714,
    "col": 13,
    "offset": 59408
  },
  "end": {
    "line": 1714,
    "col": 45,
    "offset": 59440
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 167
<a name='finding-167'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 1725, Column 13
- End: Line 1725, Column 52

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 1725,
    "col": 13,
    "offset": 59760
  },
  "end": {
    "line": 1725,
    "col": 52,
    "offset": 59799
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 168
<a name='finding-168'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py`
- Start: Line 2468, Column 9
- End: Line 2468, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pkg_resources/__init__.py",
  "start": {
    "line": 2468,
    "col": 9,
    "offset": 83676
  },
  "end": {
    "line": 2468,
    "col": 45,
    "offset": 83712
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 169
<a name='finding-169'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pygments/formatters/__init__.py`
- Start: Line 103, Column 13
- End: Line 103, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pygments/formatters/__init__.py",
  "start": {
    "line": 103,
    "col": 13,
    "offset": 3353
  },
  "end": {
    "line": 103,
    "col": 45,
    "offset": 3385
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 170
<a name='finding-170'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pygments/lexers/__init__.py`
- Start: Line 154, Column 13
- End: Line 154, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pygments/lexers/__init__.py",
  "start": {
    "line": 154,
    "col": 13,
    "offset": 4982
  },
  "end": {
    "line": 154,
    "col": 45,
    "offset": 5014
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 171
<a name='finding-171'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py`
- Start: Line 83, Column 20
- End: Line 83, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py",
  "start": {
    "line": 83,
    "col": 20,
    "offset": 61125
  },
  "end": {
    "line": 83,
    "col": 34,
    "offset": 61139
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 172
<a name='finding-172'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py`
- Start: Line 90, Column 20
- End: Line 90, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pygments/unistring.py",
  "start": {
    "line": 90,
    "col": 20,
    "offset": 61271
  },
  "end": {
    "line": 90,
    "col": 34,
    "offset": 61285
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 173
<a name='finding-173'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py`
- Start: Line 7, Column 1
- End: Line 7, Column 40

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py",
  "start": {
    "line": 7,
    "col": 1,
    "offset": 192
  },
  "end": {
    "line": 7,
    "col": 40,
    "offset": 231
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 174
<a name='finding-174'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py`
- Start: Line 70, Column 15
- End: Line 70, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py",
  "start": {
    "line": 70,
    "col": 15,
    "offset": 1924
  },
  "end": {
    "line": 70,
    "col": 38,
    "offset": 1947
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 175
<a name='finding-175'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py`
- Start: Line 367, Column 12
- End: Line 367, Column 32

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py",
  "start": {
    "line": 367,
    "col": 12,
    "offset": 11470
  },
  "end": {
    "line": 367,
    "col": 32,
    "offset": 11490
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 176
<a name='finding-176'></a>

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

# Finding 177
<a name='finding-177'></a>

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

# Finding 178
<a name='finding-178'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py`
- Start: Line 196, Column 48
- End: Line 196, Column 59

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py",
  "start": {
    "line": 196,
    "col": 48,
    "offset": 6345
  },
  "end": {
    "line": 196,
    "col": 59,
    "offset": 6356
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 179
<a name='finding-179'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py`
- Start: Line 247, Column 23
- End: Line 247, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py",
  "start": {
    "line": 247,
    "col": 23,
    "offset": 8116
  },
  "end": {
    "line": 247,
    "col": 34,
    "offset": 8127
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 180
<a name='finding-180'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py`
- Start: Line 471, Column 67
- End: Line 471, Column 84

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py",
  "start": {
    "line": 471,
    "col": 67,
    "offset": 16184
  },
  "end": {
    "line": 471,
    "col": 84,
    "offset": 16201
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 181
<a name='finding-181'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py`
- Start: Line 747, Column 31
- End: Line 747, Column 65

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/rich/style.py",
  "start": {
    "line": 747,
    "col": 31,
    "offset": 25767
  },
  "end": {
    "line": 747,
    "col": 65,
    "offset": 25801
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 182
<a name='finding-182'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers`

**Severity:** WARNING

**Message:** The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/truststore/_api.py`
- Start: Line 186, Column 16
- End: Line 186, Column 51

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
  - CWE-326: Inadequate Encryption Strength
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://docs.python.org/3/library/ssl.html#cipher-selection
  - https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers
- **category:** security
- **technology**
  - ssl
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers
- **shortlink:** https://sg.run/0Q0v

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/truststore/_api.py",
  "start": {
    "line": 186,
    "col": 16,
    "offset": 6404
  },
  "end": {
    "line": 186,
    "col": 51,
    "offset": 6439
  },
  "extra": {
    "message": "The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://docs.python.org/3/library/ssl.html#cipher-selection",
        "https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers"
      ],
      "category": "security",
      "technology": [
        "ssl"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
      "shortlink": "https://sg.run/0Q0v"
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

# Finding 183
<a name='finding-183'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/emscripten/fetch.py`
- Start: Line 42, Column 1
- End: Line 42, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/urllib3/contrib/emscripten/fetch.py",
  "start": {
    "line": 42,
    "col": 1,
    "offset": 1862
  },
  "end": {
    "line": 42,
    "col": 38,
    "offset": 1899
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 184
<a name='finding-184'></a>

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

# Finding 185
<a name='finding-185'></a>

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

# Finding 186
<a name='finding-186'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers`

**Severity:** WARNING

**Message:** The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.

## Location

- File: `venv/lib/python3.12/site-packages/pip/_vendor/urllib3/util/ssl_.py`
- Start: Line 311, Column 9
- End: Line 311, Column 37

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
  - CWE-326: Inadequate Encryption Strength
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://docs.python.org/3/library/ssl.html#cipher-selection
  - https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers
- **category:** security
- **technology**
  - ssl
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers
- **shortlink:** https://sg.run/0Q0v

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
  "path": "venv/lib/python3.12/site-packages/pip/_vendor/urllib3/util/ssl_.py",
  "start": {
    "line": 311,
    "col": 9,
    "offset": 11781
  },
  "end": {
    "line": 311,
    "col": 37,
    "offset": 11809
  },
  "extra": {
    "message": "The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://docs.python.org/3/library/ssl.html#cipher-selection",
        "https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers"
      ],
      "category": "security",
      "technology": [
        "ssl"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
      "shortlink": "https://sg.run/0Q0v"
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

# Finding 187
<a name='finding-187'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/apsw_ext.py`
- Start: Line 112, Column 9
- End: Line 112, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/apsw_ext.py",
  "start": {
    "line": 112,
    "col": 9,
    "offset": 3849
  },
  "end": {
    "line": 112,
    "col": 55,
    "offset": 3895
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 188
<a name='finding-188'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/apsw_ext.py`
- Start: Line 112, Column 9
- End: Line 112, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/apsw_ext.py",
  "start": {
    "line": 112,
    "col": 9,
    "offset": 3849
  },
  "end": {
    "line": 112,
    "col": 55,
    "offset": 3895
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 189
<a name='finding-189'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/cockroachdb.py`
- Start: Line 153, Column 13
- End: Line 153, Column 76

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/cockroachdb.py",
  "start": {
    "line": 153,
    "col": 13,
    "offset": 6252
  },
  "end": {
    "line": 153,
    "col": 76,
    "offset": 6315
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 190
<a name='finding-190'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/cockroachdb.py`
- Start: Line 153, Column 13
- End: Line 153, Column 76

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/cockroachdb.py",
  "start": {
    "line": 153,
    "col": 13,
    "offset": 6252
  },
  "end": {
    "line": 153,
    "col": 76,
    "offset": 6315
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 191
<a name='finding-191'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-cPickle`

**Severity:** WARNING

**Message:** Avoid using `cPickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/fields.py`
- Start: Line 55, Column 20
- End: Line 55, Column 39

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-cPickle
- **shortlink:** https://sg.run/eLxb

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-cPickle",
  "path": "venv/lib/python3.12/site-packages/playhouse/fields.py",
  "start": {
    "line": 55,
    "col": 20,
    "offset": 1504
  },
  "end": {
    "line": 55,
    "col": 39,
    "offset": 1523
  },
  "extra": {
    "message": "Avoid using `cPickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-cPickle",
      "shortlink": "https://sg.run/eLxb"
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

# Finding 192
<a name='finding-192'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/fields.py`
- Start: Line 55, Column 20
- End: Line 55, Column 39

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/playhouse/fields.py",
  "start": {
    "line": 55,
    "col": 20,
    "offset": 1504
  },
  "end": {
    "line": 55,
    "col": 39,
    "offset": 1523
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 193
<a name='finding-193'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-cPickle`

**Severity:** WARNING

**Message:** Avoid using `cPickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/fields.py`
- Start: Line 59, Column 23
- End: Line 59, Column 67

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-cPickle
- **shortlink:** https://sg.run/eLxb

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-cPickle",
  "path": "venv/lib/python3.12/site-packages/playhouse/fields.py",
  "start": {
    "line": 59,
    "col": 23,
    "offset": 1608
  },
  "end": {
    "line": 59,
    "col": 67,
    "offset": 1652
  },
  "extra": {
    "message": "Avoid using `cPickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-cPickle",
      "shortlink": "https://sg.run/eLxb"
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

# Finding 194
<a name='finding-194'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/fields.py`
- Start: Line 59, Column 23
- End: Line 59, Column 67

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/playhouse/fields.py",
  "start": {
    "line": 59,
    "col": 23,
    "offset": 1608
  },
  "end": {
    "line": 59,
    "col": 67,
    "offset": 1652
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 195
<a name='finding-195'></a>

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

# Finding 196
<a name='finding-196'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/reflection.py`
- Start: Line 388, Column 18
- End: Line 388, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/reflection.py",
  "start": {
    "line": 388,
    "col": 18,
    "offset": 13414
  },
  "end": {
    "line": 388,
    "col": 68,
    "offset": 13464
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 197
<a name='finding-197'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/reflection.py`
- Start: Line 388, Column 18
- End: Line 388, Column 68

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/reflection.py",
  "start": {
    "line": 388,
    "col": 18,
    "offset": 13414
  },
  "end": {
    "line": 388,
    "col": 68,
    "offset": 13464
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 198
<a name='finding-198'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py`
- Start: Line 77, Column 17
- End: Line 77, Column 61

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py",
  "start": {
    "line": 77,
    "col": 17,
    "offset": 2707
  },
  "end": {
    "line": 77,
    "col": 61,
    "offset": 2751
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 199
<a name='finding-199'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py`
- Start: Line 77, Column 17
- End: Line 77, Column 61

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/playhouse/sqlcipher_ext.py",
  "start": {
    "line": 77,
    "col": 17,
    "offset": 2707
  },
  "end": {
    "line": 77,
    "col": 61,
    "offset": 2751
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 200
<a name='finding-200'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/_json.py`
- Start: Line 187, Column 5
- End: Line 189, Column 29

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/_json.py",
  "start": {
    "line": 187,
    "col": 5,
    "offset": 6767
  },
  "end": {
    "line": 189,
    "col": 29,
    "offset": 6874
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 201
<a name='finding-201'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 553, Column 9
- End: Line 553, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 553,
    "col": 9,
    "offset": 17584
  },
  "end": {
    "line": 553,
    "col": 30,
    "offset": 17605
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 202
<a name='finding-202'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 553, Column 9
- End: Line 553, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 553,
    "col": 9,
    "offset": 17584
  },
  "end": {
    "line": 553,
    "col": 30,
    "offset": 17605
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 203
<a name='finding-203'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 559, Column 9
- End: Line 559, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 559,
    "col": 9,
    "offset": 17785
  },
  "end": {
    "line": 559,
    "col": 30,
    "offset": 17806
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 204
<a name='finding-204'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 559, Column 9
- End: Line 559, Column 30

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 559,
    "col": 9,
    "offset": 17785
  },
  "end": {
    "line": 559,
    "col": 30,
    "offset": 17806
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 205
<a name='finding-205'></a>

**Rule ID:** `python.lang.security.audit.formatted-sql-query.formatted-sql-query`

**Severity:** WARNING

**Message:** Detected possible formatted SQL query. Use parameterized queries instead.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 907, Column 9
- End: Line 911, Column 5

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **references**
  - https://stackoverflow.com/questions/775296/mysql-parameterized-queries
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query
- **shortlink:** https://sg.run/EkWw

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.formatted-sql-query.formatted-sql-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 907,
    "col": 9,
    "offset": 28435
  },
  "end": {
    "line": 911,
    "col": 5,
    "offset": 28572
  },
  "extra": {
    "message": "Detected possible formatted SQL query. Use parameterized queries instead.",
    "metadata": {
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "references": [
        "https://stackoverflow.com/questions/775296/mysql-parameterized-queries"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.formatted-sql-query.formatted-sql-query",
      "shortlink": "https://sg.run/EkWw"
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

# Finding 206
<a name='finding-206'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 907, Column 9
- End: Line 911, Column 5

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 907,
    "col": 9,
    "offset": 28435
  },
  "end": {
    "line": 911,
    "col": 5,
    "offset": 28572
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 207
<a name='finding-207'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 1086, Column 9
- End: Line 1094, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 1086,
    "col": 9,
    "offset": 35125
  },
  "end": {
    "line": 1094,
    "col": 33,
    "offset": 35410
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 208
<a name='finding-208'></a>

**Rule ID:** `python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query`

**Severity:** ERROR

**Message:** Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.

## Location

- File: `venv/lib/python3.12/site-packages/psycopg2/extras.py`
- Start: Line 1111, Column 17
- End: Line 1119, Column 26

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')
- **owasp**
  - A01:2017 - Injection
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql
  - https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm
  - https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column
- **category:** security
- **technology**
  - sqlalchemy
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - SQL Injection
- **source:** https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query
- **shortlink:** https://sg.run/2b1L

## Raw Finding JSON

```json
{
  "check_id": "python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
  "path": "venv/lib/python3.12/site-packages/psycopg2/extras.py",
  "start": {
    "line": 1111,
    "col": 17,
    "offset": 36143
  },
  "end": {
    "line": 1119,
    "col": 26,
    "offset": 36428
  },
  "extra": {
    "message": "Avoiding SQL string concatenation: untrusted input concatenated with raw SQL query can result in SQL Injection. In order to execute raw query safely, prepared statement should be used. SQLAlchemy provides TextualSQL to easily used prepared statement with named parameters. For complex SQL composition, use SQL Expression Language or Schema Definition Language. In most cases, SQLAlchemy ORM will be a better option.",
    "metadata": {
      "cwe": [
        "CWE-89: Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection')"
      ],
      "owasp": [
        "A01:2017 - Injection",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-textual-sql",
        "https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_quick_guide.htm",
        "https://docs.sqlalchemy.org/en/14/core/tutorial.html#using-more-specific-text-with-table-expression-literal-column-and-expression-column"
      ],
      "category": "security",
      "technology": [
        "sqlalchemy"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "SQL Injection"
      ],
      "source": "https://semgrep.dev/r/python.sqlalchemy.security.sqlalchemy-execute-raw-query.sqlalchemy-execute-raw-query",
      "shortlink": "https://sg.run/2b1L"
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

# Finding 209
<a name='finding-209'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/__init__.py`
- Start: Line 442, Column 18
- End: Line 442, Column 65

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pydantic/__init__.py",
  "start": {
    "line": 442,
    "col": 18,
    "offset": 15299
  },
  "end": {
    "line": 442,
    "col": 65,
    "offset": 15346
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 210
<a name='finding-210'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/__init__.py`
- Start: Line 446, Column 18
- End: Line 446, Column 61

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pydantic/__init__.py",
  "start": {
    "line": 446,
    "col": 18,
    "offset": 15434
  },
  "end": {
    "line": 446,
    "col": 61,
    "offset": 15477
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 211
<a name='finding-211'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/_internal/_validators.py`
- Start: Line 110, Column 18
- End: Line 110, Column 44

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pydantic/_internal/_validators.py",
  "start": {
    "line": 110,
    "col": 18,
    "offset": 4640
  },
  "end": {
    "line": 110,
    "col": 44,
    "offset": 4666
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 212
<a name='finding-212'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/deprecated/parse.py`
- Start: Line 54, Column 16
- End: Line 54, Column 32

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pydantic/deprecated/parse.py",
  "start": {
    "line": 54,
    "col": 16,
    "offset": 1656
  },
  "end": {
    "line": 54,
    "col": 32,
    "offset": 1672
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 213
<a name='finding-213'></a>

**Rule ID:** `python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage`

**Severity:** INFO

**Message:** Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/v1/generics.py`
- Start: Line 400, Column 9
- End: Line 400, Column 59

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **category:** security
- **references**
  - https://docs.python.org/3/library/typing.html#typing.get_type_hints
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage
- **shortlink:** https://sg.run/8R6J

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
  "path": "venv/lib/python3.12/site-packages/pydantic/v1/generics.py",
  "start": {
    "line": 400,
    "col": 9,
    "offset": 17778
  },
  "end": {
    "line": 400,
    "col": 59,
    "offset": 17828
  },
  "extra": {
    "message": "Annotations passed to `typing.get_type_hints` are evaluated in `globals` and `locals` namespaces. Make sure that no arbitrary value can be written as the annotation and passed to `typing.get_type_hints` function.",
    "metadata": {
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "category": "security",
      "references": [
        "https://docs.python.org/3/library/typing.html#typing.get_type_hints"
      ],
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dangerous-annotations-usage.dangerous-annotations-usage",
      "shortlink": "https://sg.run/8R6J"
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

# Finding 214
<a name='finding-214'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/v1/parse.py`
- Start: Line 42, Column 16
- End: Line 42, Column 32

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/pydantic/v1/parse.py",
  "start": {
    "line": 42,
    "col": 16,
    "offset": 1129
  },
  "end": {
    "line": 42,
    "col": 32,
    "offset": 1145
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 215
<a name='finding-215'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/v1/utils.py`
- Start: Line 134, Column 14
- End: Line 134, Column 40

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pydantic/v1/utils.py",
  "start": {
    "line": 134,
    "col": 14,
    "offset": 3367
  },
  "end": {
    "line": 134,
    "col": 40,
    "offset": 3393
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 216
<a name='finding-216'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/pydantic/v1/version.py`
- Start: Line 25, Column 13
- End: Line 25, Column 47

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/pydantic/v1/version.py",
  "start": {
    "line": 25,
    "col": 13,
    "offset": 537
  },
  "end": {
    "line": 25,
    "col": 47,
    "offset": 571
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 217
<a name='finding-217'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/formatters/__init__.py`
- Start: Line 103, Column 13
- End: Line 103, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pygments/formatters/__init__.py",
  "start": {
    "line": 103,
    "col": 13,
    "offset": 3320
  },
  "end": {
    "line": 103,
    "col": 45,
    "offset": 3352
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 218
<a name='finding-218'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/lexers/__init__.py`
- Start: Line 154, Column 13
- End: Line 154, Column 45

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/pygments/lexers/__init__.py",
  "start": {
    "line": 154,
    "col": 13,
    "offset": 4937
  },
  "end": {
    "line": 154,
    "col": 45,
    "offset": 4969
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 219
<a name='finding-219'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.urllib.insecure-urlopen.insecure-urlopen`

**Severity:** WARNING

**Message:** Detected 'urllib.urlopen()' using 'http://'. This request will not be encrypted. Use 'https://' instead.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py`
- Start: Line 225, Column 13
- End: Line 225, Column 50

## Proof of Concept

```
requires login
```

## Suggested Fix

```
urlopen('https://www.lua.org/manual/')
```

## Metadata

- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **references**
  - https://docs.python.org/3/library/urllib.request.html#urllib.request.urlopen
- **category:** security
- **technology**
  - urllib
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.urllib.insecure-urlopen.insecure-urlopen
- **shortlink:** https://sg.run/oxB9

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.urllib.insecure-urlopen.insecure-urlopen",
  "path": "venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py",
  "start": {
    "line": 225,
    "col": 13,
    "offset": 6080
  },
  "end": {
    "line": 225,
    "col": 50,
    "offset": 6117
  },
  "extra": {
    "message": "Detected 'urllib.urlopen()' using 'http://'. This request will not be encrypted. Use 'https://' instead.",
    "fix": "urlopen('https://www.lua.org/manual/')",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "references": [
        "https://docs.python.org/3/library/urllib.request.html#urllib.request.urlopen"
      ],
      "category": "security",
      "technology": [
        "urllib"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.urllib.insecure-urlopen.insecure-urlopen",
      "shortlink": "https://sg.run/oxB9"
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

# Finding 220
<a name='finding-220'></a>

**Rule ID:** `python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected`

**Severity:** WARNING

**Message:** Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py`
- Start: Line 233, Column 13
- End: Line 233, Column 61

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-939: Improper Authorization in Handler for Custom URL Scheme
- **owasp:** A01:2017 - Injection
- **source-rule-url:** https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163
- **bandit-code:** B310
- **asvs**
  - control_id: 5.2.4 Dynamic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://cwe.mitre.org/data/definitions/939.html
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected
- **shortlink:** https://sg.run/dKZZ

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
  "path": "venv/lib/python3.12/site-packages/pygments/lexers/_lua_builtins.py",
  "start": {
    "line": 233,
    "col": 13,
    "offset": 6370
  },
  "end": {
    "line": 233,
    "col": 61,
    "offset": 6418
  },
  "extra": {
    "message": "Detected a dynamic value being used with urllib. urllib supports 'file://' schemes, so a dynamic value controlled by a malicious actor may allow them to read arbitrary files. Audit uses of urllib calls to ensure user data cannot control the URLs, or consider using the 'requests' library instead.",
    "metadata": {
      "cwe": [
        "CWE-939: Improper Authorization in Handler for Custom URL Scheme"
      ],
      "owasp": "A01:2017 - Injection",
      "source-rule-url": "https://github.com/PyCQA/bandit/blob/b1411bfb43795d3ffd268bef17a839dee954c2b1/bandit/blacklists/calls.py#L163",
      "bandit-code": "B310",
      "asvs": {
        "control_id": "5.2.4 Dynamic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://cwe.mitre.org/data/definitions/939.html"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.dynamic-urllib-use-detected.dynamic-urllib-use-detected",
      "shortlink": "https://sg.run/dKZZ"
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

# Finding 221
<a name='finding-221'></a>

**Rule ID:** `trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal`

**Severity:** ERROR

**Message:** Possible path traversal through `tarfile.open($PATH).extractall()` if the source tar is controlled by an attacker

## Location

- File: `venv/lib/python3.12/site-packages/pygments/lexers/_php_builtins.py`
- Start: Line 3300, Column 14
- End: Line 3304, Column 33

## Proof of Concept

```
requires login
```

## Metadata

- **category:** security
- **cwe:** CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')
- **subcategory**
  - vuln
- **confidence:** MEDIUM
- **likelihood:** MEDIUM
- **impact:** MEDIUM
- **technology**
  - --no-technology--
- **description:** Potential path traversal in call to `extractall` for a `tarfile`
- **references**
  - https://docs.python.org/3/library/tarfile.html#tarfile.TarFile.extractall
- **license:** AGPL-3.0 license
- **vulnerability_class**
  - Path Traversal
- **source:** https://semgrep.dev/r/trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal
- **shortlink:** https://sg.run/2RLD

## Raw Finding JSON

```json
{
  "check_id": "trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal",
  "path": "venv/lib/python3.12/site-packages/pygments/lexers/_php_builtins.py",
  "start": {
    "line": 3300,
    "col": 14,
    "offset": 107043
  },
  "end": {
    "line": 3304,
    "col": 33,
    "offset": 107235
  },
  "extra": {
    "message": "Possible path traversal through `tarfile.open($PATH).extractall()` if the source tar is controlled by an attacker",
    "metadata": {
      "category": "security",
      "cwe": "CWE-22: Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')",
      "subcategory": [
        "vuln"
      ],
      "confidence": "MEDIUM",
      "likelihood": "MEDIUM",
      "impact": "MEDIUM",
      "technology": [
        "--no-technology--"
      ],
      "description": "Potential path traversal in call to `extractall` for a `tarfile`",
      "references": [
        "https://docs.python.org/3/library/tarfile.html#tarfile.TarFile.extractall"
      ],
      "license": "AGPL-3.0 license",
      "vulnerability_class": [
        "Path Traversal"
      ],
      "source": "https://semgrep.dev/r/trailofbits.python.tarfile-extractall-traversal.tarfile-extractall-traversal",
      "shortlink": "https://sg.run/2RLD"
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

# Finding 222
<a name='finding-222'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/unistring.py`
- Start: Line 83, Column 20
- End: Line 83, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pygments/unistring.py",
  "start": {
    "line": 83,
    "col": 20,
    "offset": 61128
  },
  "end": {
    "line": 83,
    "col": 34,
    "offset": 61142
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 223
<a name='finding-223'></a>

**Rule ID:** `python.lang.security.dangerous-globals-use.dangerous-globals-use`

**Severity:** WARNING

**Message:** Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.

## Location

- File: `venv/lib/python3.12/site-packages/pygments/unistring.py`
- Start: Line 90, Column 20
- End: Line 90, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **references**
  - https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use
- **shortlink:** https://sg.run/jNzn

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.dangerous-globals-use.dangerous-globals-use",
  "path": "venv/lib/python3.12/site-packages/pygments/unistring.py",
  "start": {
    "line": 90,
    "col": 20,
    "offset": 61274
  },
  "end": {
    "line": 90,
    "col": 34,
    "offset": 61288
  },
  "extra": {
    "message": "Found non static data as an index to 'globals()'. This is extremely dangerous because it allows an attacker to execute arbitrary code on the system. Refactor your code not to use 'globals()'.",
    "metadata": {
      "cwe": [
        "CWE-96: Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://github.com/mpirnat/lets-be-bad-guys/blob/d92768fb3ade32956abd53bd6bb06e19d634a084/badguys/vulnerable/views.py#L181-L186"
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
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.dangerous-globals-use.dangerous-globals-use",
      "shortlink": "https://sg.run/jNzn"
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

# Finding 224
<a name='finding-224'></a>

**Rule ID:** `generic.secrets.security.detected-jwt-token.detected-jwt-token`

**Severity:** ERROR

**Message:** JWT token detected

## Location

- File: `venv/lib/python3.12/site-packages/pyjwt-2.13.0.dist-info/METADATA`
- Start: Line 76, Column 5
- End: Line 76, Column 67

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py
- **category:** security
- **technology**
  - secrets
  - jwt
- **confidence:** LOW
- **references**
  - https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/
- **cwe**
  - CWE-321: Use of Hard-coded Cryptographic Key
- **owasp**
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token
- **shortlink:** https://sg.run/05N5

## Raw Finding JSON

```json
{
  "check_id": "generic.secrets.security.detected-jwt-token.detected-jwt-token",
  "path": "venv/lib/python3.12/site-packages/pyjwt-2.13.0.dist-info/METADATA",
  "start": {
    "line": 76,
    "col": 5,
    "offset": 3049
  },
  "end": {
    "line": 76,
    "col": 67,
    "offset": 3111
  },
  "extra": {
    "message": "JWT token detected",
    "metadata": {
      "source-rule-url": "https://github.com/Yelp/detect-secrets/blob/master/detect_secrets/plugins/jwt.py",
      "category": "security",
      "technology": [
        "secrets",
        "jwt"
      ],
      "confidence": "LOW",
      "references": [
        "https://semgrep.dev/blog/2020/hardcoded-secrets-unverified-tokens-and-other-common-jwt-mistakes/"
      ],
      "cwe": [
        "CWE-321: Use of Hard-coded Cryptographic Key"
      ],
      "owasp": [
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/generic.secrets.security.detected-jwt-token.detected-jwt-token",
      "shortlink": "https://sg.run/05N5"
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

# Finding 225
<a name='finding-225'></a>

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

# Finding 226
<a name='finding-226'></a>

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

# Finding 227
<a name='finding-227'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/requests/compat.py`
- Start: Line 24, Column 27
- End: Line 24, Column 55

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/requests/compat.py",
  "start": {
    "line": 24,
    "col": 27,
    "offset": 525
  },
  "end": {
    "line": 24,
    "col": 55,
    "offset": 553
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 228
<a name='finding-228'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/rich/_unicode_data/__init__.py`
- Start: Line 90, Column 14
- End: Line 90, Column 62

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/rich/_unicode_data/__init__.py",
  "start": {
    "line": 90,
    "col": 14,
    "offset": 2475
  },
  "end": {
    "line": 90,
    "col": 62,
    "offset": 2523
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 229
<a name='finding-229'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/rich/style.py`
- Start: Line 200, Column 48
- End: Line 200, Column 59

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/rich/style.py",
  "start": {
    "line": 200,
    "col": 48,
    "offset": 6418
  },
  "end": {
    "line": 200,
    "col": 59,
    "offset": 6429
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 230
<a name='finding-230'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/rich/style.py`
- Start: Line 251, Column 23
- End: Line 251, Column 34

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/rich/style.py",
  "start": {
    "line": 251,
    "col": 23,
    "offset": 8190
  },
  "end": {
    "line": 251,
    "col": 34,
    "offset": 8201
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 231
<a name='finding-231'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/rich/style.py`
- Start: Line 475, Column 67
- End: Line 475, Column 84

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/rich/style.py",
  "start": {
    "line": 475,
    "col": 67,
    "offset": 16259
  },
  "end": {
    "line": 475,
    "col": 84,
    "offset": 16276
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 232
<a name='finding-232'></a>

**Rule ID:** `python.lang.security.deserialization.pickle.avoid-pickle`

**Severity:** WARNING

**Message:** Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.

## Location

- File: `venv/lib/python3.12/site-packages/rich/style.py`
- Start: Line 751, Column 31
- End: Line 751, Column 65

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A08:2017 - Insecure Deserialization
  - A08:2021 - Software and Data Integrity Failures
  - A08:2025 - Software or Data Integrity Failures
- **cwe**
  - CWE-502: Deserialization of Untrusted Data
- **references**
  - https://docs.python.org/3/library/pickle.html
- **category:** security
- **technology**
  - python
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Insecure Deserialization 
- **source:** https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle
- **shortlink:** https://sg.run/OPwB

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.deserialization.pickle.avoid-pickle",
  "path": "venv/lib/python3.12/site-packages/rich/style.py",
  "start": {
    "line": 751,
    "col": 31,
    "offset": 25845
  },
  "end": {
    "line": 751,
    "col": 65,
    "offset": 25879
  },
  "extra": {
    "message": "Avoid using `pickle`, which is known to lead to code execution vulnerabilities. When unpickling, the serialized data could be manipulated to run arbitrary code. Instead, consider serializing the relevant data as JSON or a similar text-based serialization format.",
    "metadata": {
      "owasp": [
        "A08:2017 - Insecure Deserialization",
        "A08:2021 - Software and Data Integrity Failures",
        "A08:2025 - Software or Data Integrity Failures"
      ],
      "cwe": [
        "CWE-502: Deserialization of Untrusted Data"
      ],
      "references": [
        "https://docs.python.org/3/library/pickle.html"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Insecure Deserialization "
      ],
      "source": "https://semgrep.dev/r/python.lang.security.deserialization.pickle.avoid-pickle",
      "shortlink": "https://sg.run/OPwB"
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

# Finding 233
<a name='finding-233'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/ruamel/yaml/main.py`
- Start: Line 87, Column 34
- End: Line 87, Column 58

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/ruamel/yaml/main.py",
  "start": {
    "line": 87,
    "col": 34,
    "offset": 2821
  },
  "end": {
    "line": 87,
    "col": 58,
    "offset": 2845
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 234
<a name='finding-234'></a>

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

# Finding 235
<a name='finding-235'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/semgrep/console_scripts/entrypoint.py`
- Start: Line 30, Column 1
- End: Line 30, Column 27

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/semgrep/console_scripts/entrypoint.py",
  "start": {
    "line": 30,
    "col": 1,
    "offset": 1693
  },
  "end": {
    "line": 30,
    "col": 27,
    "offset": 1719
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 236
<a name='finding-236'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/semgrep/semgrep_core.py`
- Start: Line 13, Column 1
- End: Line 13, Column 27

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/semgrep/semgrep_core.py",
  "start": {
    "line": 13,
    "col": 1,
    "offset": 467
  },
  "end": {
    "line": 13,
    "col": 27,
    "offset": 493
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 237
<a name='finding-237'></a>

**Rule ID:** `python.flask.security.xss.audit.direct-use-of-jinja2.direct-use-of-jinja2`

**Severity:** WARNING

**Message:** Detected direct use of jinja2. If not done properly, this may bypass HTML escaping which opens up the application to cross-site scripting (XSS) vulnerabilities. Prefer using the Flask method 'render_template()' and templates with a '.html' extension in order to prevent XSS.

## Location

- File: `venv/lib/python3.12/site-packages/starlette/templating.py`
- Start: Line 95, Column 24
- End: Line 95, Column 96

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
- **references**
  - https://jinja.palletsprojects.com/en/2.11.x/api/#basics
- **category:** security
- **technology**
  - flask
- **cwe2022-top25:** True
- **cwe2021-top25:** True
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cross-Site-Scripting (XSS)
- **source:** https://semgrep.dev/r/python.flask.security.xss.audit.direct-use-of-jinja2.direct-use-of-jinja2
- **shortlink:** https://sg.run/RoKe

## Raw Finding JSON

```json
{
  "check_id": "python.flask.security.xss.audit.direct-use-of-jinja2.direct-use-of-jinja2",
  "path": "venv/lib/python3.12/site-packages/starlette/templating.py",
  "start": {
    "line": 95,
    "col": 24,
    "offset": 3374
  },
  "end": {
    "line": 95,
    "col": 96,
    "offset": 3446
  },
  "extra": {
    "message": "Detected direct use of jinja2. If not done properly, this may bypass HTML escaping which opens up the application to cross-site scripting (XSS) vulnerabilities. Prefer using the Flask method 'render_template()' and templates with a '.html' extension in order to prevent XSS.",
    "metadata": {
      "cwe": [
        "CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')"
      ],
      "owasp": [
        "A07:2017 - Cross-Site Scripting (XSS)",
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "references": [
        "https://jinja.palletsprojects.com/en/2.11.x/api/#basics"
      ],
      "category": "security",
      "technology": [
        "flask"
      ],
      "cwe2022-top25": true,
      "cwe2021-top25": true,
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cross-Site-Scripting (XSS)"
      ],
      "source": "https://semgrep.dev/r/python.flask.security.xss.audit.direct-use-of-jinja2.direct-use-of-jinja2",
      "shortlink": "https://sg.run/RoKe"
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

# Finding 238
<a name='finding-238'></a>

**Rule ID:** `javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket`

**Severity:** ERROR

**Message:** Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.

## Location

- File: `venv/lib/python3.12/site-packages/starlette/testclient.py`
- Start: Line 661, Column 24
- End: Line 661, Column 29

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **asvs**
  - control_id: 13.5.1 Insecure WebSocket
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements
  - section: V13: API and Web Service Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - regex
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket
- **shortlink:** https://sg.run/GWyz

## Raw Finding JSON

```json
{
  "check_id": "javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
  "path": "venv/lib/python3.12/site-packages/starlette/testclient.py",
  "start": {
    "line": 661,
    "col": 24,
    "offset": 25152
  },
  "end": {
    "line": 661,
    "col": 29,
    "offset": 25157
  },
  "extra": {
    "message": "Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.",
    "metadata": {
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "asvs": {
        "control_id": "13.5.1 Insecure WebSocket",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements",
        "section": "V13: API and Web Service Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "regex"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
      "shortlink": "https://sg.run/GWyz"
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

# Finding 239
<a name='finding-239'></a>

**Rule ID:** `python.lang.security.audit.eval-detected.eval-detected`

**Severity:** WARNING

**Message:** Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/typing_extensions.py`
- Start: Line 4172, Column 54
- End: Line 4172, Column 82

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected
- **shortlink:** https://sg.run/ZvrD

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.eval-detected.eval-detected",
  "path": "venv/lib/python3.12/site-packages/typing_extensions.py",
  "start": {
    "line": 4172,
    "col": 54,
    "offset": 156163
  },
  "end": {
    "line": 4172,
    "col": 82,
    "offset": 156191
  },
  "extra": {
    "message": "Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected",
      "shortlink": "https://sg.run/ZvrD"
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

# Finding 240
<a name='finding-240'></a>

**Rule ID:** `python.lang.security.audit.eval-detected.eval-detected`

**Severity:** WARNING

**Message:** Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/typing_extensions.py`
- Start: Line 4254, Column 21
- End: Line 4254, Column 48

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected
- **shortlink:** https://sg.run/ZvrD

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.eval-detected.eval-detected",
  "path": "venv/lib/python3.12/site-packages/typing_extensions.py",
  "start": {
    "line": 4254,
    "col": 21,
    "offset": 159369
  },
  "end": {
    "line": 4254,
    "col": 48,
    "offset": 159396
  },
  "extra": {
    "message": "Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/blacklists/blacklist_calls.html#b307-eval",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.eval-detected.eval-detected",
      "shortlink": "https://sg.run/ZvrD"
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

# Finding 241
<a name='finding-241'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py`
- Start: Line 101, Column 5
- End: Line 101, Column 39

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py",
  "start": {
    "line": 101,
    "col": 5,
    "offset": 2861
  },
  "end": {
    "line": 101,
    "col": 39,
    "offset": 2895
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 242
<a name='finding-242'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py`
- Start: Line 133, Column 5
- End: Line 133, Column 39

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/typing_inspection/typing_objects.py",
  "start": {
    "line": 133,
    "col": 5,
    "offset": 4247
  },
  "end": {
    "line": 133,
    "col": 39,
    "offset": 4281
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 243
<a name='finding-243'></a>

**Rule ID:** `python.lang.compatibility.python37.python37-compatibility-importlib2`

**Severity:** ERROR

**Message:** Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.

## Location

- File: `venv/lib/python3.12/site-packages/urllib3/contrib/emscripten/fetch.py`
- Start: Line 42, Column 1
- End: Line 42, Column 38

## Proof of Concept

```
requires login
```

## Metadata

- **category:** compatibility
- **technology**
  - python
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **source:** https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2
- **shortlink:** https://sg.run/eL3y

## Raw Finding JSON

```json
{
  "check_id": "python.lang.compatibility.python37.python37-compatibility-importlib2",
  "path": "venv/lib/python3.12/site-packages/urllib3/contrib/emscripten/fetch.py",
  "start": {
    "line": 42,
    "col": 1,
    "offset": 1862
  },
  "end": {
    "line": 42,
    "col": 38,
    "offset": 1899
  },
  "extra": {
    "message": "Found 'importlib.resources', which is a module only available on Python 3.7+. This does not work in lower versions, and therefore is not backwards compatible. Use importlib_resources instead for older Python versions.",
    "metadata": {
      "category": "compatibility",
      "technology": [
        "python"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "source": "https://semgrep.dev/r/python.lang.compatibility.python37.python37-compatibility-importlib2",
      "shortlink": "https://sg.run/eL3y"
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

# Finding 244
<a name='finding-244'></a>

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

# Finding 245
<a name='finding-245'></a>

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

# Finding 246
<a name='finding-246'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers`

**Severity:** WARNING

**Message:** The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.

## Location

- File: `venv/lib/python3.12/site-packages/urllib3/util/ssl_.py`
- Start: Line 311, Column 9
- End: Line 311, Column 37

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
  - CWE-326: Inadequate Encryption Strength
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://docs.python.org/3/library/ssl.html#cipher-selection
  - https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers
- **category:** security
- **technology**
  - ssl
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers
- **shortlink:** https://sg.run/0Q0v

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
  "path": "venv/lib/python3.12/site-packages/urllib3/util/ssl_.py",
  "start": {
    "line": 311,
    "col": 9,
    "offset": 11781
  },
  "end": {
    "line": 311,
    "col": 37,
    "offset": 11809
  },
  "extra": {
    "message": "The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://docs.python.org/3/library/ssl.html#cipher-selection",
        "https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers"
      ],
      "category": "security",
      "technology": [
        "ssl"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
      "shortlink": "https://sg.run/0Q0v"
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

# Finding 247
<a name='finding-247'></a>

**Rule ID:** `python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers`

**Severity:** WARNING

**Message:** The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.

## Location

- File: `venv/lib/python3.12/site-packages/uvicorn/config.py`
- Start: Line 134, Column 9
- End: Line 134, Column 33

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
  - CWE-326: Inadequate Encryption Strength
- **asvs**
  - control_id: 9.1.3 Weak TLS
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements
  - section: V9 Communications Verification Requirements
  - version: 4
- **references**
  - https://docs.python.org/3/library/ssl.html#cipher-selection
  - https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers
- **category:** security
- **technology**
  - ssl
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Cryptographic Issues
- **source:** https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers
- **shortlink:** https://sg.run/0Q0v

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
  "path": "venv/lib/python3.12/site-packages/uvicorn/config.py",
  "start": {
    "line": 134,
    "col": 9,
    "offset": 4611
  },
  "end": {
    "line": 134,
    "col": 33,
    "offset": 4635
  },
  "extra": {
    "message": "The 'ssl' module disables insecure cipher suites by default. Therefore, use of 'set_ciphers()' should only be used when you have very specialized requirements. Otherwise, you risk lowering the security of the SSL channel.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "cwe": [
        "CWE-326: Inadequate Encryption Strength"
      ],
      "asvs": {
        "control_id": "9.1.3 Weak TLS",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x17-V9-Communications.md#v91-client-communications-security-requirements",
        "section": "V9 Communications Verification Requirements",
        "version": "4"
      },
      "references": [
        "https://docs.python.org/3/library/ssl.html#cipher-selection",
        "https://docs.python.org/3/library/ssl.html#ssl.SSLContext.set_ciphers"
      ],
      "category": "security",
      "technology": [
        "ssl"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Cryptographic Issues"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.insecure-transport.ssl.no-set-ciphers.no-set-ciphers",
      "shortlink": "https://sg.run/0Q0v"
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

# Finding 248
<a name='finding-248'></a>

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

# Finding 249
<a name='finding-249'></a>

**Rule ID:** `python.lang.security.audit.non-literal-import.non-literal-import`

**Severity:** WARNING

**Message:** Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.

## Location

- File: `venv/lib/python3.12/site-packages/uvicorn/importer.py`
- Start: Line 19, Column 18
- End: Line 19, Column 53

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A01:2021 - Broken Access Control
  - A01:2025 - Broken Access Control
- **cwe**
  - CWE-706: Use of Incorrectly-Resolved Name or Reference
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A01_2021-Broken_Access_Control
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authorization
- **source:** https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import
- **shortlink:** https://sg.run/y6Jk

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.non-literal-import.non-literal-import",
  "path": "venv/lib/python3.12/site-packages/uvicorn/importer.py",
  "start": {
    "line": 19,
    "col": 18,
    "offset": 498
  },
  "end": {
    "line": 19,
    "col": 53,
    "offset": 533
  },
  "extra": {
    "message": "Untrusted user input in `importlib.import_module()` function allows an attacker to load arbitrary code. Avoid dynamic values in `importlib.import_module()` or use a whitelist to prevent running untrusted code.",
    "metadata": {
      "owasp": [
        "A01:2021 - Broken Access Control",
        "A01:2025 - Broken Access Control"
      ],
      "cwe": [
        "CWE-706: Use of Incorrectly-Resolved Name or Reference"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A01_2021-Broken_Access_Control"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authorization"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.non-literal-import.non-literal-import",
      "shortlink": "https://sg.run/y6Jk"
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

# Finding 250
<a name='finding-250'></a>

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

# Finding 251
<a name='finding-251'></a>

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

# Finding 252
<a name='finding-252'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/debug/console.py`
- Start: Line 177, Column 13
- End: Line 177, Column 36

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/werkzeug/debug/console.py",
  "start": {
    "line": 177,
    "col": 13,
    "offset": 4830
  },
  "end": {
    "line": 177,
    "col": 36,
    "offset": 4853
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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

# Finding 253
<a name='finding-253'></a>

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

# Finding 254
<a name='finding-254'></a>

**Rule ID:** `python.lang.security.audit.httpsconnection-detected.httpsconnection-detected`

**Severity:** WARNING

**Message:** The HTTPSConnection API has changed frequently with minor releases of Python. Ensure you are using the API for your version of Python securely. For example, Python 3 versions prior to 3.4.3 will not verify SSL certificates by default. See https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection for more information.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/middleware/http_proxy.py`
- Start: Line 151, Column 27
- End: Line 156, Column 22

## Proof of Concept

```
requires login
```

## Metadata

- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A07:2021 - Identification and Authentication Failures
  - A07:2025 - Authentication Failures
- **cwe**
  - CWE-295: Improper Certificate Validation
- **references**
  - https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection
- **category:** security
- **technology**
  - python
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** LOW
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Improper Authentication
- **source:** https://semgrep.dev/r/python.lang.security.audit.httpsconnection-detected.httpsconnection-detected
- **shortlink:** https://sg.run/8yby

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.httpsconnection-detected.httpsconnection-detected",
  "path": "venv/lib/python3.12/site-packages/werkzeug/middleware/http_proxy.py",
  "start": {
    "line": 151,
    "col": 27,
    "offset": 5144
  },
  "end": {
    "line": 156,
    "col": 22,
    "offset": 5362
  },
  "extra": {
    "message": "The HTTPSConnection API has changed frequently with minor releases of Python. Ensure you are using the API for your version of Python securely. For example, Python 3 versions prior to 3.4.3 will not verify SSL certificates by default. See https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection for more information.",
    "metadata": {
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A07:2021 - Identification and Authentication Failures",
        "A07:2025 - Authentication Failures"
      ],
      "cwe": [
        "CWE-295: Improper Certificate Validation"
      ],
      "references": [
        "https://docs.python.org/3/library/http.client.html#http.client.HTTPSConnection"
      ],
      "category": "security",
      "technology": [
        "python"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "LOW",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Improper Authentication"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.httpsconnection-detected.httpsconnection-detected",
      "shortlink": "https://sg.run/8yby"
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

# Finding 255
<a name='finding-255'></a>

**Rule ID:** `javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket`

**Severity:** ERROR

**Message:** Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/routing/rules.py`
- Start: Line 427, Column 65
- End: Line 427, Column 70

## Proof of Concept

```
requires login
```

## Metadata

- **cwe**
  - CWE-319: Cleartext Transmission of Sensitive Information
- **asvs**
  - control_id: 13.5.1 Insecure WebSocket
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements
  - section: V13: API and Web Service Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - regex
- **owasp**
  - A03:2017 - Sensitive Data Exposure
  - A02:2021 - Cryptographic Failures
  - A04:2025 - Cryptographic Failures
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** MEDIUM
- **confidence:** LOW
- **references**
  - https://owasp.org/Top10/A02_2021-Cryptographic_Failures
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Mishandled Sensitive Information
- **source:** https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket
- **shortlink:** https://sg.run/GWyz

## Raw Finding JSON

```json
{
  "check_id": "javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
  "path": "venv/lib/python3.12/site-packages/werkzeug/routing/rules.py",
  "start": {
    "line": 427,
    "col": 65,
    "offset": 14632
  },
  "end": {
    "line": 427,
    "col": 70,
    "offset": 14637
  },
  "extra": {
    "message": "Insecure WebSocket Detected. WebSocket Secure (wss) should be used for all WebSocket connections.",
    "metadata": {
      "cwe": [
        "CWE-319: Cleartext Transmission of Sensitive Information"
      ],
      "asvs": {
        "control_id": "13.5.1 Insecure WebSocket",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x21-V13-API.md#v135-websocket-security-requirements",
        "section": "V13: API and Web Service Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "regex"
      ],
      "owasp": [
        "A03:2017 - Sensitive Data Exposure",
        "A02:2021 - Cryptographic Failures",
        "A04:2025 - Cryptographic Failures"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "MEDIUM",
      "confidence": "LOW",
      "references": [
        "https://owasp.org/Top10/A02_2021-Cryptographic_Failures"
      ],
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Mishandled Sensitive Information"
      ],
      "source": "https://semgrep.dev/r/javascript.lang.security.detect-insecure-websocket.detect-insecure-websocket",
      "shortlink": "https://sg.run/GWyz"
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

# Finding 256
<a name='finding-256'></a>

**Rule ID:** `python.lang.security.audit.exec-detected.exec-detected`

**Severity:** WARNING

**Message:** Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.

## Location

- File: `venv/lib/python3.12/site-packages/werkzeug/routing/rules.py`
- Start: Line 727, Column 9
- End: Line 727, Column 32

## Proof of Concept

```
requires login
```

## Metadata

- **source-rule-url:** https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html
- **cwe**
  - CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')
- **owasp**
  - A03:2021 - Injection
  - A05:2025 - Injection
- **asvs**
  - control_id: 5.2.4 Dyanmic Code Execution Features
  - control_url: https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements
  - section: V5: Validation, Sanitization and Encoding Verification Requirements
  - version: 4
- **category:** security
- **technology**
  - python
- **references**
  - https://owasp.org/Top10/A03_2021-Injection
- **subcategory**
  - audit
- **likelihood:** LOW
- **impact:** HIGH
- **confidence:** LOW
- **license:** Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license
- **vulnerability_class**
  - Code Injection
- **source:** https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected
- **shortlink:** https://sg.run/ndRX

## Raw Finding JSON

```json
{
  "check_id": "python.lang.security.audit.exec-detected.exec-detected",
  "path": "venv/lib/python3.12/site-packages/werkzeug/routing/rules.py",
  "start": {
    "line": 727,
    "col": 9,
    "offset": 25217
  },
  "end": {
    "line": 727,
    "col": 32,
    "offset": 25240
  },
  "extra": {
    "message": "Detected the use of exec(). exec() can be dangerous if used to evaluate dynamic content. If this content can be input from outside the program, this may be a code injection vulnerability. Ensure evaluated content is not definable by external sources.",
    "metadata": {
      "source-rule-url": "https://bandit.readthedocs.io/en/latest/plugins/b102_exec_used.html",
      "cwe": [
        "CWE-95: Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')"
      ],
      "owasp": [
        "A03:2021 - Injection",
        "A05:2025 - Injection"
      ],
      "asvs": {
        "control_id": "5.2.4 Dyanmic Code Execution Features",
        "control_url": "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x13-V5-Validation-Sanitization-Encoding.md#v52-sanitization-and-sandboxing-requirements",
        "section": "V5: Validation, Sanitization and Encoding Verification Requirements",
        "version": "4"
      },
      "category": "security",
      "technology": [
        "python"
      ],
      "references": [
        "https://owasp.org/Top10/A03_2021-Injection"
      ],
      "subcategory": [
        "audit"
      ],
      "likelihood": "LOW",
      "impact": "HIGH",
      "confidence": "LOW",
      "license": "Semgrep Rules License v1.0. For more details, visit semgrep.dev/legal/rules-license",
      "vulnerability_class": [
        "Code Injection"
      ],
      "source": "https://semgrep.dev/r/python.lang.security.audit.exec-detected.exec-detected",
      "shortlink": "https://sg.run/ndRX"
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
