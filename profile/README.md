# Welcome to [yag.im](https://yag.im)!

# Goal and Main Design Principles

yag.im aims to be the ultimate destination where gamers worldwide can play any classic video game released in the past, 
directly in their browser — no installation required, and completely free. Our guiding principles include:

- 100% Open Source: all code is open and accessible;
- Multi-OS Support: utilizing containerized environments for diverse game runners;
- Installer-as-Code: easily add or modify installers through GitHub PRs;
- Unified Gameplay Experience: seamless play in the browser with minimal load delays and input lag.

# Technology Stack

- Scalable, highly-available architecture: microservices (OVH K8S, minikube);
- Smooth gameplay streaming: WebRTC (gstreamer)
    - supports both X11 and Wayland; 
    - video encoder hardware offload: iGPU (Intel HD), Nvidia;
- Games runners: DosBox, Wine, ScummVM etc wrapped into portable platform-independent containers (docker);
- Distributed NFS-based cloud storage with CoW support (BTRFS).

# Alternatives

## Cloud Gaming Platforms (Amazon Luna)

Google Stadia (RIP), Amazon Luna and others mostly target AAA games or specific platforms (like Xbox Cloud Gaming and 
PlayStation Plus Premium). While Amazon Luna's collaboration with GOG looks promising for retro gamers, the collection 
remains tiny, and you still need to pay even if you own the original media.

## Online Gaming Platforms (Steam, GOG)

These platforms have recently expanded their libraries of classic video games, but you still need to purchase all games
you want to play even if you own the original media. Also, not all games run on every OS (e.g. some require Windows and 
won't start on Linux).

## Local Games Organizers (Lutris)

Lutris excels at enabling native gameplay on Linux with strong community support. However, maintenance of installers 
can be cumbersome, and most of them are just stubs linking to GOG and Steam. Non-stub installers often lack quality. 
Due to its reliance on native components, it's limited to Linux OS.

# How to Start

## *Gamer* Mode

Visit https://yag.im, select your favorite game, and start playing. Try few games to let the platform choose the closest 
data center for you (REF: link to the issue);

## *Self-hosted* Mode

This is for when you want to deploy and host `yag.im` in your own cloud or local infrastructure with minimal effort.

## *Developer* Mode

If you want to contribute to development, deploy yag.im services locally following the instructions below.

### Adding New Installers
