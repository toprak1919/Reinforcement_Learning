# Interactive Reinforcement Learning Learning Platform

An interactive web-based platform to learn Reinforcement Learning concepts through hands-on experimentation.

## Features

### 🎮 Interactive Grid World
- Visual representation of a 5x5 grid environment
- Agent that learns to navigate from start to goal
- Obstacles to avoid
- Real-time visualization of learning progress

### 📚 Q-Learning Implementation
- Full Q-Learning algorithm implementation
- Visual representation of the learning process
- Adjustable hyperparameters

### ⚙️ Customizable Parameters
- **Learning Rate (α)**: Control how quickly the agent updates its knowledge
- **Discount Factor (γ)**: Adjust how much the agent values future rewards
- **Exploration Rate (ε)**: Balance exploration vs exploitation
- **Training Speed**: Control the visualization speed

### 📊 Real-time Statistics
- Episode count
- Total reward
- Step count
- Success rate tracking

## How to Use

### Manual Control
1. Open `index.html` in your web browser
2. Use the arrow buttons (⬆️ ⬇️ ⬅️ ➡️) to manually control the agent
3. Try to reach the goal (green) while avoiding obstacles (black)

### Watch the Agent Learn
1. Adjust the learning parameters using the sliders
2. Click "🎓 Start Training" to begin automated training
3. Watch as the agent learns through trial and error
4. Observe how success rate improves over episodes

### See the Learned Policy
1. Train the agent for several episodes (50-100 recommended)
2. Click "🎯 Show Best Path" to see the optimal policy
3. The agent will demonstrate the best path it has learned

## Key Concepts Covered

1. **Agent-Environment Interaction**: How an RL agent interacts with its environment
2. **States and Actions**: Understanding the state space and action space
3. **Rewards**: How feedback shapes learning
4. **Q-Learning**: The Q-Learning algorithm and update rule
5. **Exploration vs Exploitation**: The fundamental trade-off in RL
6. **Convergence**: How the agent improves over time

## Getting Started

Simply open the `index.html` file in any modern web browser:

```bash
# Using Python's built-in server
python -m http.server 8000

# Or with Python 2
python -m SimpleHTTPServer 8000

# Then visit http://localhost:8000
```

Or just double-click the `index.html` file to open it directly in your browser.

## Technical Details

### Q-Learning Update Rule
```
Q(s,a) ← Q(s,a) + α[r + γ max Q(s',a') - Q(s,a)]
```

Where:
- `Q(s,a)`: Q-value for state s and action a
- `α`: Learning rate
- `r`: Reward received
- `γ`: Discount factor
- `s'`: Next state
- `a'`: Next action

### Reward Structure
- Goal reached: +100
- Obstacle hit: -100
- Empty cell: -1 (encourages shorter paths)

## Recommended Experiments

1. **Effect of Learning Rate**:
   - Try α = 0.01 (slow learning)
   - Try α = 0.5 (fast learning)
   - Observe stability vs speed

2. **Effect of Discount Factor**:
   - Try γ = 0.1 (myopic - values immediate rewards)
   - Try γ = 0.99 (far-sighted - values future rewards)

3. **Exploration vs Exploitation**:
   - Try ε = 0.9 (high exploration)
   - Try ε = 0.1 (low exploration)
   - See how it affects learning speed

## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## Future Enhancements

Potential additions:
- Different environment layouts
- More complex algorithms (SARSA, DQN)
- 3D visualization
- Multi-agent scenarios
- Continuous action spaces

## License

MIT License - Feel free to use and modify!

## Contributing

Contributions welcome! Feel free to:
- Add new environments
- Implement additional RL algorithms
- Improve visualizations
- Add more educational content

---

**Happy Learning! 🚀**
