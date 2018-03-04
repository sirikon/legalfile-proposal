# Legalfile Proposal #

Legalfile - A proposal for defining software legal terms in a structured way.

## Why ##

Today, software licensing is really important, and should be done **well**. But we're used to search for a package that fit our needs and just use it without seeing the software's license, which is a plain text file inside the repository.

What if we could see, automatically, the legal terms of any software, and even see if it fits with our needs?

For example: "Is commercial use forbidden for any of the installed packages?". "What's the list of all the people and projects that should be referenced based on the licenses?".

All this could be done directly making a database of simplified terms for the most known licenses (Something that tldrlegal.com does well), but to enable this level of automation, defining this terms inside a file in our projects could ease the process a lot, and having an open standard for doing this would be even better.

We could even build our own license with some builder, that outputs a `LICENSE.txt` and a `Licensefile`.

## The Legalfile ##

```yaml
license:
    name: MIT # Name of the license, if any.
    can: # Things that the license explicitly allows.
        - commercial-use
        - modify
        - distribute
        - sublicense
        - private-use
    cannot: # Things that the license explicitly forbids.
        - hold-liable
    must: # Requirements to use the software.
        - include-copyright
        - include-license
    warn:
        - "This area could be used to describe some perks of the license that isn't supported yet by a, right now, imaginary standard."
```

<details>
<summary>Why YAML?</summary>
<br>
Well-known language, implementations in any language, human-readable and easy to write.
</details>

## It's a proposal, so, I'm looking for feedback and discussion on this ##

I think it's an important topic, and that having legal terms in this way in every project could be **so** useful.

Be free to make pull requests, write issues and everything :D
