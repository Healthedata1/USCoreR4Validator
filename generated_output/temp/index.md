---
title: Implementation Guide HomePage
layout: default
---

{:.no_toc}

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

### Introduction

The US Core Implementation Guide is based on [FHIR Version R4] and defines the minimum conformance requirements for accessing patient data. The [Argonaut] pilot implementations, ONC [2015 Edition Common Clinical Data Set (CCDS)], and the latest proposed ONC [U.S. Core Data for Interoperability (USCDI)] provided the requirements for this guide.  The prior Argonaut search and vocabulary requirements, based on [FHIR DSTU2](http://hl7.org/fhir/DSTU2/index.html), are updated in this guide to support [FHIR Version R4]. These profiles are the foundation for future US Realm FHIR implementation guides. In addition to Argonaut, they are used by [DAF-Research], [QI-Core], and [CIMI].  Under the guidance of HL7 and the HL7 US Realm Steering Committee, the content will expand in future versions to meet the needs specific to the US Realm.

These requirements were originally developed, balloted, and published in FHIR DSTU2 as part of the [Office of the National Coordinator for Health Information Technology (ONC)] sponsored [Data Access Framework] (DAF) project. For more information on how DAF became US Core see the [US Core change notes](change-notes.html).

### How to read this Guide

This Guide is divided into several pages which are listed at the top of each page in the menu bar.

- [Home]\: The home page provides the introduction and background for {{site.title}}.
- [Guidance]\: These pages provides overall guidance in using the profiles and transactions defined in this guide.
  - [General Guidance] provides guidance, definitions and requirements common to all {{site.title}} actors used in this guide..
  -  [Clinical Notes Guidance] gives guidance on the interactions between Consumers and Producers of clinical notes.
  -  [Future of {{site.title}}] outlines the approach to adding new content to {{site.title}}.
- [Profiles and Extensions]\: This page lists the set of Profile and Extension that are defined in this guide to exchange quality data. Each Profile page includes a narrative introduction, formal definition and a "Quick Start" guide to the supported search transaction for each {{site.title}} Profile.
- [Search Parameters and Operations]\: This page lists the{{site.title}} defined Operations and Search Parameters that are used in US Core transactions.
- [Terminology]\: This page lists the value sets and code system defined for {{site.title}} profiles.
- [Capability Statements]\: This set of pages describes the expected FHIR capabilities of the various {{site.title}} actors.
- [Security]\: General security requirements and recommendations for {{site.title}} actors.
- [Examples]\: List of links to all the examples used in this guide.
- [Downloads]\: This page provides links to downloadable artifacts.



### US Core Actors

The following actors are part of the US Core IG:

* US Core Requestor: An application that initiates a data access request to retrieve patient data. This can be thought of as the client in a client-server interaction.
* US Core Responder: A product that responds to the data access request providing patient data. This can be thought of as the server in a client-server interaction.


### US Core Profiles

The list of US Core Profiles is shown below.  Each profile defines the minimum mandatory elements, extensions and terminology requirements that **MUST** be present. For each profile requirements and guidance are given in a simple narrative summary. A formal hierarchical table that presents a [logical view] of the content in both a differential and snapshot view is also provided along with references to appropriate terminologies and examples.  For each US Core Profile, an overview of the required set of RESTful FHIR interactions - for example, search and read operations - is provided in the *Quick Start* Section of the profile page.

{% include list-simple-profiles.xhtml %}

- In addition US Core uses the [Vital Signs Profile] from the FHIR Specification.

See the General Guidance page for a [mapping] to the USCDI.

### US Core Conformance Requirements

The [Capability Statements Section](capstatements.html) outlines conformance requirements and expectations for the US Core Servers and Client applications, identifying the specific profiles and RESTful transactions that need to be supported. Note that the individual US Core profiles identify the structural constraints, terminology bindings and invariants.  Similarly, the individual US Core SearchParameter and Operation resources specify how they are understood by the server. However, implementers must refer to the CapabilityStatement for details on the RESTful transactions, specific profiles and the search parameters applicable to each of the US Core actors.

----


Primary Authors: Brett Marquard, Eric Haas

Secondary Authors: Grahame Grieve, Nagesh Bashyam

{% include link-list.md %}
