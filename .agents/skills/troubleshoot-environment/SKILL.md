---
name: troubleshoot-environment
description: Diagnose and recover from recurring or clear setup, policy, permission and toolchain failures after the resident repository trigger pauses ordinary work. Do not use for expected code, content or test failures without infrastructure evidence.
---

# Troubleshoot Environment

Restore a verified working path without broadening the suspended task.

1. Suspend the original task. Capture the failed operation, output, environment
   boundary and whether activation followed one clear infrastructure failure or
   a second equivalent failure after one plausibly transient retry. A different
   shell or transport does not make an equivalent retry new evidence.
2. Load `TROUBLESHOOTING.local.md` when present and then
   `TROUBLESHOOTING.md`. These records are conditional context: do not read them
   before the resident trigger fires. Reuse an entry only when its stable
   signature and applicability both match and its safe diagnostic reconfirms
   the recorded cause. Otherwise diagnose anew with bounded, read-only evidence.
3. Classify the recovery as a durable repair, stable workaround or task-local
   bypass. Prefer a durable repair, explain why a lesser option is stable and
   bounded when one is necessary, and never disguise an equivalent failed path
   as a workaround.
4. Preserve every existing boundary. Troubleshooting does not grant access to
   `input/`, registered materials or `temp/restricted/`. Ask before privilege,
   installation, credential or sensitive access, outside writes, transmission,
   global configuration, security relaxation, destructive recovery or another
   protected action. A proposed authorization is not maintainer authorization.
5. Apply only the authorized recovery, then rerun the originally failing
   operation through its normal path. Recheck any access, security or trust
   assumption changed by the recovery. Do not infer success from a diagnostic
   substitute.
6. Resume the original task only after verification. If recovery remains
   unavailable or unauthorized, leave the task paused and record the failure,
   evidence, requested authority and smallest next step in the handoff.
7. After a verified recovery, update `TROUBLESHOOTING.md` only for a portable,
   sanitized pattern. Put machine identifiers, absolute paths and host-specific
   facts in ignored `TROUBLESHOOTING.local.md`. Record the signature,
   applicability, cause, safe diagnostic, durable repair, bounded workaround,
   authorization needs, verification and last confirmed date. Never record
   secrets or treat a workaround as template policy.
