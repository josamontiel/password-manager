# Random Password Generator

> Only to be used for educational purposes, although the secrets library is cryptographically secure, there is more that goes into a password generator than just random character selection.

## Introduction

There are a lot blogs, videos, classes and even books dedicated to passwords. There is no shortage of information and theory around passwords. But one of the most talked about points is [password entropy](https://www.techtarget.com/whatis/definition/password-entropy). 

## What makes a strong password?

[NIST](https://www.nist.gov), basically release privacy guidelines every so often, the last set of benchmarks (NIST 800-63B) were:

1. Check passwords against breached lists.
2. Block the use of any passwords listed in password dictionaries.
3. Prevent the use of incremental or repetitive passwords.
4. Disallow context-specific passwords.
5. Increase the length of passwords.

But their Password requirements have, for as long as I can remember, have been:

1. 8 character minimum length.
2. Only change your passwords if there is evidence of compromise.
3. Screen new passwords against a list of known compromised passwords.
4. Skip password hints and knowledge-based security questions.
5. Limit the number of failed authentication attempts.

Some of there recommendations for passwords also include:

1. Set the max length of your password to 64 characters.
2. Skip character composition rules as they are an unnecessary burden for end users.
3. Allow copy/paste functionality in password fields to facilitate the use of password managers.
4. Allow the use of all printable [ASCII](https://en.wikipedia.org/wiki/ASCII) characters as well as all [UNICODE](https://en.wikipedia.org/wiki/Unicode) characters.

![XKDC Password Graphic](/bin/pw_generator/password_strength_graphic.png)

## Entropy

Essentially, password entropy is how Unpredictable your password is. Password entropy is typically measured in bits. The more bits your password has, the more likely you are to resist [brute force attacks](https://www.techtarget.com/searchsecurity/definition/brute-force-cracking) and [dictionary attacks](https://www.techtarget.com/searchsecurity/definition/dictionary-attack).

Password Entropy matters when developing a strong password, but it is **NOT** all that matters. Multiple passwords can have equal amount of bits, but when looking at the passwords themselves, one could be very strong while the other can be weak. This is mainly due to passwords in a list of already leaked passwords (Dictionary Attacks).

### Calculate password entropy

| Bits of entropy      | Strength |
| ----------- | ----------- |
|  0-39       | Very Weak   |
| 36-59       | Weak        |
|  60-119     | Strong      |
| 120+        | Very Strong |
