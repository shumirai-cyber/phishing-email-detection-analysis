# Activity 9: Reviewing Email Security and Authentication Concepts

## Objective

To understand how email authentication technologies help organisations detect sender spoofing and reduce phishing risks.

## Key Concepts

### 1. SPF — Sender Policy Framework

SPF allows a domain owner to publish a policy identifying which servers are authorised to send email for that domain.

**Purpose:** Helps receiving email systems check whether a sending server is authorised by the domain's SPF policy.

**Key question:** Is this sending server authorised to send mail for the domain?

### 2. DKIM — DomainKeys Identified Mail

DKIM uses a digital signature associated with a domain. Receiving systems can verify the signature using the corresponding public key.

**Purpose:** Helps verify the signature and detect changes to signed email content.

**Key question:** Does the digital signature verify correctly?

### 3. DMARC — Domain-based Message Authentication, Reporting and Conformance

DMARC builds on SPF and DKIM. It checks whether their authentication results align with the domain in the visible From address. Domain owners can publish policies instructing receiving systems how to handle messages that fail DMARC and can receive reports.

**Purpose:** Helps reduce direct domain spoofing and provides policy and reporting options.

**Key question:** Do SPF or DKIM pass and align with the visible sender domain, and what policy should be applied if DMARC fails?

## Practical Scenarios

### Scenario A: Email passes SPF

A fictional email passes SPF because the sending server is authorised under the domain's SPF policy.

**Finding:** SPF passed, but this result alone does not prove that the email content is trustworthy.

### Scenario B: Email has a valid DKIM signature

A fictional email's DKIM signature verifies correctly.

**Finding:** The signature provides evidence that the signed content has not been altered since signing and that the message was signed using a key associated with the domain. It does not guarantee that the sender or message is harmless.

### Scenario C: Email fails DMARC

A fictional email fails DMARC because its authentication results do not satisfy the required alignment and authentication conditions.

**Finding:** The receiving system can apply the domain owner's published DMARC policy, which may request monitoring, quarantining or rejection.

## Key Findings

1. SPF checks whether a sending server is authorised under a domain's policy.
2. DKIM uses digital signatures to support email authentication and integrity checks.
3. DMARC checks alignment with the visible From domain and specifies handling policies and reporting.
4. Authentication results are useful security signals, but they do not establish that an email's content is safe.
5. Phishing can still occur through compromised legitimate accounts or authenticated domains.

## Security Recommendations

* Configure SPF, DKIM and DMARC correctly for organisational email domains.
* Monitor authentication results and investigate suspicious failures.
* Use an appropriate DMARC policy and introduce stricter enforcement carefully.
* Train staff to recognise suspicious links, attachments and requests for sensitive information.
* Verify unexpected requests through a known official channel.
* Never share passwords in response to an email.
* Use additional security controls, including multi-factor authentication and email filtering.

## Skills Demonstrated

* Understanding email authentication concepts.
* Distinguishing SPF, DKIM and DMARC.
* Evaluating email authentication results.
* Recognising the limitations of authentication.
* Recommending practical email security controls.

## Assessment Result

**Quiz score: 5/5 (100%)**

All five questions were answered correctly.

## Scope and Safety

This activity used fictional scenarios and conceptual examples. No real email accounts were accessed, and no live email authentication systems were tested or modified.

## Conclusion

SPF, DKIM and DMARC provide complementary protections against email spoofing. Correct configuration and monitoring can strengthen email security, but users must still evaluate suspicious messages and verify unusual requests independently.

**Status:** Completed
