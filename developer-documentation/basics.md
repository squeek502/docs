---
description: >-
  This page introduces you to projects and targets within the context of the
  Fuzzbuzz platform.
---

# Basics

## Projects

A project on Fuzzbuzz is a codebase that has been connected to the platform, either via an automatically-updating system such as GitHub, which will ensure you're always fuzzing the latest version of your code, or a manually-updating system which allows you to push changes whenever you're ready.

To learn how to connect your code to Fuzzbuzz, read the detailed [Projects Documentation.](projects.md)

## Targets

Every project on Fuzzbuzz consists of targets - simple components that run Fuzzbuzz-generated tests on your code. Each target follows the same 3 steps:

1. Read Fuzzbuzz-generated test case
2. Run the test case on your code
3. Check for errors

At its most basic level, a target can be thought of as a Unit Test, only rather than defining the test data yourself, you test using Fuzzbuzz-generated test data. To learn how to configure your targets for Fuzzbuzz, read the detailed [Targets Documentation.](targets.md)

