# DIY RabbitMQ on Kubernetes

### ⚠️⚠️⚠️ Stop! There is a Better Way!

These examples were put together to accompany [a blog post](https://www.rabbitmq.com/blog/2020/08/10/deploying-rabbitmq-to-kubernetes-whats-involved/).
They **should not** be used as the primary example of RabbitMQ deployments on Kubernetes.
This code **is unlikely to receive timely updates**. For most intents and purposes,
it should be considered frozen in time 🥶 and **effectively unmaintained**.

The recommended way to deploy RabbitMQ on Kubernetes is the [RabbitMQ Cluster Operator for Kubernetes](https://www.rabbitmq.com/kubernetes/operator/operator-overview.html).
The Operator is developed [on GitHub](https://github.com/rabbitmq/cluster-operator/) and contains its own [set of examples](https://github.com/rabbitmq/cluster-operator/tree/master/docs/examples).

## What is This?

This directory contains **examples** that demonstrate a DIY minimalistic [RabbitMQ cluster](https://www.rabbitmq.com/clustering.html) deployments
on Kubernetes with [Kubernetes peer discovery](https://www.rabbitmq.com/cluster-formation.html).
There are several examples:

 * An [extensive one that targets the Google Kubernetes Engine (GKE)](./gke), originally contributed by Feroz Jilla
 * A [basic one that targets Minikube](./minikube)
 * Another [basic one that targets Kind](./kind), originally contributed by Gabriele Santomaggio

## Production (Non-)Suitability

Some values in these example files **may or may not be optimal for your deployment**. There are many aspects to
deploying and running a production-grade cluster on Kubernetes that this example cannot know or make too many assumptions about.
Persistent volume configuration is one obvious examples. You are welcome and encouraged to expand
the example by adding more files under the `examples/{environment}` directory.

We assume that the users of this plugin familiarize themselves with the [RabbitMQ Peer Discovery guide](https://www.rabbitmq.com/cluster-formation.html),
[RabbitMQ Production Checklist](https://www.rabbitmq.com/production-checklist.html),
and the rest of [RabbitMQ documentation](https://www.rabbitmq.com/documentation.html) before going into production.

Having [metrics](https://www.rabbitmq.com/monitoring.html), both of RabbitMQ and applications that use it,
is critically important when making informed decisions about production systems.


## Copyright and License

Released under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/).

(c) VMware, Inc. or its affiliates, 2020-2021.
