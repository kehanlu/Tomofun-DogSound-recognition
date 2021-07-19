# Tomofun-DogSound-recognition

**Blog post**
- [Tomofun 狗音辨識挑戰賽：初賽資料處理與模型(Top10%)](http://blog.hanklu.tw/post/2021/tomofun-dogsound-recognition-competetion-1/)
- Tomofun 狗音辨識挑戰賽：決賽 MLops 與心得 `WIP`

**初賽**

Data Augmentation + ResNet18

|                     | Public Test | Private Test | Rank<br>(301 teams) |
|---------------------|------------:|-------------:|----------------:|
| My model            | 0.97697     | 0.98060      | 30*             |
| My teammate's model | **0.97702**     | **0.98272**      | **22**  |

*\*Rank 30是指直接從 Fianl Leaderboard 看這個分數在第幾名。*

**決賽**

AWS MLOps

|             | Rank |          AUC | Response Success Rate |
|-------------|-----:|-------------:|----------------------:|
|  Test round |   15 | 0.8352815001 |               100.00% |
| Final round |    9 | 0.9373086568 |               100.00% |

---

## Structure

Model: 初賽模型

incremental-training: 決賽 MLOps `WIP`

```
.
├── Model
│   └── Dataset
│       ├── augmented
│       │   ├── 0.9
│       │   │   ├── public_test
│       │   │   └── train
│       │   ├── 1.1
│       │   │   ├── public_test
│       │   │   └── train
│       │   └── noise
│       │       ├── public_test
│       │       └── train
│       ├── musan
│       │   └── noise
│       │       └── sound-bible
│       ├── public_test
│       └── train
└── incremental-training
```


## Acknowledgement

The model code is based on [daisukelab/sound-clf-pytorch](https://github.com/daisukelab/sound-clf-pytorch)
