# Cloud Load Balancer Modules

This repo contains modules to perform load balancing on [Google Cloud Platform (GCP)](https://cloud.google.com/) using [Google Cloud Load Balancing](https://cloud.google.com/load-balancing/). It's based on [Gruntwork similary named module](https://github.com/gruntwork-io/terraform-google-load-balancer).

## Cloud Load Balancer Architecture

![Cloud Load Balancer Architecture](https://github.com/Estivador/terraform-google-load-balancer/blob/main/_docs/cloud-load-balancer.png "Cloud Load Balancer Architecture")

## Features

- Load balance HTTP and HTTPS traffic across multiple backend instances, across multiple regions with HTTP(S) Load Balancing.
- Load balance internal TCP/UDP traffic with Internal Load Balancing
- Load balance external TCP/UDP traffic with Network Load Balancing

## Learn

### Core concepts

- [What is Cloud Load Balancing](https://github.com/Estivador/terraform-google-load-balancer/blob/main/modules/http-load-balancer/core-concepts.md#what-is-cloud-load-balancing)
- [HTTP(S) Load Balancer Terminology](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/http-load-balancer/core-concepts.md#https-load-balancer-terminology)
- [Internal Load Balancer Terminology](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/internal-load-balancer/core-concepts.md#internal-load-balancer-terminology)
- [Network Load Balancer Terminology](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/network-load-balancer/core-concepts.md#network-load-balancer-terminology)
- [Cloud Load Balancing Documentation](https://cloud.google.com/load-balancing/)

### Repo organisation

This repo has the following folder structure:

- [root](https://github.com/Estivador/terraform-google-load-balancer/tree/main): The root folder contains an example of how to deploy a HTTP Load Balancer with multiple backends. See [http-multi-backend example documentation](https://github.com/Estivador/terraform-google-load-balancer/blob/main/examples/http-multi-backend) for the documentation.

- [modules](https://github.com/Estivador/terraform-google-load-balancer/blob/main/modules): This folder contains the main implementation code for this Module.

  The primary modules are:

  - [http-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/main/modules/http-load-balancer) is used to create an [HTTP(S) External Load Balancer](https://cloud.google.com/load-balancing/docs/https/).
  - [internal-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/main/modules/internal-load-balancer) is used to create an [Internal TCP/UDP Load Balancer](https://cloud.google.com/load-balancing/docs/internal/).
  - [network-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/main/modules/network-load-balancer) is used to create an [External TCP/UDP Load Balancer](https://cloud.google.com/load-balancing/docs/network/).

- [examples](https://github.com/Estivador/terraform-google-load-balancer/blob/main/examples): This folder contains examples of how to use the submodules.

## Deploy

If you want to try this repo out for experimenting and learning, check out the following resources:

- [examples folder](https://github.com/Estivador/terraform-google-load-balancer/blob/main/examples): The `examples` folder contains sample code optimized for learning, experimenting, and testing.

## Manage

### Day-to-day operations

- [How to configure a custom domain](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/http-load-balancer/core-concepts.md#how-do-you-configure-a-custom-domain)
- [How to configure SSL](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/http-load-balancer/core-concepts.md#how-do-you-configure-ssl)
- [How to configure access logging and monitoring](https://github.com/Estivador/terraform-google-load-balancer/tree/main/modules/http-load-balancer/core-concepts.md#how-do-you-configure-access-logging-and-monitoring)

## Support

If you need help with this repo - create an issue.

## Contributions

Contributions to this repo are very welcome and appreciated! If you find a bug or want to add a new feature or even contribute an entirely new module, we are very happy to accept pull requests, provide feedback.

## License

Please see [LICENSE](https://github.com/Estivador/terraform-google-load-balancer/blob/main/LICENSE.txt) for details on how the code in this repo is licensed.

Copyright &copy; 2022 Estivador.
