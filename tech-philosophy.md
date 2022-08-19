# **Technology Philosophy**

As described in lists:

  - **values** that we aim for;
  - **priorities** we use to decide between potential approaches;
  - **verbotens** that we never do;
  - and **plagues** that we avoid.

Universal best practices are imaginary. This is how we think about
software. This is not necessarily how you or anyone else should make
software, unless you are in the codes with us.

## Values

  - Developer productivity es número uno.
  - Developer autonomy es número dos.
  - Developer happiness is the result of números uno y dos.
  - But production failures are often more damaging than slowed/lost
    developer productivity.
      - Negotiating between developer/devops/systems/etc needs am the
        hards.
      - So put a lot of thought, intention, and your back into it.
  - Security and privacy are 21st century.
  - Solve environments and devops before application code.
  - Solve least-understood engineering problems before other application
    code.
  - Break problems down until the pieces fit comfortably in your head.
  - Code like you're handing it off to someone who has a lot less
    experience and their native language doesn't use a Latin script.
  - Code like your phone is the one that gets called when the app dies
    at 3am.
      - But resist the temptation to over-solve the problem. (So hard,
        we know.)
          - Normalize logic after there's three well-understood use
            cases (just copy & paste before that).
  - There is more than one way to skin a cat.
      - Anyone can call an assembly to discuss a potential need for an
        architectural change.
      - Project leads resolve stalemates during cat-skinning
        disagreements, and they accept responsibility for their
        decision.
      - Skinning cats is a fucked up metaphor.
  - Peer reviews are how code gets better and how people learn.
  - "It works like you'd expect" is not a thing.
  - Making the team more productive is better than making yourself more
    productive.
  - Keep the big picture and long-term in mind, but more pragmatism,
    less paranoia.
  - UIs, CLIs, and APIs are all interfaces for humans, so make them nice
    to use.
  - As an engineer/designer/human/etc, the brain's working memory is the
    shittiest storage mechanism at your disposal.
      - It usually takes multiple attempts before anything's actually
        stored.
      - It usually doesn't store what you were trying to store.
      - So just put shit in clear text/code.
      - And focus more on retrieving shit that's \[probably\] already
        been stored in long-term memory.
  - Everybody sucks at estimating time, difficulty, others' potential,
    how logical/rational your argument is, etc; so adjust accordingly,
    and then adjust some more.

## Priorities

### Code

Encrypted secrets \> Deleting code \> Avoiding writing code \> Easy to
read code \> Easy to follow execution flow \> Easy to debug code \>
Easter eggs \> The team's coding style \> Easy to self-teach the
codebase \> Easy to test \> Easy to extend \> Community conventions \>
Easy to read a diff of the changes between commits \> Abstractions \>
Your coding style \> Being clever

### Devops

Encrypted secrets \> Production stability \> Production security \>
Local development speed/performance \> Local development observability
\> Local development debuggability \> Production observability \>
Production debuggability \> Production speed/performance \> Everybody
can deploy to every environment \> Continuous integration \> Automated
test speed/performance \> Standardized environments across projects \>
Works on Windows 👿 (you hafta help tho) \> Bastion hosts

### DX

Encrypted secrets \> Easy-to-use scripts for most development tasks \>
Easy to understand the contents of said scripts \> Accurate project
setup docs \> Accurate common issues docs \> Enforcing team's code style
\> Well-participated-in pull requests \> Standardization of
aforementioned dev scripts across projects \> Accurate architecture docs
when the system is kinda complex \> Works in PowerShell 💀 (you and your
doing-it-the-hard-way hafta help tho)

### Stacks

Encrypted secrets \> Boringness and maturity \> Fewer moving parts \>
Fun to use \> Well-documented FOSS \> Pleasant to debug \> Pleasant to
maintain in production \> Easy to hire for \> Used in the past \> What
projects dictate \> What clients want \> What blogs say \> What's
popular according to crawlers and search engine analyses \> New and
shiny \> The JavaScript ecosystem 🤠 (no hate...shit's just crazy...be
careful out there yall)

### Testing

Encrypted secrets \> TDD for logic that has catastrophic consequences
when it fails \> TDD for code that handles real-ass money or assets \>
Writing tests for actions that have lots of side effects \> Writing
tests for things that are difficult or cumbersome to manually test in
the CLI/API/UI \> Deploying untested code to production \> Writing tests
for bugs that bork production \> Writing tests for practical use cases
that, in part, demonstrate how parts of the system work together (is
better than documentation because failing tests force you to keep them
up-to-date and accurate) \> Arbitrary tests \> Code coverage \> TDD \>
Automated tests for HTML (there are infinite correct HTML, there can
only be one correct datum)

## Verbotens

  - Completely different stack on every project
  - Terse code that's "elegant" but requires interpreter/parser/arcane
    knowledge to understand
  - Automagic
  - Esoteric patterns, frameworks, and languages
  - `dotenv` (because `senv` is more secure, easier to manage, and
    harder to botch)

## Plagues (only if you must)

  - Rplling your pwn
  - Metaprogramming
  - Asking for permission (you're on the team because we trust you...no
    really...yeah we know everybody says that...we really do mean
    it...we can rollback if we have to)
