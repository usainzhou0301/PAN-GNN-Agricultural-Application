# PAN-GNN-Agricultural-Application
This repository is used to showcase the code and simulation results for the paper "A Feature-Driven Reinforcement Learning-Based UAV System for Agricultural Data Collection." We will update the whole experiment code after acceptance. Now, we just put the simulation results for algorithms EI-PAN and EI-GNN.


# Code-Structure
After the paper is accepted, we will update the code as follows:
```bash
simulation
│   ├── communication.py                         # UAV-WS (Wireless Station) communication logic
│   ├── ws_generation.py                         # Generator for spatial WS distributions
│   ├── physical_model.py                        # UAV dynamics and energy model for agriculture
│   ├── terrain.py                               # Procedural terrain generation
│   ├── EAC-PAN/                                 # PAN-based learning for dual agricultural UAV tasks
│   │   ├── outputs_visit/                       # Output for visitation subtask
│   │   │   ├── photos/                          # Visual outputs
│   │   │   ├── 2Dpath/                          # Trajectory visualizations
│   │   │   ├── 3Dpath/                          # Trajectory visualizations
│   │   │   └── results/                         # Evaluation metrics
│   │   ├── outputs_return/                      # Output for return subtask
│   │   │   ├── photos/                          # Visual outputs
│   │   │   ├── 2Dpath/                          # Trajectory visualizations
│   │   │   ├── 3Dpath/                          # Trajectory visualizations
│   │   │   └── results/                         # Evaluation metrics
│   │   ├── model/                               # Trained PAN model weights
│   │   ├── feature_extraction.py                # PAN training script
│   │   ├── pointarray_feature_extractor.pth     # Trained extractor weights
│   │   ├── sample_for_return.py                 # Dataset preparation for BPN
│   │   ├── pre-train-predict.py                 # Energy predictor training
│   │   ├── energy_predictor.pth                 # Trained BPN model
│   │   ├── time-print.py                        # Inference time evaluation
│   │   ├── visit_env.py                         # Environment for visitation task
│   │   ├── return_env.py                        # Environment for return task
│   │   ├── main_env.py                          # Combined UAV task environment
│   │   ├── agri_eac_pan_model.py                # PAN + RL structure for agriculture
│   │   ├── visit_train.py                       # Subtask-specific training
│   │   ├── return_train.py                      # Subtask-specific training
│   │   ├── main_train.py                        # Full task training
│   │   ├── visit_test.py                        # Subtask evaluation
│   │   ├── return_test.py                       # Subtask evaluation
│   │   └── main_test.py                         # Full task evaluation
│   └── EAC-GNN/                                 # GNN-based UAV control in agriculture
│       ├── outputs_visit/                       # Same structure and purpose as PAN variant
│       ├── outputs_return/                      # Same structure and purpose as PAN variant
│       ├── model/                               # GNN model weights
│       ├── sample_for_return.py                 # Dataset preparation
│       ├── pre-train-predict.py                 # BPN training
│       ├── energy_predictor.pth                 # Trained BPN weights
│       ├── time-print.py                        # Timing analysis
│       ├── visit_env.py                         # Environment simulations
│       ├── return_env.py                        # Environment simulations
│       ├── main_env.py                          # Environment simulations
│       ├── agri_eac_gnn_model.py                # GNN-RL model
│       ├── visit_train.py                       # Subtask & full training
│       ├── return_train.py                      # Subtask & full training
│       ├── main_train.py                        # Subtask & full training
│       ├── visit_test.py                        # Subtask & full evaluation
│       ├── return_test.py                       # Subtask & full evaluation
│       └── main_test.py                         # Subtask & full evaluation
```

# Simulation Results
EI-PAN/3d-trajectories-visualization/ and EI-GNN/3d-trajectories-visualization/ store the 3D visualization figure result of the algorithm EI-PAN and GNN. The i.html means the i-th scenario. In the paper, we choose the 0th terrain as scenario 1 and the 8th terrain as scenario 2. The HTML file we generated opens a 3D model of the trajectories, which can be dragged, zoomed, and rotated, allowing convenient observation of both the trajectories and the terrain.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e9420dea-ca55-45f0-a8b3-55778057615c" width="500" height="500" />
</p>
<p align="center"><b>Figure: EI-PAN 2D trajectories result for 1st terrain</b></p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/eb68d7ae-bc3b-4adf-abf1-28094b8ac96b" width="500" height="500" />
</p>
<p align="center"><b>Figure: EI-GNN 2D trajectories result for 1st terrain</b></p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f650de39-14a1-4b0e-ad77-b9c17e23459e" width="1200" height="600" />
</p>
<p align="center"><b>Figure: EI-PAN 3D trajectories result for 1st terrain</b></p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/5bfbcc69-ec40-4abf-87c4-32f2b6b8d6d1" width="1200" height="600" />
</p>
<p align="center"><b>Figure: EI-GNN 3D trajectories result for 1st terrain</b></p>



# Updates
``` Oct, 25, 2025: ``` Paper Submission.
