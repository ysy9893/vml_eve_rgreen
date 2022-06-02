# CycleGAN_summary

- The model
    
    ![Untitled](CycleGAN_summary%20b64f9f84a8f546049ca1690ac2cce399/Untitled.png)
    
- Goal:
    
    ![Untitled](CycleGAN_summary%20b64f9f84a8f546049ca1690ac2cce399/Untitled%201.png)
    
    ![Untitled](CycleGAN_summary%20b64f9f84a8f546049ca1690ac2cce399/Untitled%202.png)
    
- Loss Breakdown:
    - Adversarial Loss
        
        ![Untitled](CycleGAN_summary%20b64f9f84a8f546049ca1690ac2cce399/Untitled%203.png)
        
    - Cycle Consistency Loss
        
        ![Untitled](CycleGAN_summary%20b64f9f84a8f546049ca1690ac2cce399/Untitled%204.png)
        
        - Forward cycle consistency + backward cycle consistency
            - with large enough capacity, a network can map the same
            set of input images to any random permutation of images in
            the target domain, where any of the learned mappings can
            induce an output distribution that matches the target distribution. Thus, adversarial losses alone cannot guarantee that the learned function can map an individual input xi to a desired output yi.
            - To further reduce the space of possible mapping functions, the authors argue functions should be cycle consistent.