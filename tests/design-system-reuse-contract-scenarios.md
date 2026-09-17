# Confirmed Design System Reuse Contract Scenarios

These conceptual scenarios validate the contract between confirmed Design System discovery and materialization.

| ID | Confirmed official match | Materialization result | Expected outcome |
| --- | --- | --- | --- |
| A | Component confirmed and functionally applicable. | Official instance is used. | PASS. |
| B | Component confirmed and functionally applicable. | Primitive replaces it without recorded incompatibility. | FAIL. The result cannot receive `Ready`. |
| C | Component confirmed initially. | A concrete functional incompatibility is recorded and the element is reclassified before using the next policy level. | PASS. The next policy level may be used. |
| D | No component, variant, or pattern is confirmed as applicable. | Local Composition is used. | PASS. |
| E | External asset has no Design System equivalent. | Asset/container is used without creating or forcing a component. | PASS. |
| F | Official icon is confirmed and functionally applicable. | Unicode symbol replaces it without recorded incompatibility. | FAIL. The result cannot receive `Ready`. |
