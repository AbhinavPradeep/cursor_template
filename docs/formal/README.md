# Formal Models (Optional)

This directory is intentionally empty by default.

Do not create a formal model merely because the system uses concurrency.

A formal model is justified only for a small concurrency-critical protocol where state ownership, ordinary tests, property/stateful testing, and manual reasoning are not giving adequate confidence.

Model the abstract protocol, not Python implementation details.

If a model checker finds a meaningful counterexample, encode the trace as a Python regression/stateful test where practical.
