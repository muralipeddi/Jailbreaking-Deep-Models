Methology: 
1. **Model Selection**
    
    Chose a pretrained ResNet-34 model trained on a 100-class subset of ImageNet-1K as the primary target for adversarial attacks.
    
2. **Baseline Evaluation**
    
    Assessed the model’s clean performance using top-1 and top-5 accuracy as baseline metrics.
    
3. **FGSM Implementation**
    
    Applied the Fast Gradient Sign Method (FGSM) to generate single-step $L_\infty$ perturbations with ε = 0.02 to evaluate initial vulnerability.
    
    ![image.png](attachment:4061d93e-a4bf-467e-ae99-9b059a7281ac:image.png)
    
4. **Multi-step Attack Design**
    
    Developed stronger adversarial examples using iterative gradient-based attacks under $L_\infty$ budgets up to ε = 0.5, optimizing for maximum degradation with minimal distortion.
    
    ![image.png](attachment:cdeb5b86-a89b-4bb9-b14b-071dae55c9e0:image.png)
    
5. **Patch-based Attack Generation**
    
    Introduced fixed-size (32×32) patch attacks, concentrating adversarial perturbations in a localized region to bypass spatial defenses and simulate realistic tampering.
    
    ![image.png](attachment:34f875c9-ce00-46b2-84c3-e51429a2664d:image.png)
    
6. **Transferability Testing**
    
    Evaluated cross-model generalization by applying adversarial examples generated for ResNet-34 on a DenseNet-121 model to observe attack transferability.
    
7. **Robustness Analysis**
    
    Measured performance drop in both models and analyzed the relationship between attack strength, perceptual distortion, and model architecture sensitivity.
