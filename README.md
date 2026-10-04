# TCP SYN Flood Incident Analysis

**Author:** Moriah Kantar
**Course:** Google Cybersecurity Professional Certificate
**Completed:** September 2026
**Project type:** Simulated incident analysis

## Overview

This project examines course-provided TCP/HTTP logs to assess a suspected SYN flood denial-of-service (DoS) attack against a web server.

The analysis documents normal connection behavior, repeated SYN traffic, connection resets, and a recorded gateway timeout. It explains the potential attack mechanism while distinguishing observed evidence from conclusions that require further investigation.

## Project Files

* [Incident Report](SYN-Flood-Incident-Report.pdf): My written attack assessment, evidence and findings, and technical explanation.
* [Supporting Network Log](TCP-HTTP-Log.pdf): Course-provided simulated traffic data, preserved without alteration.

## My Approach

1. Examined successful TCP handshakes and HTTP responses to establish normal behavior.
2. Identified repeated SYN packets from source IP 203.0.113.0 targeting 192.0.2.1 on TCP port 443.
3. Referenced specific log rows documenting connection resets and an HTTP 504 Gateway Timeout response.
4. Explained how half-open connections can affect server availability during a SYN flood.
5. Documented evidence limitations and the additional information needed to confirm the cause in a production environment.

## Key Findings

* Legitimate clients initially established connections and received HTTP 200 OK responses.
* Repeated SYN traffic appeared alongside connection failures affecting other clients.
* The log recorded an HTTP 504 Gateway Timeout response, indicating an unsuccessful upstream response through a gateway or proxy.
* The combined observations are consistent with the course's SYN flood scenario, but do not independently confirm server backlog exhaustion or identify an attacker.

## Skills Demonstrated

* Network log interpretation
* TCP three-way handshake analysis
* Recognition of suspicious traffic patterns
* Interpretation of TCP resets and HTTP status codes
* Assessment of service availability impact
* Evidence-based reasoning and technical report writing

## Scope and Limitations

This is an educational project using simulated data, not an investigation of a live system. I analyzed the supplied log rather than capturing traffic or performing an attack.

The dataset contains simplified entries and inconsistencies, including repeated row numbering and an HTTP response labeled as TCP. The report addresses these limitations. No mitigation measures were implemented or tested as part of this project.

## Learning Takeaway

This project strengthened my ability to connect network traffic patterns with service disruption and explain a suspected attack without overstating what the available evidence proves.

## Attribution

The scenario and supporting network log were provided through the Google Cybersecurity Professional Certificate. The incident report presents my analysis of those materials.
