# Docker

The Dojo4 approach to Docker development...

# Container Background

The general trend in software development is towards container based
development. And when we say "container" we mean Docker. So, what is
Docker? The sort answer is that it's a system for defining all of the
dependancies of a project (build tools, databases, etc) and then running
the project and it's dependancies in a virtual server that's separate
from the developers computer. For deploying software it builds a "Docker
image" which has all of the dependancies baked in and can be run on any
number of platforms Heroku, AWS, GCP, etc, without any need to confirm
servers.

The advantage of using Docker for development is the a dev can simple
pull down the Git repo build the environment and get to developing.
There's no need to install the correct version of Ruby, or Node, or
whatever and no need to install database servers or any other supporting
software. In theory, it doesn't matter at all what kind of computer the
dev is using, this will work on Mac, Linux, and even Windows. And, when
a dev is no longer working on the project all of the dependancies can be
removed. No more discovering some giant database left over from a
project you worked on 7 years ago. Finally, because the output of Docker
is a image that contain everything the project needs to run, we can know
it will work in production, no more "well it works for me".

The advantage of Docker for production is that the image can be run with
pretty much any hosting service and take advantage of features like
autoscaling and auto-failover.

The downside of Docker is that it takes some getting used to. The
workflow is more like developing on a server, you have to connect to the
Docker container and work inside it. This can be confusing at first.

In addition, you can't just login to a production Docker and start
debugging on the fly. There are ways around this, but it's a really bad
habit we have and something we should stop doing. There are much better
accepted practices for debugging issues that happen only in production
and Docker actually makes them easier to implement.

# State of the Container Union

We are very much it the process of transitioning to Docker. Projects
that have launch since mid-2019 built with Docker. Projects that
pre-date that are not.

There are two difference approaches to Docker in use at Dojo4.

Earlier Docker projects architected by Ara, such as the two Invited Home
apps, Value IO (currently not under contract), and Colorado School of
Public Health, use a highly customized build process. One design
principle of these projects was to allow for easily running outside of
Docker if the host OS is Linux. This feature has been dropped in later
implementations in favor of simplicity and having a single convention.
We think this change results in a more plug-and-play developer
experience, and everyone runs apps the same way, no matter your host OS.

Later Docker projects architected by Spike, such as NavPass and
Projects4 (Dojo Redmine), take a more off the shelf approach (i.e.
favors official images on Docker Hub). They work equally well on Mac and
Linux. Using official images means new devs have less to learn when
onboarding because they've likely already used these images. And there
is more writing on the Web that is helpful for researching and
troubleshooting when using these standard images instead of custom
images (tho there's always reasons to not use standard images, just make
sure you have a good one).

# Container Goals Yall

## Consistency

  - Projects should follow the same convention, so that developers need
    to have minimal, but preferably *no*, project-specific environment
    or deployment knowledge to work on the project.
  - Having the same dev scripts per project helps allow project do
    slightly different, project-specific things without impacting the
    developer experience or pushing project-specific knowledge onto the
    developer.

## Easy Onboarding

  - A developer should be able to run one command to get a project and
    all of its dependencies installed and running locally.
  - The more familiar the Docker setup feels to newcomers, the better

## Flexible Deployment

  - Projects should build in such a way that they can be deployed to any
    Docker hosting service, Heroku, AWS, GCP so that we can choose the
    best deployment strategy for a given project

# Container TODOs

  - \[ \] Create a base Docker/docker-compose setup (Navpass is a good
    start).
  - \[ \] Create scripts to make the experience consistent across
    different platforms. Derek's scripts in Navpass are a good start as
    are some of Ara's.
  - \[ \] Think about deploy. Is it part of the our tooling (as it is
    now) or should it be part of Github for automated deploys.
