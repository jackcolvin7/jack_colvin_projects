# Optimal Shot Tracker  

## Overview  
This project develops a framework for measuring **shot optimality** in soccer.  
Optimality is defined as a combination of:  

- **Shot Conversion** – how often shots from a given location or situation are scored (a proxy for xG).  
- **Shot Frequency** – how often players or teams actually get into those positions (a simplistic measure of how difficult they are to create).  

By combining these factors, the model provides insight into whether teams and players are more "optimal" when pursuing **many low-xG opportunities** or **fewer, harder-to-create high-xG chances**.  
Note: This project does not reject that having more overall xg is better, but rather asks the quesion **what is the best, easiest way to hit a given xg threshold?**

## Motivation  
Traditional xG models focus on shot quality, but they ignore the **creation difficulty** of those chances.  
For example:  
- A 0.35 xG shot might look ideal in isolation, but if such shots are created only once every few matches, is it optimal to design play solely around them? Should players wait to shoot for those moments, or maybe let it fly more often from range?   
- On the other hand, a team might consistently generate lower-xG shots, which individually seem less valuable but are more abundant and easier to produce.  

This project aims to quantify that trade-off by scaling shot quality with shot creation frequency.  

## Methodology  
1. **Data**: Shot-level data from open football datasets (location, context, outcome).  
2. **Optimality Measure**:  
   \[
   \text{Optimality} = \text{Shot Conversion} \times \text{Shot Frequency}
   \]  
   - Conversion ≈ xG proxy (likelihood of scoring).  
   - Frequency ≈ chance creation ease (how often shots from that situation occur).  
3. **Analysis**:  
   - Use **Radial Basis Function (RBF) interpolation** to evaluate optimality smoothly across pitch space.  
   - Compare strategies of high-volume/low-quality vs. low-volume/high-quality shooting.  

## Features  
- A simple yet powerful **optimality metric** grounded in xG theory.  
- **Visualization tools** to map where on the pitch shot-taking is most optimal.  
- Comparative analysis of different team or player strategies (Coming soon if enough data is found).  

## Future Work  
- Refine creation difficulty using possession length, buildup intensity, or tracking data.  
- Apply optimality scores to **player decision-making evaluation**.  
- Explore **team-level styles**, e.g., Liverpool’s shot volume vs. Manchester City’s chance quality.
- Note: these changes may require finding additional data that I currently do not have access to :(

## Requirements  
- Python 3  
- PyTorch  
- NumPy, Pandas, Matplotlib  
- Scikit-learn (for RBF interpolation)  

