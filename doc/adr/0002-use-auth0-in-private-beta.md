# 2. Use <software> for private beta

Date: 2018-07-05

## Status

Proposed

## Abstract

Use <software> for user authentication and authorisation for Private Beta. Reconsider the approach after that.

## Context

DfE are developing a Sign-In service which we will use for user authentication and authorisation in the longer term, but we need something more quickly to enable a private beta rollout. 

We need to provide restricted access to a small number of users during private beta, to support continued testing and iteration of the supply teacher framework service. We also expect to need a mechanism for user authentication and authorisation for the other frameworks. 

Using a single authentication service will reduce administration overheads because we won't have to manage a JML (Joiners Movers Leavers) process. For users it will also mean they don't have to remember yet another username and password combination.

However, we want to get moving quickly, and integration with DfE Sign-In and identifying an identity solution for the other frameworks will take time. For now, we want a simple sign-in service that we can integrate with quickly, to enable us to test and iterate the application.

Auth0 is already in use by another CCS digital service, Report Management Information, as recorded [in their decision records](https://github.com/Crown-Commercial-Service/ReportMI-ADRs/blob/master/doc/adr/0011-use-auth0-for-temporary-user-authentication.md). 

## Decision

### option 1

We will use [Auth0](https://auth0.com) for authentication on a temporary basis.

Auth0 is an authentication service that uses the OAuth protocol. It provides and simple integration path, and is free for several thousand active users.

### option 1

We will use AWS Cognito for authentication on a temporary basis.

Cognito is tied in with our existing infrastructure approach and easy to integrate.

We acknowledge that we are incurring technical debt by not integrating immediately with DfE Sign-In, however we believe that this will let us move more quickly during development.

This decision will also allow us to gain a better understanding of the user needs around authentication before a decision around the final authentication solution for the other frameworks is made.

We will replace Auth0 with the proper authentication service later in the development process.


## Consequences

We will integrate with Auth0, but will need to replace this later.

We will work with other projects within CCS to establish the user needs around authentication, and feed into the decision around the final solution.

