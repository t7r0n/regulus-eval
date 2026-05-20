# Decision Report: Regulus Eval

A regulatory document evaluation harness + citation integrity runtime for AI drafted FDA submissions. Quantifies hallucination, orphan citation, and edit decay rates - and produces the GxP evidence pack a pharma CISO will actually sign off on.

## Evidence-Grounded Findings

CLAIM: claim regression harness should `open a regression issue with trace and benchmark delta` because blocks=3 reviews=5 mean_severity=2.528. [EVID: ev_0022]
CLAIM: evidence replay should `block release until cited evidence is regenerated` because blocks=4 reviews=5 mean_severity=2.611. [EVID: ev_0088]
CLAIM: handoff boundary probe should `route to reviewer with evidence packet` because blocks=3 reviews=4 mean_severity=2.528. [EVID: ev_0033]
CLAIM: review operator packet should `accept only if decision claims cite fixture evidence` because blocks=4 reviews=5 mean_severity=2.556. [EVID: ev_0099]
