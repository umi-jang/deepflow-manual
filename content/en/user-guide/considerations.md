# Additional Considerations

*How DeepFlow improves accuracy and recommended transition models*

## Recommendations for getting more out of DeepFlow

### Understanding how DeepFlow improves accuracy

DeepFlow uses two mechanisms in tandem to maintain healthy inventory levels.

### Better shipment forecasts through data science

Advanced machine-learning models produce more accurate shipment forecasts.

### Better inventory by optimizing safety stock

When the ML forecast has residual error, optimizing safety stock corrects for it and keeps inventory within target.

Safety stock can be set in either of two ways:

- The user explores and defines a safety-stock level that fits the target inventory range, referring to the shipment forecast.
- DeepFlow predicts the residual error and automatically derives the optimal safety-stock level.

> **Note:** The automatic derivation is not available in DeepFlow V1.

### Transitioning from your existing process

AI systems can improve efficiency and productivity, but only if they fit your existing organizational processes.

- Teams that are used to today's process are typically not enthusiastic about adopting a new one overnight.
- Switching in one step also carries operational risk.
- A staged transition model is usually what works in practice.

**Transition model 1**

Keep using the existing process at first, treating DeepFlow as an insights reference. As the team gets comfortable with DeepFlow, expand its role gradually.

**Best for**: long-running processes or large operations.

**Transition model 2**

Switch to DeepFlow's process from the start, keeping the existing process as a safety net for reference. Later, replace the legacy process entirely.

**Best for**: short-lived processes or smaller operations.

**Transition model 3**

Adopt DeepFlow's approach end-to-end and run a forecast-first process from day one.

**Best for**: early-stage businesses or small operations that can adopt modern processes directly.
