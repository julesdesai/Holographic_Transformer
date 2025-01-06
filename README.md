(THIS IS V1 - AN IMPROVED V2 IS UNDER DEVELOPMENT)

# Holographic_Transformer
Sandbox for string-theory/holographic inspired attention experiment (WIP!) This project implements and compares a novel holographic attention mechanism inspired by string theory with standard transformer attention.

# Overview
The holographic attention mechanism processes information at multiple scales simultaneously, similar to how holography in string theory maps between different dimensional representations. In this implementation, we compare its performance with standard transformer attention on time series data containing patterns at multiple time scales.

I am exploring a novel attention mechanism called "Holographic Attention" that's inspired by principles from holographic theories in physics, particularly the AdS/CFT correspondence. The core theoretical motivation comes from how information is organized in holographic systems.

# Theoretical Background:
In holographic theories like AdS/CFT, information about a bulk region of spacetime can be encoded on its boundary in a specific way: information at different radial distances from the boundary corresponds to different scales of organization in the boundary theory. As you move deeper into the bulk (increasing radial coordinate), you capture increasingly coarse-grained or long-range features of the boundary theory.

# Approach:
I'm implementing this principle in neural networks through a modified attention mechanism that explicitly handles information at different scales. Instead of treating all attention equally, our mechanism:

- Processes information at multiple discrete scales simultaneously
- Uses a geometric weighting inspired by the AdS metric
- Allows different scales to interact through learned mixing parameters

# Features:

- Each scale has its own attention pattern
- Lower scales capture local, fine-grained relationships
- Higher scales capture global, coarse-grained relationships
- The scales are mixed through learned parameters that determine how information at different scales should be combined

# Plausible Expected Advantages:

- More efficient handling of hierarchical structure
- Better capture of multi-scale relationships
- Natural handling of both local and global dependencies
- Potentially better scaling with sequence length due to the hierarchical organization


# Key Components

Holographic Attention

- Multiple scale-dependent attention mechanisms
- Geometric weighting based on scales
- Scale mixing through learned parameters


# Current Test Framework: Time Series Dataset

- Synthetic data with multiple frequency components
- Patterns at different timescales (fast, medium, slow)
- Binary classification task based on future volatility


# Model Architectures

- HolographicTransformer: Uses our custom attention mechanism
- StandardTransformer: Uses classic transformer attention

# Required packages
pip install torch
pip install pytorch-lightning
pip install numpy
