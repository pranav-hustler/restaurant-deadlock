# 🍳 Restaurant Kitchen Deadlock Simulator

An interactive web-based educational tool that demonstrates operating system deadlock concepts using a familiar restaurant kitchen analogy.

## 🎯 Project Overview

This simulator visualizes deadlock in operating systems through an intuitive restaurant kitchen scenario where chefs (processes) need utensils (resources) to cook. When circular wait occurs, the kitchen "freezes" - demonstrating deadlock in action!

## 📚 Educational Value

**Concepts Demonstrated:**
- **Four Necessary Conditions for Deadlock:**
  1. Mutual Exclusion - Only one chef can use a utensil at a time
  2. Hold and Wait - Chefs hold one utensil while waiting for another
  3. No Preemption - Utensils cannot be forcefully taken
  4. Circular Wait - Chef A waits for Chef B, who waits for Chef C, who waits for Chef D, who waits for Chef A

**Deadlock Prevention Methods:**
- Resource Ordering (Numbered utensil request protocol)
- Timeout Method (Release resources after waiting too long)
- Banker's Algorithm (Safe state verification before allocation)

## ✨ Features

- **Interactive Drag-and-Drop:** Assign utensils to chefs by dragging
- **Real-Time Deadlock Detection:** Algorithm detects circular wait automatically
- **Visual Feedback:** Kitchen "freezes" with red alert when deadlock occurs
- **Prevention Method Explanations:** Learn three different prevention strategies
- **Automatic Deadlock Scenario:** Click button to see deadlock form step-by-step
- **Status Tracking:** Real-time display of all four deadlock conditions

## 🚀 Live Demo

👉 **[Try it Live!](https://pranav-hustler.github.io/restaurant-deadlock/)**

## 🛠️ Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with animations (gradients, keyframes, transitions)
- **Vanilla JavaScript** - All logic (no frameworks!)
- **HTML5 Drag and Drop API** - Interactive utensil assignment

## 📸 Screenshots

### Initial State
Clean kitchen with 4 chefs and 4 utensils ready to be assigned.

### Deadlock Detected!
All chefs holding one utensil and waiting for another - circular wait forms a cycle.

### Prevention Methods
Interactive modals explaining resource ordering, timeout, and Banker's algorithm.

## 💻 Installation & Usage

### Option 1: Quick Start (No Installation)
1. **Clone the repository:**
```bash
   git clone https://github.com/YOUR_USERNAME/restaurant-deadlock-simulator.git
```

2. **Open in browser:**
```bash
   cd restaurant-deadlock-simulator
   open index.html
```

That's it! No dependencies, no build process, no server needed.

### Option 2: GitHub Pages
Just visit the live demo link above!

## 🎮 How to Use

### Creating Deadlock Manually:
1. **Drag utensils to chefs:**
   - Drag 🔪 Knife to Chef A
   - Drag 🍳 Pan to Chef B
   - Drag 🥄 Spatula to Chef C
   - Drag 🥣 Bowl to Chef D

2. **Watch the deadlock form:**
   - Each chef holds one utensil but needs another
   - All chefs enter "Waiting" state
   - Circular wait condition is met
   - 🚨 DEADLOCK ALERT appears!

### Automatic Deadlock:
- Click **"⚠️ Create Deadlock"** button
- Watch automated scenario create deadlock step-by-step

### Learning Prevention:
- Click any prevention method button:
  - 📋 **Resource Ordering** - Always request in fixed order
  - ⏱️ **Timeout Method** - Release after waiting too long
  - 🏦 **Banker's Algorithm** - Only allocate if safe state remains

### Reset:
- Click **"🔄 Reset Kitchen"** to start fresh

## 🧠 Core Concepts Explained

### Deadlock Detection Algorithm
```javascript
function checkDeadlock():
    waitingCount = 0
    allHaveOne = true
    
    for each chef:
        if chef is waiting:
            waitingCount++
        if chef has 0 utensils:
            allHaveOne = false
    
    if waitingCount == 4 AND allHaveOne:
        DEADLOCK DETECTED!
```

**Logic:** Deadlock exists when ALL chefs are waiting AND each holds at least one resource (proving circular wait).

### Why Restaurant Analogy?
- **Tangible:** Everyone understands kitchens and cooking
- **Visual:** Utensils and chefs are easy to visualize
- **Relatable:** "Waiting for resources" makes intuitive sense
- **Memorable:** Concrete examples stick better than abstract process IDs

## 🎓 Educational Context

**Project Type:** Interactive Learning Showcase - FJ2  
**Course:** Operating Systems (Unit 3)  
**Topics Covered:**
- System Model (Processes & Resources)
- Deadlock Characterization (Four Conditions)
- Methods for Handling Deadlocks
- Deadlock Prevention Strategies

**Learning Outcomes:**
- Visual understanding of circular wait
- Recognition of deadlock conditions in real-time
- Appreciation of prevention method trade-offs
- Hands-on experimentation with resource allocation

## 👥 Team

**Developed by:**
- **Pranav Gonuguntla** 

## 🤝 Contributing

This is an educational project, but suggestions are welcome!

**To contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Future Enhancements

- [ ] Add more chefs and utensils (scalability testing)
- [ ] Implement actual prevention algorithms interactively
- [ ] Add resource allocation graph visualization
- [ ] Include process state diagrams
- [ ] Add sound effects for immersion
- [ ] Multi-language support
- [ ] Mobile-responsive improvements
- [ ] Save/load scenarios

## 📄 License

MIT License - Feel free to use for educational purposes!

## 📚 References

- Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). *Operating System Concepts* (10th ed.). Wiley.
- Tanenbaum, A. S., & Bos, H. (2014). *Modern Operating Systems* (4th ed.). Pearson.
- Course Materials: Operating Systems - Unit 3

## 🔗 Related Projects

- [CPU Scheduling Visualizer](https://github.com/pranav-hustler/cpu-scheduling-visualizer) - Interactive visualization of CPU scheduling algorithms


**⭐ Star this repo if you found it helpful for learning OS concepts!**

Made with ❤️ for Operating Systems education
EOF
