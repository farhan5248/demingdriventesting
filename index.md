---
layout: home
title: Deming Driven Testing
permalink: /
---

This site documents the cultural and technical transformation of QA teams using Dr. Deming's System of Profound Knowledge and lean principles. It explores how QA teams can evolve from defect inspection to prevention-based approaches.

## The Transformation Approach

The methodology applies four key frameworks to the process of inspection carried out by QA teams:

1. **Toyota Production System concepts** ([Jidoka][6], [Kaizen][7], [Poka-Yoke][8]): Error detection, continuous improvement, and mistake-proofing
2. **Dr Deming's System of Profound Knowledge**: Understanding systems, variation, knowledge theory, and psychology of change
3. **Improvement Kata by Mike Rother**: Systematic approach to developing improvement thinking and practice
4. **Lean Software Development by Tom and Mary Poppendieck**: Applying lean principles specifically to software development processes

The direction of challenge is to gradually provide feedback earlier by having QA tests run earlier, reducing the need for mass inspection. QA testers write test cases in [ubiquitous language][9] using an IDE, enabling quality to be built-in rather than inspected-in.

## Ubiquitous Language for QA

A key enabler of this transformation is adopting the ubiquitous language concept from Domain Driven Design. QA testers become domain experts who write test specifications in a shared language that both business stakeholders and developers understand. This natural language DSL approach allows teams to decide later which tests to automate while maintaining clear communication and reducing the need for traditional programming skills across the entire QA team.

For detailed technical implementation of ubiquitous language with IDE tooling and automation frameworks, see [Specification by Prompt][10].

## Learning Path

1. [Who was Dr Deming][1]: Understand the foundation - learn about Dr. Deming's philosophy, the 14 points, and System of Profound Knowledge that drives the transformation approach
2. [Why run the QA tests earlier?][2]: Discover the benefits of shift-left testing, statistical process control, and how early feedback reduces inspection dependency
3. [What led me to a QA team?][3]: See the practical journey from systems architecture to QA leadership and the challenges that drove this transformation
4. [Communicating the strategy to QA][4]: Learn proven approaches for introducing change to QA teams, handling resistance, and building buy-in for transformation
5. [Migrating from defect inspection to prevention][5]: Implement the step-by-step process for moving teams from reactive testing to prevention-focused quality practices

[1]: deming/index
[2]: why-run-the-qa-tests-earlier/index
[3]: what-led-me-to-a-qa-team/index
[4]: communicating-the-strategy-to-qa/index
[5]: migrating-from-defect-inspection-to-prevention/index
[6]: migrating-from-defect-inspection-to-prevention/jidoka
[7]: migrating-from-defect-inspection-to-prevention/kaizen
[8]: migrating-from-defect-inspection-to-prevention/poka-yoke
[9]: https://martinfowler.com/bliki/UbiquitousLanguage.html
[10]: /specificationbyprompt/index
