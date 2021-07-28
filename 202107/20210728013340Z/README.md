# Cloud concepts

High Availability

- Is core to the cloud, in that on traditional on-prem servers, you own the
  hardware, and all its failures, hardware is hard to replace and can take a
  while, in the cloud, you don't own the hardware, but you can replace hardware
  with a click when it fails, you can also use clusters spread across differents
  regions easily, to increase your availability

Fault Tolerance

- The idea here is that, with proper configuration, if hardware fails, it gets
  fixed automatically, so the system isnt affected by a fault; think of multi-az
  deployments and clusters or managed database services

Disaster Recovery

- It is about the ability to recover from natural disasters for example, such as
  hurricanes, floods or fire hazards

Scalability

- either scaling out or up (horizontal or vertical)
- is about the ability to increase|decrease resources to handle a demand

Elasticity

- usually goes along with scalability
- __makes use of scalability__ to dynamically and automatically increase or
  decrease resources as the demand itself increases or decreases
- a service can have high scalability, but not high elasticity, meaning you
  might be able to scale it out as needed, but it might not be possible to keep
  scaling in and out as the demands shifts
- Some interpret scalability as a long term strategic thing, while elasticity is
  more about short-term tactical usage

Agility

- ability to develop, test and deploy quickly, by leveraging the cloud features

> tags: cloud; azure; aws;

> uid: 20210728013340Z

> links:
