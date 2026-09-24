# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Driver Alert Notifications - Reduces reliance on calls and texts by making route changes visible quickly.
- **My finalized Must-Haves (after overriding the AI):** 1. Push notification when an assigned route changes
2. Clear summary of what changed and when
3. Tap notification to open the relevant route or task
4. Notification remains visible until opened or acknowledged
5. Reliable delivery after temporary connectivity loss
- **What I demoted from Must → Should/Won’t, and why:** I moved the in-app history of recent notifications to Should-Have. It would be useful for drivers to review previous alerts, but it is not required to validate the core route-change alert experience in the first sprint.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The PRD makes the expected behavior during poor connectivity explicit: alerts must be queued and delivered once the driver reconnects, while incomplete route updates must never trigger an alert.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The prototype showed that “route changed” was too vague. I clarified that the alert and updated route must show the specific type of change, such as a stop added, delayed, or cancelled, so the driver can understand it immediately.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://lovable.dev/projects/8afdd33d-4233-49a5-b75d-02902d016ef7?magic_link=mc_be997ce0-56a7-49d3-805b-854864ad7734
