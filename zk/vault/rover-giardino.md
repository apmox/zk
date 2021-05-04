---
id: d0a0298c-25fe-4abe-820f-d7f2148502db
title: Rover Giardino
desc: ''
updated: 1620141796218
created: 1620137488587
---

# Progetto drone giardino casa

Framework generali:
- ROS
- Ardupilot

## Missione preimpostata
- Mission Planner https://ardupilot.org/planner/docs/mission-planner-overview.html

## SLAM
**Mathieu Labbe** grandissimo ricercatore di SLAM per esterno

### Stereocamera
Cosa mi posso aspettare da una stereocamera su un rover?
- Video dimostrativo https://www.youtube.com/watch?v=qpTS7kg9J3A
- Setup ROS https://wiki.ros.org/rtabmap_ros/Tutorials/StereoOutdoorMapping

### RGBD tipo Kinect
Come calibro il Kinect bene bene?
- F. Basso, E. Menegatti and A. Pretto,“Robust Intrinsic and Extrinsic Calibration of RGB-D Cameras”, in IEEE Transactions on Robotics, vol. 34, no. 5, 2018. [arXiv](https://arxiv.org/pdf/1701.05748.pdf), [IEEE](https://ieeexplore.ieee.org/document/8423784), [SciHub](https://scihub.unblockit.onl/https://ieeexplore.ieee.org/document/8423784)

SLAM con Kinect?
- https://github.com/Choitek/mmmros-docs/blob/master/tutorials/kinect.md

## Localizzazione alternativa
- Beacon radio che permettono trilaterazione, concept spiegato a grandi linee http://grauonline.de/wordpress/?page_id=467

Articolo che spiega concetti da leggere meglio
- BULUSU, Nirupama; HEIDEMANN, John; ESTRIN, Deborah. GPS-less low-cost outdoor localization for very small devices. IEEE personal communications, 2000, 7.5: 28-34. [Paper](https://www.isi.edu/~johnh/PAPERS/Bulusu00a.pdf)

Marvelmind Robotics, ditta che fa praticamente solo questo:
- https://marvelmind.com/
- Video dimostrativo localizzazione con beacon https://www.youtube.com/watch?v=rjcnDvrS7yk

## Localizzazione generale
Lezioni di Cyrill Stachniss super utili https://www.youtube.com/c/CyrillStachniss/videos per i concetti di base, ma in generale guardare:
- SLAM https://www.youtube.com/watch?v=uHbRKvD8TWg
- Monte Carlo  [Particle Filter MATLAB](https://www.youtube.com/watch?v=NrzmH_yerBU)
- Libreria trovata linkata https://github.com/borglab/gtsam