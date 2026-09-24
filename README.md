# Net Detective #
Runs locally on a host and flags malicious connections to it in real time. Packets get turned into flows, and an ML model sorts each flow into benign or malicious.

### Brainstorming ###
1) First milestone we should aim to reach is to be able to process a network dump file, and sort from logged connections which one is malicious and which is not.
2) Then test on our own traffic (a VM lab for attacks), and make it run live.

### Resources ###
- https://github.com/stratosphereips/stratospherelinuxips
- https://github.com/sanjaybalaji014/LINDEF-Lightweight-Real-Time-Network-Intrusion-Detection-and-Containment-Framework 
- https://github.com/cstub/ml-ids
- https://arxiv.org/pdf/2506.19877v1 -> paper that uses CICIDS2017 and compares how different ML models "perform" in anomaly detection, could be useful when deciding architecture
- https://onlinelibrary.wiley.com/doi/10.1155/2023/6048087
- https://github.com/lisa-lt/CICFlowMeter

### Datasets ###
- Improved CICIDS2017 / CSE-CIC-IDS2018 (remade with the fixed CICFlowMeter)
- UNSW-NB15
- Kitsune / IoT-23 ( more to do with IoT, maybe worth exploring (~_^) )


### Notes ###
1) Dataset (improved CICIDS2017)  
The original CICFlowMeter had bugs, https://github.com/lisa-lt/CICFlowMeter is the fixed one. We use it and the improved dataset so both match.  
Improved datasets: https://intrusion-detection.distrinet-research.be/CNS2022/Datasets/ (CICIDS2017_improved.zip), put them in data/.
