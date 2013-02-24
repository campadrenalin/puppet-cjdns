# puppet-cjdns, a Puppet module for installing and configuring cjdns.

This is forked from a [not-that-maintained version][sebnow] that I found on the internet. It's being revitalized for use as a standard part of the Roaming Initiative FOSS system, to be put into real world use in mesh relays and towers, with regular testing via Travis-CI.

System configurations currently supported:
 * Debian Stable with repo ruby, repo Augeas, git Puppet, and git CJDNS.
 * Travis-CI (Coming soon)

## Installation

Installation should be easy, and include installing CJDNS from source and generating a config if it's not already available. This part is still under development, but should eventually follow the following workflow:

1. Install non-CJDNS dependencies, including Augeas.
2. Install module via `puppet module install campadrenalin/cjdns`.
3. Specify a "cjdns" class in one of your development manifests.
4. Apply that manifest.

This will be filled out in more detail as it becomes reality.

## Testing

### Travis-CI

One of the big priorities right now is to develop support for Travis-CI, so that people don't need to set up VirtualBox or similar software to test their work. It's even more convenient for me, and I already have a VirtualBox image to test in.

This is not available yet.

### Personal VM

Anyone with a free afternoon can download a copy of Debian Stable, install it on a virtual machine, and play with puppet-cjdns in there.

My personal environment is in VirtualBox, with:

 * Ruby, installed via apt
 * Augeas, installed via apt
 * Puppet, installed via git
 * CJDNS, installed via git

At some point, puppet-cjdns will also support handling the CJDNS installation process for you.

## Help wanted?

I'm only just getting started working with Puppet. While I'm happy to learn, I don't want the delays of my learning curve to unnecessarily slow down the development process of puppet-cjdns.

As soon as I've got the really serious installation bugs worked out, I'm going to be using [FreedomSponsors.org][fs] to encourage rapid development and outside perspective, which will help ensure the stability and cross-platform support of this project.

[sebnow]: https://github.com/sebnow/puppet-cjdns
[fs]: http://www.freedomsponsors.org/
