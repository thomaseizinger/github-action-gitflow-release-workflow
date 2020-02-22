# GitFlow release workflow using GitHub actions

This repository contains GitHub workflows that allow for fully automated release as per the GitFlow conventions.
You are welcome to use it for inspiration for your own release workflows or maybe even copying them verbatim if the fit your needs.

## Usage

If you are using the workflows as they are in this repository, there are only two manual steps for releasing a new version:

1. Create a ticket that is titled "Release version x.y.z" and label it with "release".
2. Merge the PR that is created for you.

The automation will do the following things:

- Update your changelog with the new version
- Change the version in the necessary manifest files
- Tag the final release and create a GitHub release

## Design

I've written a blog post that describes the technical design in detail here: https://blog.eizinger.io/12274/using-github-actions-and-gitflow-to-automate-your-release-process

The idea of these workflows is to automate all the tedious aspects of releases while still allowing manual intervention if necessary and control over crucial aspects.

I think I've achieved this by doing the following:

- The individual GitHub actions used are small and focused.

This allows you to adapt the workflows to your own needs.
Ironically, this is what makes this whole repository not special.
It just takes good ideas that are already out there and creates automation around them.

- You have full control over what the next version is.

There is no magic involved, only the tedious things are automated.
You have full control over what is being released and under which version.

## Hall of fame

If you are using these workflow or got inspired by them to build something similar, feel free to add yourself to this list:

- BE THE FIRST ONE!

## License

MIT.
