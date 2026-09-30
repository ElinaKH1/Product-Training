# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on the user feedback and product data, I believe simplifying core delivery workflows for experienced delivery drivers will reduce manual workarounds and improve adoption, measured by increasing Driver Compliance CSAT from 2.8 to at least 3.5. I will protect Manager Reporting CSAT at 4.5 or above and decide whether to scale after an 8–12 week pilot.
- **From M3, your primary success metric & guardrail metric:** Primary metric: Increase Driver Compliance CSAT from 2.8 to at least 3.5.
 Guardrail: Maintain Manager Reporting CSAT at 4.5 or above, ensuring simplification does not weaken valued enterprise capabilities.
- **From M4, the feature you scoped in your PRD this is what you're testing:** Driver Alert Notifications: Notify experienced delivery drivers immediately when their assigned route changes, clearly explain what changed, and provide direct access to the updated route.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** Driver Alert Notifications that immediately inform drivers about route changes and link directly to the updated route.
- **Persona pull your M2 persona:** Delivery driver who relies on RouteLogic throughout the day to navigate routes and complete deliveries.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Drivers become aware of route changes sooner, reducing reliance on calls and texts and the risk of following outdated routes.
- **Primary success metric the one number that defines success, from M3:** Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 10% planning assumption, based on some evidence of route changes currently taking 8–15 minutes to reach drivers and no push notification being available.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** No alerts are delivered to the wrong driver; inaccurate or duplicate alerts remain below 2%.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** 50 percentage points, representing an improvement from the assumed 10% baseline to at least 60%.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 14
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 split between control and variant across the three pilot accounts for four weeks, covering at least two full weekly operating cycles.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** The dispatcher reassigns or changes a route, but the driver receives no notification. The updated route takes 8–15 minutes to appear in the driver app, so dispatchers often use calls or WhatsApp to reach the driver.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** When an assigned route changes, the driver receives an alert showing what changed and when. The driver can open the alert and go directly to the updated route.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Both groups use the same RouteLogic app, route data, route-assignment process, optimization engine, devices, and onboarding. The only difference is that the variant receives a route-change alert with direct access to the updated route.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that Driver Alert Notifications that immediately inform drivers about route changes and link directly to the updated route. for Delivery driver who relies on RouteLogic throughout the day to navigate routes and complete deliveries. will result in Drivers become aware of route changes sooner, reducing reliance on calls and texts and the risk of following outdated routes., as measured by a 50% change in Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission. within 14 days. We will protect Wrong-driver alert rate throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission. improves by ≥ 50% at [significance] and Wrong-driver alert rate does not reach Zero tolerance. Pause the experiment immediately and investigate if any alert is delivered to the wrong driver. after 14 days. We will ITERATE if direction is positive but lift is below MDE. We will KILL if the primary metric shows no improvement or moves negatively. The read date is fixed at the end of 14 days, no results reviewed before then.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The primary metric was hardest to define. I initially focused on alert delivery, but realized that delivery alone does not show user value if drivers do not open the alert. I therefore changed the metric to alerts opened within five minutes, which also refined the hypothesis toward earlier driver awareness.
