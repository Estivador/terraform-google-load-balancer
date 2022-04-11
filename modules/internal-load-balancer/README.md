# Internal Load Balancer Module

This Terraform Module creates an [Internal TCP/UDP Load Balancer](https://cloud.google.com/load-balancing/docs/internal/) using [internal forwarding rules](https://cloud.google.com/load-balancing/docs/internal/#forwarding_rule).

Google Cloud Platform (GCP) Internal TCP/UDP Load Balancing distributes traffic among VM instances in the same region in a VPC network using a private, internal (RFC 1918) IP address.

Module is based on [Gruntwork similary named module](https://github.com/gruntwork-io/terraform-google-load-balancer).

## Learn

### Core concepts

- [What is Cloud Load Balancing](https://github.com/Estivador/terraform-google-load-balancer/blob/master/modules/internal-load-balancer/core-concepts.md#what-is-cloud-load-balancing)
- [Internal Load Balancer Terminology](https://github.com/Estivador/terraform-google-load-balancer/tree/master/modules/internal-load-balancer/core-concepts.md#internal-tcpudp-load-balancer-terminology)
- [Internal Load Balancing Documentation](https://cloud.google.com/load-balancing/docs/internal/)

### Repo organisation

This repo has the following folder structure:

* [root](https://github.com/Estivador/terraform-google-load-balancer/tree/master): The root folder contains an example of how to deploy a HTTP Load Balancer with multiple backends. See [http-multi-backend example documentation](https://github.com/Estivador/terraform-google-load-balancer/blob/master/examples/http-multi-backend) for the documentation.

* [modules](https://github.com/Estivador/terraform-google-load-balancer/blob/master/modules): This folder contains the main implementation code for this Module.

  The primary modules are:

    * [http-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/master/modules/http-load-balancer) is used to create an [HTTP(S) External Load Balancer](https://cloud.google.com/load-balancing/docs/https/).
    * [internal-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/master/modules/internal-load-balancer) is used to create an [Internal TCP/UDP Load Balancer](https://cloud.google.com/load-balancing/docs/internal/).
    * [network-load-balancer](https://github.com/Estivador/terraform-google-load-balancer/blob/master/modules/network-load-balancer) is used to create an [External TCP/UDP Load Balancer](https://cloud.google.com/load-balancing/docs/network/).
                                                                                                                                           
* [examples](https://github.com/Estivador/terraform-google-load-balancer/blob/master/examples): This folder contains examples of how to use the submodules.

## Deploy

If you want to try this repo out for experimenting and learning, check out the following resources:

- [examples folder](https://github.com/Estivador/terraform-google-load-balancer/blob/master/examples): The `examples` folder contains sample code optimized for learning, experimenting, and testing.

## Manage

### Day-to-day operations

- [Internal Load Balancer access logging and monitoring](https://github.com/Estivador/terraform-google-load-balancer/tree/master/modules/internal-load-balancer/core-concepts.md#internal-tcpudp-load-balancing-monitoring)
- [Internal Load Balancer DNS names](https://github.com/Estivador/terraform-google-load-balancer/tree/master/modules/internal-load-balancer/core-concepts.md#internal-tcpudp-load-balancing-and-dns-names)

## Support

If you need help with this repo - create an issue.

## Contributions

Contributions to this repo are very welcome and appreciated! If you find a bug or want to add a new feature or even contribute an entirely new module, we are very happy to accept pull requests, provide feedback.

## License

Please see [LICENSE](https://github.com/Estivador/terraform-google-load-balancer/blob/master/LICENSE.txt) for details on how the code in this repo is licensed.

Copyright &copy; 2022 Estivador.
