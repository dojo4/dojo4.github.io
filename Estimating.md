*Based on original by Ara Howard @drawohara:*
[*https://github.com/dojo4/dojo4/blob/master/docs/how-tos/how-to-estimate-a-project.md*](https://github.com/dojo4/dojo4/blob/master/docs/how-tos/how-to-estimate-a-project.md)

  

# **How to estimate a project**

## Do

  - **Estimate broad categories** of work such as 'api', and 'site
    design'.
  - **Avoid estimating features and focus on estimating business goals
    and requirements** such as 'can buy a product' vs 'integrate with
    stripe', or 'ability to download movies' vs 'ability to click a red
    button and download a movie if no other movie is in the queue which
    is displayed in a widget in the upper right corner.'
  - **Keep estimates to one page**, or even one paragraph with bullet
    points. If it doesn't fit on a page it's likely the project will
    cost \> 100k and you'll want help, a white board, and 1/2 day to
    make the estimate. Never do these kind for free.
  - **Ask for an internal review** of your estimate by one team member.
  - **Work in teams** to estimate large projects.
  - **Consider collateral work**. For instance: a logo implies a favicon
    and an apple-home-screen icon, a production deploy implies a staging
    deploy, monitoring, and database backups... think from the client
    perspective about everything they will need to do to be live
    including DNS procurement, password management, account setup, etc.
  - **Consider the personality of the client**. How much communication
    do they need? How much detail in tickets/invoices/etc? If they will
    be involved multiply by about 200%, if they want to help 300%.
  - **Time box your effort estimating**. 15 minutes is good. 1 hour is
    pushing it. Too many unknowns to do this suggests a paid exploration
    period of 1-3 days in order to write code, research, and provide a
    more accurate estimate. Alternatively give big ranges - ask for paid
    exploration to narrow them.
  - **Look for something small to start**. If 15k of work is clear and
    the remaining 85k is murky, suggest getting going *tomorrow* on the
    clear discrete bit and returning to estimate the murky bit when more
    it known. The client will still want a ballpark - but this can
    unblock negotiations.
  - **Avoid talking about rates in estimates**. Ideally we can charge
    25k for completed project *regardless* of how many hours were spent
    when that number was in the range estimated (this doesn't happen
    often but is possible).
  - **Include a minimum and maximum number of hours** we'll work on the
    project *regardless of its completion*. This protects us from
    never-ending feature creep and the client by promising a minimum
    effort level. To calculate this divide the highest cost you can
    imagine by \~$100 (we are losing money) for the maximum and, for the
    minimum, divide the lowest cost you can image by \~$200 (we are
    killing it).
  - **Include a suggested start date and end date**. Assuming the team
    is working at 50% capacity to get this number. So if you think it'll
    take 2 people working 30 hrs/wk for one month suggest an end date *2
    months* after the start date.
  - **Include an expiration date for the estimate**. When a client comes
    back 3 months later ready to start something any research done will
    need to be repeated, now apis may exist, the product may have many
    competitors where once it had none, our pipeline may be more full or
    empty than it was when we originally made the estimate... all of
    these things can cause a big change to an estimate.
  - **Consider our pipeline**. When it is empty, aim for smaller bits of
    cheaper work. When it is full aim high.
  - S**uggest staying on our current stacks**. Moving to another
    framework or deployment container always need considered.
  - **State the problem you'll be solving in the estimate**. Are you
    *sure* they understand what they are asking for?

## Do Not

  - **Underestimate the importances of having access to** ***all***
    **production content, apis, etc** ***up front***. Not having these
    up front has the ability to make any estimate a wild ass guess from
    the get go.
  - **Underestimate the lag time legal can add to a possible start
    date**. This goes along with getting *any* contract signed ASAP.
  - **Estimate specific details** unless every single aspect of it is
    known (it never is).
  - **Underestimate authentication**. If the project colors outside the
    lines (we don't already have it 100% programmed), it will cost at
    least 2.5k to get right if it is a standard 3rd party (OAuth,
    Google, etc.). If it's custom it will absolutely consume a week
    before the project is finished.
  - **Underestimate deployment and delivery**. A day is 1k. Even getting
    a DNS entry setup and static files to a client takes time and
    energy.
  - **Underestimate integrations**. An external api or dependency adds
    an *order of magnitude* of difficulty because of communication,
    bugs, blocking, and changes.
  - **Underestimate the cost of duration and handoffs**. A project that
    stretches over long periods of time and has many handoffs incurs
    lots of increased costs. For small projects (\< 10k) expect this to
    be a factor of about 100%.

## An Example

Hi Clientperson,

I've reviewed your fucking vague Microsoft Word doc full of mutually
contradictory requirements docs and see the following:

You will need:

  - A micro site put up on <http://sweet-new-thang.com>.
  - An API integration with <http://awesome-sauce.com> in order to
    conquer the world and sell lots of kittens.
  - Some sort of ability to turn this into books full of kittens.

We see the following next steps:

  - Getting your micro-site up is something we can start next Monday.
    This could take 3-5 man days and cost \~3.5-4k.
  - The api integration with <http://awesome-sauce.com> will take a bit
    of research since it's currently in beta and the repo seems to be
    under active development. We'd like to do a time-boxed assessment of
    it now in order to fully understand the difficulty in integrating
    with it in production, although we think this will take about 2
    weeks, or \< \~10k.
  - The book fulfillment is a really big project and we're not prepared
    to estimate it at this time without access to the fulfillment api
    that is being built by
    <http://aint-going-to-happen-any-time-soon.com> and without
    reviewing at least three samples of complete book content -- the
    animated gif of the kitten isn't cutting it... In any case, while it
    is possible that this could cost 19 bucks, as you suggest, it also
    may cost $999,999 bucks and we think it's prudent to consider this
    effort in another sprint.

Assuming we can start work next Monday, and no later than two weeks from
now, we'd be able to finish the microsite in 2 weeks and have a go/no-go
on the awesome-sauce API in that same time frame. assuming our research
on the API doesn't reveal any blockers, we'd finish the integration 6
weeks from now.

Ignoring the book fulfillment you'll be looking at:

  - \~ 5-14k
  - \~ 6 calendar weeks until launch

If this sounds good let us know asap and we'll get this up in
[concordnow.com](http://concordnow.com) where we can continue to make
adjustments.

Cheers - I'm sure you'll rule the world with kitten books.
