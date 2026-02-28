# HT-MOTR
**HT-MOTR: End-to-End Multi-Object Tracking with Hierarchical Matching and Temporal Guidance**

<p align="center">
    <img src="https://i.imgur.com/waxVImv.png" alt="Oryx Video-ChatGPT">
</p>

#### [Yuhao Li](), [Jinqiu Sun](https://teacher.nwpu.edu.cn/m/2009010133), [Yu Zhu]() and [Yanning Zhang](https://jszy.nwpu.edu.cn/1999000059)


#### **Northwestern Polytechnical University**

## Latest 
- `2026/02/22`: Our work has been accepted by IEEE TMM. Our code and models are coming soon!

<br>
<details>
  <summary>
  <font size="+1">Abstract</font>
  </summary>
End-to-end multi-object tracking (MOT) methods often suffer from imbalanced training between detection and tracking queries, primarily caused by the one-by-one label assignment mechanism. A common solution involves either introducing an additional detection decoder or applying detection-specific supervision. However, the former substantially increases computational overhead, while the latter may result in unstable optimization due to implicit matching competition between detection and tracking queries.
In this paper, we present HT-MOTR, a real-time end-to-end MOT framework that achieves a better balance between accuracy and efficiency. HT-MOTR introduces two key components: Proposal-Guided Hierarchical Matching (PHM) and Tracking-Conditioned Guided Decoding (TCGD). In PHM, we first generate initial detection queries based on the output proposals of an efficient hybrid encoder. Then, we perform progressive matching for detection and tracking queries at different decoder layers: 
early detection-prioritized matching, middle joint matching, and final tracking-prioritized matching. The TCGD module further enhances detection queries with temporal information derived from tracking queries. Specifically, tracking queries first attend to encoder features via cross-attention, and the resulting temporally enriched queries subsequently guide detection queries through self-attention before interacting with visual features.
Extensive experiments demonstrate the effectiveness of our approach. HT-MOTR achieves 66.5\% HOTA on DanceTrack and runs at  a real-time speed of 26.7 FPS, thus validating both its robustness and efficiency. 
</details>


## Citation
if you use our work, please consider citing us:
```BibTeX
@ARTICLE{HTMOTR,
  author={Li, Yuhao and Sun, Jinqiu and Zhu, Yu and Zhang, Yanning},
  journal={IEEE Transactions on Multimedia}, 
  title={HT-MOTR: End-to-End Multi-Object Tracking with Hierarchical Matching and Temporal Guidance}, 
  year={2026},
  }


```


## License
This project is released under the Apache license. See [LICENSE](LICENSE) for additional details.
## Acknowledgement
The code is mainly based on [RT-DETR](https://github.com/lyuwenyu/RT-DETR) and [MOTR](https://github.com/megvii-research/MOTR). Thanks for their wonderful works.
