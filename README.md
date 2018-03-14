# broken-hashserve
Testing of broken-hashserve from JumpCloud
Tested on ubuntu 16.04, using Postman, curl, and shell scripts.
Used a test template from Google for test plan documentation.

Did not test on Windows or macOS. Those should
be tested as well if they are supposed to run this application.

Tried to run happy path tests and some negative path tests.

Did not validate the SHA512 content beyond reproducibility and length. That maybe
could use more testing.

The AC is a bit incomplete so I made some assumptions about:
Password length and valid content for a password.
Specification of return codes for post hash or get hash. I made some basic assumptions.
Does the average time of hash request include the 5 second wait?
Among the performance requirements missing is capacity. How many hashes/jobids can be stored?
How many can be processed at the same time?

Did some rudimentary performance testing using shell scripts. Am teaching myself JMeter so will
probably try JMeter on broken-hash later as an exercise. But did not want to wait to deliver the results.

Lots of negative path tests. Though I think these are good for completeness I would
consider some of this overkill. This service looks very much like an internal one and not
public facing. If available outside the company then requirements like password length,
special character handling, password strength, and capacity would be good.
Maybe a different call might wrap this one.
