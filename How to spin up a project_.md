  

# Client Onboarding Admin

*See also:*
[*https://projects.dojo4.com/documents/499*](https://projects.dojo4.com/documents/499)

## Communications

Once the client is ready to be onboarded, send them an email something
like one of these:

### Sample Onboarding Email

*Hi XXXX\!*

*I’m about to send you our agreements. There’s a basic master services
agreement and a lightweight engagement agreement- look for invites
through concordnow.com. You’ll have full edit access- please feel free
to make any necessary edits directly to the documents.*

*You’re also about to get an invitation to our project management tool
(Redmine) and I’m including our client onboarding survey here. Survey is
in no way a requirement but gives us added info about how best to work
with new clients, if you have time to jot down a few
thoughts: *[*https://dojo4.typeform.com/to/KzvasC*](https://dojo4.typeform.com/to/KzvasC)

*Same with our PM tool- you can choose to use it or not. We’ll be using
it for tasking, communication and documentation- and you’ll have full
access but if email is easier, use that and we’ll put your
communications in the tool ourselves. Here’s a
mini-orientation: *[*https://bit.ly/3ezmGoy*](https://bit.ly/3ezmGoy)

*Let me know if there’s anyone else at XXXX that we should add to the
project or should receive the contracts for review. And just let me know
if you have any questions...*

*Best,*

*XXX*

**<span class="underline">OR</span>**

*Hi XXX,*

*All three of you are about to get an invitation to our project
management tool (Redmine). The url for the project is
here: *[*https://projects.dojo4.com/projects/XXX/*](https://projects.dojo4.com/projects/XXX/)*.
This is the custom online tool that we use to manage the project
internally at dojo4 - we use it for tasking, communication and
documentation. You’ll have full access and visibility into our workflow
and activity. However, if email is easier, use that and we’ll put your
communications in the tool ourselves. Here’s a
mini-orientation: *[*https://projects.dojo4.com/pages/orientation*](https://projects.dojo4.com/pages/orientation)*.
If any of you does not need to be involved at this level, please just
ignore the invitation to the project tool. And if there is anyone else
from the XXX team that should be added, please let me know.*

*Our client onboarding survey can be found
here: *[*https://dojo4.typeform.com/to/KzvasC*](https://dojo4.typeform.com/to/KzvasC)*.
This survey is in no way a requirement but gives us added info about how
best to work with new clients, if you have time to jot down a few
thoughts.*

*We’ll follow up soon about scheduling a kickoff meeting and
introduction to the specific dojo4 team members that you’ll be working
with.*

*Best,*

*XXX*

### Documents & Agreements

[**Redmine orientation**](https://dojo4.bit.ai/docs/i7VMnKMr1bdDY9zb)

  - <https://docs.google.com/document/d/1Lxqs20SOZwz3dY7f71AlT-gytqVYHKkpMqrsCtp8408/edit?usp=sharing>
  - <https://github.com/dojo4/projects2/blob/master/app/views/pages/orientation.html.erb>

**Various client onboarding docs**

  - <https://drive.google.com/drive/folders/1DIf-QnMLZUwCr4f4qwDAJ-Q79g786knR?usp=sharing>

**Client orientation survey **

  - <https://dojo4.typeform.com/to/KzvasC>

**Master Services Agreement**

  - <https://secure.concordnow.com/negotiation/library/#/template/8769>
  - <https://drive.google.com/drive/folders/1DIf-QnMLZUwCr4f4qwDAJ-Q79g786knR?usp=sharing>

**Engagement Agreements**

  - <https://secure.concordnow.com/negotiation/library/#/template/8770> and <https://secure.concordnow.com/negotiation/library/#/template/37276>
  - <https://drive.google.com/drive/folders/1DIf-QnMLZUwCr4f4qwDAJ-Q79g786knR?usp=sharing>

  

# Technical Onboarding

## Naming

Naming the project is important. The name, or at least a **slug** of the
project name is used across multiple systems (GitHub, Redmine,
Freshbooks etc) so it should follow some simple rules.

  - all lower case
  - no spaces
  - no punctuation
  - words separated by dashes

If a system the project is connected to has a write-once -
can't-change-it field to identify the project, it should be this
`kebab-case-slug-for-the-project`. This slug will be used when [Setting
up
Redmine](https://www.notion.so/Setting-up-Redmine-for-a-New-Project-cba3725202ac41ebac5787c04c34e3c8)

## 1Password

  - create the vault
  - assign appropriate members - maybe invite the client as a guest to
    it
  - add the rails master key

Consider how to onboard someone with a blank new machine.

  - bundler
  - homebrew
  - ruby
  - rbenv
  - nvm
  - docker
  - add to dojo4 github
  - what else?
  -   

## GitHub

We use GitHub for our primary source code repository. Depending on the
client there could be a couple of different ways to configure this. See
[GitHub](https://dojo4.bit.ai/docs/YcusOEeoO7XNztMy) for more dojo4

### Project starts in Dojo4 organization

Often a new client will not have a GitHub organization and the project
will need to start in the [Dojo4 GitHub
Organization](https://github.com/dojo4/)

  - [Create a new
    repository](https://github.com/organizations/dojo4/repositories/new)
    using the `kebab-case-slug-name-name` that you came up with in
    **Naming** above
  - Make sure the project is **private**
  - do not select any of the checkbox options, we'll take care of that
    when we push to the repo for the first time.

### Client Already has GitHub Organization

This is the case when the client we are in a contract with already has a
GitHub Organization. The steps for the client are as follows:

  - go to their GitHub Organization page and create a new team
      - `https://github.com/orgs/[organization]/new-team`
  - Set `dojo4` as the team name - or if they already have a policy on
    team names have them use that.
  - They may want to select a parent team if they already have a team
    structure setup.
  - go to the new Team page and add the `dj4` user along with all the
    other Dojo4 github users that are to be on the project.
      - `https://github.com/orgs/[organization]/teams/[team-name]/members`
  - Add the new `dojo4` team to the 1 or more repositories that Dojo4
    will be working on. Or if its a new project have the client create
    the one or more repositories and give the team administrative access
    to it.

## Redmine

### Steps to Setup a New Project

1.  Got to [Dojo4 Projects
    Admin](https://projects.dojo4.com/admin/projects)
      - Click on **New Project**For **Name** pick a human readable name
        - this is required
      - For **Description** choose an appropriate paragraph or something
        from the contract.
      - For **Identifier** use the slug value you decided on in
        **Naming** above
      - Remind yourself to fill out the **github** link at some point
        once that is settled. See the **GitHub** Section above
      - At the bottom of the page under modules make sure all of the
        following are checked (they should be by default)
          - Issue Tracking
          - Time Tracking
          - News
          - Documents
      - Click on **Create**You'll now be on the **Settings** page for
        the newly created project.
          - In the **Members** tab click **Add new Member** and select
            the `@dojo4` group (you can search for it) and check the
            **Team** box
          - In the **Issue Tracking** tab Select the Project Lead from
            the **Default Assignee** tab and **Save**. *If there is
            nothing in the drop down, click back to the main project
            page, then back to Settings and then pick Issue Tracking
            again.*
2.  Create a group in the members settings to hold all the client
    Stakeholders that will have redmine accounts. If this is an existing
    client no need to do this section, although you may need to adjust
    the group memberships
      - Got <https://projects.dojo4.com/groups/new> and Create a new
        group. Name it appropriately for the client.
      - Head back over to the Project you created, and go to **Settings
        → Members** and add the new group to the project as
        **Stakeholder** role.
      - Invite all the client email addresses to redmine (Corey will
        normally handle this with onboarding documents and explain
        remine to them).
      - Once all the clients have their accounts in redmine - add them
        to the new group you just created

## Freshbooks

\[Corey / Jetha need to fill out the rest of this section\]

### Sync Freshbooks and Redmine projects

In order to get paid, the hours we log in Redmine need to be propagated
to Freshbooks. This is done automatically through the Redmine Freshbooks
Sync plugin.

  - Go to <https://projects.dojo4.com/freshbooks/projects>
  - Click the Big Blue **Sync Projects** button
  - Scroll down the list until you see the new Redmine project on the
    left, and the dropdown for Freshbooks Projects near it.
  - Select the appropriate Freshbooks Project from the dropdown and
    press the Big Blue **Associate** button.

## Project Tooling

Each project is unique, but here are the basic building blocks. We might
use some, all or none depending on the project requirements.

### Project type

  - Setting up a new Rails project
      - should we just do this with a rails template? `rails new --from
        template github-repo`

### Docker

mutagen, docker-compose, etc

### Vue/Nuxt

    yarn create nuxt-app <project-name>

Standard utils, Vue filters, patterns, etc? Do we use yarn vs npm?

### React/Next

  

### Ruby
