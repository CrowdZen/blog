---
layout: post
title:  "What is Privacy (Part III)"
date:   2018-01-12 08:00:00 -0800
categories: privacy
---

In our last [post](https://medium.com/the-privacy-point/what-is-privacy-part-ii-af6b53c36c74) we looked at how an exponential adversary performs a privacy attack when the database releases exact answers.

In this post we illustrate another example by showing what is NOT private.

# Majority Population Inference Problem

Let's say we are interested in the number of people currently at Pauley Pavilion. If everyone currently at Pauley Pavilion acknowledged their attendance to some service, the service could easily aggregate and publish the counts.

However, is this privacy preserving?

Some might say that an individaul blends in a crowd, especially in a place as large as Pauley Pavilion that hosts over 10,000 people.

Though there is one observation. That is, as long as we know someone is participating in this crowd collection service, there is absolutely NO security or privacy mechanism that can protect the fact that the individual is at the Pauley Pavilion. Mere participation implies their exact location.

Let's look at another example.

Suppose we are interested in understanding the link between eating red meat and heart disease. Say we query 100 individuals and ask the question "Do you eat red meat and have heart disease?".

Now suppose that 85 out of the 100 do eat red meat and have heart disease, so truthfully respond "Yes".

Again, regardless of any security or privacy mechanism, anyone can reasonably infer that any participant eats red meat and has heart disease. The majority of the population in question has the characteristic thus allowing any adversary to correctly guess more than 50%.

Can we do better?

# Scalable Privacy via Query Expansion

Let's say we expand the query to 100,000 individuals where 99.99% of the population is vegetarian.

Now, the vegetarians blend with and provide privacy protection of the red meat eaters. That is, participation no longer implies eating red meat.

Thus, we desire large query sets, minority truthful population, and perturbation.

# Goals

Achieving scalable privacy achieves 3 goals.

First, it is difficult to determine if a particular individual participated.

Second, if someone participated it should be difficult to determine which population they belong (e.g., meat eater versus vegetarian).

Third, increasing the number of populations also provides us with additional analytics (e.g., monitoring 1 locations versus 15 locations)


