# Welcome to [yag.im](https://yag.im)!

# Goal and Main Design Principles

According to the Video Game History Foundation, [only 13% of classic video games released in the US before 2010 are 
still commercially available](https://gamehistory.org/87percent/). `yag.im` aims to be the ultimate destination where 
gamers worldwide can play any classic video game released in the past, directly in their browser — no installation 
required, and completely free. Our guiding principles include:

- Fully Open Source platform: all code is open and accessible;
- Multi-OS Support: utilizing containerized environments for diverse game runners;
- Installer-as-Code: easily contribute or update installers via GitHub PRs;
- Unified Gameplay Experience: seamless play in any modern browser with minimal load delays and input lag.

# Technology Stack

- Scalable, highly-available architecture: microservices (K8S for prod, minikube for dev);
- Smooth gameplay streaming: WebRTC (gstreamer), supporting:
    - X11 and Wayland frames capturing; 
    - video encoding hardware offload: iGPU (Intel HD), Nvidia;
- Games runners: DosBox, Wine, ScummVM etc wrapped into portable platform-independent containers (docker);
- Distributed NFS-based cloud storage with CoW support (BTRFS).

# Alternatives

## Cloud gaming platforms (Amazon Luna)

Proprietary Google Stadia (RIP), Amazon Luna and others mostly target AAA games or specific platforms (like Xbox Cloud 
Gaming and PlayStation Plus Premium). While Amazon Luna's collaboration with GOG looks promising for retro gamers, the 
collection remains tiny, and you still need to pay to play even if you own the original media.

## Online gaming platforms (Steam, GOG)

These proprietary platforms have recently expanded their libraries of classic video games, but it's still required to 
purchase all games you want to play even if you own the original media. Also, not all games run on every OS (e.g. some 
require Windows and won't start on Linux).

## Local games organizers (Lutris, "Wine wrappers" etc) with streaming solutions.

Lutris excels at enabling native gameplay on Linux with strong community support. However, maintenance of installers 
can be cumbersome, and most of them are just stubs linking to GOG and Steam. Non-stub installers often lack quality. 
Because it relies on native components, it is limited to Linux OS. Even on Linux, launching a game can be quite the 
challenge due to OS dependencies across different Linux distributions.
In conjunction with popular open-source streaming solutions like Moonlight and Sunshine, you can create a DIY 
"cloud gaming" platform. This is likely where an experienced user would begin, provided they know how to configure all 
the components.

# Where to Start

Based on your experience, choose one of the operational modes listed below.

## Gamer Mode

Visit [yag.im](https://yag.im), find your favorite game and start playing. Try few games to let the platform choose the 
closest data center for you (TODO: make DC selection preemptive :). If you can't find your favorite game, share your 
requests for new games on our [Discord Channel](https://discord.gg/N4QavHBBAG).

## Self-Hosted Gamer Mode

This is for advanced gamers, when you want to deploy and host `yag.im` in your own cloud or local infrastructure with 
minimal effort. Begin by following the 
[Self-Hosted](https://github.com/yag-im/infra/blob/main/docs/dev-local.md) 
tutorial.

## New Installers (Ports) Creator

In this mode, you can contribute to the project by creating new installers (ports) using 
[Adding New Installers (Ports)](https://github.com/yag-im/ports/blob/main/docs/new-port.md)
tutorial; this also eliminates the need for the lengthy local setup process.

## Code Contributor (Developer Mode)

If you want to contribute to development of this project, deploy all `yag.im` components locally following the 
[Developer](https://github.com/yag-im/infra/blob/main/docs/dev-mode.md) 
instructions.
