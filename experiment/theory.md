#### Problem of false minima

It is possible to design (determine a set of weights) a Hopfield model with energy minima at desired states of the model, which correspond to stable states of the network, provided these states are representable in the network.
But for a given set of weights, there may be more than the desired number of stable states (energy minima). Some of them correspond to desired patterns and the rest of the stable states correspond to false minima in the energy landscape. The presence of such additional stable states may result in recalling a pattern not present in the set of desired patterns.

The errors in recall due to the false minima can be reduced by the following methods:

- Designing the minima in such a way that the given patterns correspond to the lowest energy minima in the energy landscape of the network.
- Using probabilistic (stochastic) update for the state for each unit, instead of the deterministic update of the states of the units as dictated by the activation value and the ouput function.

#### Stochastic Update

Error in pattern recall due to the presence of false minima can be reduced significantly using suitable activation dynamics. Let us assume that we are able to determine weights in such a way that the desired patterns are stored at the lowest energy minima. The activation dynamics can be modified so that initially the network can move even to a state with higher energy from the current state, and then settle down to a nearest deep energy minimum. Its possible to realize a transition to a higher energy state from the lower energy state using stochastic update for each unit, instead of the deterministic update of the output function in the Hopfield Model. In the stochastic update model, the transition from one state to another, is expressed in probabilistic terms, i.e., probability of firing is greater than 0.5, if activation value exceeds the threshold and the probability of firing is less than 0.5, if the activation value is below the threshold value.

The output function is still a nonlinear function, either hard limiting or a sigmoid semilinear function.

We can see that the probability function depends on a parameter called temperature (T). For T=0, the update is actually deterministic. But as the temperature is increased, the probability of firing increases rapidly when the activation value exceeds the threshold.

**Figure 1**: *shows the probability function and the output function of a given unit.*

<img src="images/probabilistic_update.jpg">


**Figure 1**: *Illustration of output function \( f(x) \) and probability of firing function \( p(1/x) \) for state update.