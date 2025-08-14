---
title: "DexSinGrasp: Learning a Unified Policy for Dexterous Object Singulation and Grasping in Cluttered Environments"
authors:
  - Lixin Xu$^{1^{*}}$
  - Zixuan Liu$^{1^{*}}$
  - Zhewei Gui$^{1}$
  - Jingxiang Guo$^{1}$
  - Zeyu Jiang$^{1}$
  - Zhixuan Xu$^{1}$
  - Chongkai Gao$^{1}$
  - Lin Shao$^{1}$
date: "2025-08-13T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2025-08-13T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

# Summary. An optional shortened abstract.
summary: ""
tags:
  -
featured: false

links:
  - name: Custom Link
    url: http://example.org
url_pdf: http://arxiv.org/pdf/1512.04133v1
url_code: "https://github.com/HugoBlox/hugo-blox-builder"
url_dataset: "#"
url_poster: "#"
url_project: ""
url_slides: ""
url_source: "#"
url_video: "https://nus-lins-lab.github.io/dexsingweb/static/data/DexSinGrasp.mp4"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: "Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)"
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

{{< video src="DexSinGrasp.mp4" controls="true" autoplay="false" loop="false" muted="false" playsinline="true" >}}

## Abstract

Grasping objects in cluttered environments remains a fundamental yet challenging problem in robotic manipulation. While prior works have explored learning-based synergies between pushing and grasping for two-fingered grippers, few have leveraged the high degrees of freedom (DoF) in dexterous hands to perform efficient singulation for grasping in cluttered settings. In this work, we introduce DexSinGrasp, a unified policy for dexterous object singulation and grasping. DexSinGrasp enables high-dexterity object singulation to facilitate grasping, significantly improving efficiency and effectiveness in cluttered environments. We incorporate clutter arrangement curriculum learning to enhance success rates and generalization across diverse clutter conditions, while policy distillation enables a deployable vision-based grasping strategy. To evaluate our approach, we introduce a set of cluttered grasping tasks with varying object arrangements and occlusion levels. Experimental results show that our method outperforms baselines in both efficiency and grasping success rate. Experimental results show that our method outperforms baselines in both efficiency and grasping success rate, particularly in dense clutter. Codes, appendix, and videos are available on our project website https://nus-lins-lab.github.io/dexsingweb/.

## Pipeline Overview

{{< figure src="pipeline.png" title="Framework of DexSinGrasp" >}}
Firstly, we employ clutter arrangement curriculum learning to progressively improve our teacher policy's performance, and acquire two teacher policies at the end of this stage for dense and random arrangement tasks, respectively. We then collect various state and action data along with pointcloud data from the trained two teachers to train a vision-based student policy via behavior cloning, which better facilitates real-world deployment.

## Cluttered Environments Generation

{{< figure src="cluttered_environment_generation.png" title="Dense and random arrangement settings" >}}
We introduce a cluttered environment generation module to create diverse object settings, including different obstacle quantities from 0 to 8, dense and random arrangements, various poses, and block shapes. For simplicity, we only show obstacles with numbers 4 to 8.

## Simulation Experiments

|             ![](s1.gif)             |             ![](s2.gif)             |             ![](s3.gif)             |
| :---------------------------------: | :---------------------------------: | :---------------------------------: |
| Dense arrangement with 4 obstacles  | Dense arrangement with 6 obstacles  | Dense arrangement with 8 obstacles  |
|             ![](s4.gif)             |             ![](s5.gif)             |             ![](s6.gif)             |
| Random arrangement with 4 obstacles | Random arrangement with 6 obstacles | Random arrangement with 8 obstacles |

## Real-World Experiments

|             ![](r1.gif)             |             ![](r2.gif)             |             ![](r3.gif)             |
| :---------------------------------: | :---------------------------------: | :---------------------------------: |
| Dense arrangement with 4 obstacles  | Dense arrangement with 6 obstacles  | Dense arrangement with 8 obstacles  |
|             ![](r4.gif)             |             ![](r5.gif)             |             ![](r6.gif)             |
| Random arrangement with 4 obstacles | Random arrangement with 6 obstacles | Random arrangement with 8 obstacles |

## BibTex

```bibtex
@article{xu2025dexsingrasp,
    title={DexSinGrasp: Learning a Unified Policy for Dexterous Object Singulation and Grasping in Cluttered Environments},
    author={Xu, Lixin and Liu, Zixuan and Gui, Zhewei and Guo, Jingxiang and Jiang, Zeyu and Xu, Zhixuan and Gao, Chongkai and Shao, Lin},
    journal={arXiv preprint},
    year={2025}
}
```
