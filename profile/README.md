# Welcome to [yag.im](https://yag.im)!

# Goal and Main Design Principles

yag.im aims to be the ultimate destination where gamers worldwide can play any classic video game released in the past, 
directly in their browser — no installation required, and completely free. Our guiding principles include:

- 100% Open Source: all code is open and accessible;
- Multi-OS Support: utilizing containerized environments for diverse game runners;
- Installers-as-Code: easily add or modify installers through GitHub PRs;
- Unified Gameplay Experience: seamless play in the browser with minimal load delays and input lag.

# Technology Stack

- Microservices architecture: supports Kubernetes (K8S) deployments;
- WebRTC: For smooth gameplay streaming;
- Docker Containers: For game runners.

# Alternatives

## Cloud Gaming Platforms (Amazon Luna)

Google Stadia (RIP), Amazon Luna (with uncertain future), and others mostly target AAA games or specific platforms like 
Xbox Cloud Gaming and PlayStation Plus Premium. While Amazon Luna's collaboration with GOG is promising for retro 
gamers, the collection remains small, and you still need to buy the games even if you own the original media.

## Non-Cloud Gaming Platforms (Steam, GOG)

These platforms have recently expanded their libraries of classic video games, but you still need to purchase all games,
you want to play even if you own the original media. Also, not all games run on every OS (some require Windows and won't 
start on Linux).

## Local Games Managers (Lutris)

Lutris excels at enabling native game play on Linux with strong community support. However, maintenance of installers 
can be cumbersome, and many are just stubs linking to GOG and Steam. Non-stub installers often lack quality. Due to its 
reliance on native components, it's limited to Linux OS.

# How to Start

There are three ways to use `yag.im`:

1. Cloud Gaming Mode: visit https://yag.im, select your favorite game, and start playing. Try few games to let the 
platform choose the data center with minimal RTT for you (REF: link to the issue);
2. "Local"-streaming gaming mode: initially designed for cloud gaming, but can also run locally on your PC or network;
3. Development Mode: if you want to contribute to development, deploy yag.im services locally following the instructions 
below.

# Adding New Installers
(TODO)
