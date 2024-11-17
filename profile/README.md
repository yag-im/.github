# Welcome to [yag.im](https://yag.im)!

# Goal and Main Design Principles

According to the Video Game History Foundation, [only 13% of classic video games released in the US before 2010 are 
still commercially available](https://gamehistory.org/87percent/). `yag.im` aims to be the ultimate destination where 
gamers worldwide can play any classic video game released in the past, directly in their browser — no installation 
required, and completely free. Our guiding principles include:

- Fully Open Source platform: all code is open and accessible;
- Multi-OS Support: utilizing containerized environments for diverse game runners;
- Installer-as-Code: easily contribute or update installers via GitHub PRs;
- Unified Gameplay Experience: seamless play in any modern browser (in a full-screen mode) with minimal load delays and
input lag.

# Technology Stack

- Scalable, highly-available architecture: microservices (K8S, minikube);
- Smooth gameplay streaming: WebRTC (gstreamer), supporting:
    - both X11 and Wayland frames capturing; 
    - video encoding hardware offload: iGPU (Intel HD), Nvidia;
- Games runners: DosBox, Wine, ScummVM etc wrapped into portable platform-independent containers (docker);
- Distributed NFS-based cloud storage with CoW support (BTRFS).

# Alternatives

## Cloud Gaming Platforms (Amazon Luna)

Proprietary Google Stadia (RIP), Amazon Luna and others mostly target AAA games or specific platforms (like Xbox Cloud 
Gaming and PlayStation Plus Premium). While Amazon Luna's collaboration with GOG looks promising for retro gamers, the 
collection remains tiny, and you still need to pay even if you own the original media.

## Online Gaming Platforms (Steam, GOG)

These proprietary platforms have recently expanded their libraries of classic video games, but it's still required to 
purchase all games you want to play even if you own the original media. Also, not all games run on every OS (e.g. some 
require Windows and won't start on Linux).

## Local Games Organizers (Lutris, "Wine wrappers" etc)

Lutris excels at enabling native gameplay on Linux with strong community support. However, maintenance of installers 
can be cumbersome, and most of them are just stubs linking to GOG and Steam. Non-stub installers often lack quality. 
Because it relies on native components, it is limited to Linux OS. Even on Linux, launching a game can be quite the 
challenge due to OS dependencies across different Linux distributions.

# Where to Start

Based on your experience, choose one of the operational modes listed below.

## Gamer Mode

Visit [yag.im](https://yag.im), find your favorite game and start playing. Try few games to let the platform choose the 
closest data center for you (TODO: make DC selection preemptive). If you can't find your favorite game, share your 
requests for new games on our [Discord Channel](https://discord.gg/N4QavHBBAG).

## Self-Hosted Mode

This is for when you want to deploy and host `yag.im` in your own cloud or local infrastructure with minimal effort.
Begin by following the [Self-Hosted Mode](https://github.com/yag-im/infra/blob/main/docs) tutorial.

## Developer Mode

If you want to contribute to development, deploy `yag.im` services locally following the 
[Developer Mode](https://github.com/yag-im/infra/blob/main/docs) 
instructions. Keep in mind that you can add new installers by following the 
[Adding New Installers (Ports)](https://github.com/yag-im/ports/blob/main/docs/NEW_PORT.md)
tutorial, eliminating the need for the lengthy local setup process.
