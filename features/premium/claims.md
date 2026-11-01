# Claims

Status: draft.

A signed-in member pays through PayPal and submits a claim with the PayPal transaction id. A payment that arrived as two charges may include a second id. The same id cannot be used twice. A site admin approves the claim, and the member's Premium extends by 30 days from the later of now and the current expiry. The member can see how many days remain, and is reminded during the last five.

Nothing is charged automatically. A member may set a preference that they intend to renew; that preference does not take payment.

A site admin may also grant Premium for 1, 2, or 3 months, or for life, and may revoke a lifetime grant. Every grant, claim, and revocation is kept in a history the admin can search. Approving a claim and granting Premium are the only ways a member becomes Premium.

Until a site admin approves a claim, it does not unlock Premium tools or guild registration. What an active entitlement allows is defined in [Entitlement](entitlement.md).

## Done when

- A signed-in member can submit one claim for a payment, and cannot reuse a transaction id.
- Until a site admin approves it, the claim does not unlock Premium tools or guild registration.
- An approved claim extends Premium by 30 days from the later of now and the current expiry.
- A site admin can grant Premium for 1, 2, or 3 months, or for life, and can revoke a lifetime grant.
- Every grant, claim, and revocation is kept in a history the admin can search.
- A renew preference does not take payment.
