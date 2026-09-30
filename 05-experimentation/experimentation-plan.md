# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Driver Alert Notifications that immediately inform drivers about route changes and link directly to the updated route. |
| Persona | Delivery driver who relies on RouteLogic throughout the day to navigate routes and complete deliveries. |
| Expected outcome | Drivers become aware of route changes sooner, reducing reliance on calls and texts and the risk of following outdated routes. |
| Primary success metric | Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission. |
| Baseline rate | 10% |
| Guardrail metric | Wrong-driver alert rate |
| Guardrail boundary | Zero tolerance. Pause the experiment immediately and investigate if any alert is delivered to the wrong driver. |
| Second guardrail | Inaccurate or duplicate alerts to the correct driver must remain below 2%; investigate if the rate reaches 2%. |
| Minimum Detectable Effect | 50% |
| Sample size per arm | 14 |
| Traffic split | · |
| Test duration | 14 days |
| Significance threshold | · |

## Control vs. Variant
- **Control (A):** The dispatcher reassigns or changes a route, but the driver receives no notification. The updated route takes 8–15 minutes to appear in the driver app, so dispatchers often use calls or WhatsApp to reach the driver.
- **Variant (B):** When an assigned route changes, the driver receives an alert showing what changed and when. The driver can open the alert and go directly to the updated route.
- **Held constant (isolation check):** Both groups use the same RouteLogic app, route data, route-assignment process, optimization engine, devices, and onboarding. The only difference is that the variant receives a route-change alert with direct access to the updated route.

## Hypothesis
> I believe that Driver Alert Notifications that immediately inform drivers about route changes and link directly to the updated route. for Delivery driver who relies on RouteLogic throughout the day to navigate routes and complete deliveries. will result in Drivers become aware of route changes sooner, reducing reliance on calls and texts and the risk of following outdated routes., as measured by a 50% change in Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission. within 14 days. We will protect Wrong-driver alert rate throughout the test.

## Shipping criteria
> We will **ship** if Percentage of route-change alerts opened by the assigned driver within five minutes of dispatcher submission. improves by ≥ 50% at _(not filled in)_ and Wrong-driver alert rate does not reach Zero tolerance. Pause the experiment immediately and investigate if any alert is delivered to the wrong driver. after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
