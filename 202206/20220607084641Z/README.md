# Learning plan 2022

It has been a busy year thus far, but now, in June/2022 I decided to create some
kind of plan for structured and guided learning, so here it goes:

## Things to learn
In order of priority

Must:
- Technical writing
- Authentication protocols (OIDC, SAML, etc)
- Advanced bash scripting
- Advanced GO

Bonus:
- Security as a Mindset
- Communicating with influence
- Basic statistics
- Actual TDD

Why learn technical writing?

It is a fundamental part of SREs and DevOps workers to document their how the
things they built work, it will also be useful in order to document all the
other learning topics throughout the year, rather than just have bullet points
and notes, learning to properly write technical content will help me in the long
run in a lot of ways.

Authentication protocols

They are a fundamental part of our day-to-day, and are very present in a lot of
dicussion, just superficial knowledge has been sufficient to me so far, but
recently I've found the need to know the more in-depth details about how it
works, specially OIDC, for this it might be useful to setup a few labs using
keycloak

Why bash instead of other language?

Bash is present in every unix OS, and is the language mostly used for
automation, learning better bash will also improve my day-to-day work in the
terminal, worth to take a look in `man bash`

Why GO? how to tackle it?

GO is becoming a paramount language in devops, I already know the basics, but to
get a grasp of advanced concepts and uses I see little alternative right now
other than becoming contributor to a big project, so that is the path I'll try
to take

Security is often overlooked

Security is often overlooked at development time and becomes a blocker when it
comes time to actually deploy some system to production, when it starts to fail
simple security checks or pentesters find a lot of holes, so to consider
security from the gecko in your development cycle is paramount, consider the
proper tool for each job, eg. use `tfsec` when doing terraform, try to use
`gitleaks` as a pre-commit hook, if using github, remember they have dependabot
checks in your dependencies, if you have sonarqube available, it can also run
some scans

> tags: plan; learning; path;

> uid: 20220607084641Z

> links: 

