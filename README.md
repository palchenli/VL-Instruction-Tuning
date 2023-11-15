# Vision-Language Instruction Tuning: A Review and Analysis

---

## 📆 Schedule

- ⬜️ Release New Instruction Data ... (circulation)
- ⬜️ Release Construction Tools
- ⬜️ Release Instruction Data
- ☑️ [2023.11.15] Paper Released ([ArXiv](https://arxiv.org/abs/2311.08172))

## 🗒️ Existing VLIT Dataset

| Dataset | MLLM | G | R | I | Paper |
| :--- | :--- | :---: | :---: | :---: | :---:|
| LLaVA_instruct_150K | LLaVA | ✔︎ | ✔︎ | ✗ | [Visual Instruction Tuning](https://github.com/palchenli/VL-Instruction-Tuning/blob/main/assert/papers/Visual%20Instruction%20Tuning.pdf) |

## 📂 Multi-Modal Instruction Data Constructed in This Paper

In this paper, we propose a vision-language instruction construction pipeline and generate a corresponding dataset.
Specifically, the generated instruction data is a multi-round question answering about a given image.
Here are some examples of the generated instruction data:

### Examples

| Image | Conversation |
| :--- | :--- |
| <img src="./assert/images/COCO_train2014_000000288586.jpg" width="200%"/> | User: Can you describe the scene in the image?<br>AI: Sure, the image captures a large grizzly bear wading through a moving river. The bear has a brown coat and appears to be quite large and furry. It's currently not holding anything in its mouth and it doesn't seem to have caught any fish from the river.<br>User: Are grizzly bears typically found in such environments?<br>AI: Yes, indeed. Grizzly bears are often found near rivers or streams. They are excellent swimmers and often go into the water in search of food. During salmon spawning seasons, they are known to frequent river areas to catch the fish.<br>User: Is the bear possibly looking for food?<br>AI: That's a strong possibility. While there are no fish present in the river in the image, grizzly bears are known to forage for various food sources in rivers, including fish and other aquatic organisms. However, without further context, it's hard to say definitively.<br>User: What other characteristics does a grizzly bear have?<br>AI: Grizzly bears, which are a subspecies of brown bear, are known for their size, strength, and excellent swimming ability. They have a distinct hump over their shoulders which is a muscle mass used for digging and clawing. Their fur color can vary from very light tan to dark brown, with the fur on their back often being darker than the rest of their body. Also, despite their large size, grizzlies are quite fast and can run at speeds of up to 30 miles per hour. |
| <img src="./assert/images/COCO_train2014_000000030722.jpg" width="200%"/> | User: What is the main animal in the picture?<br>AI: The main animal in the picture is a giraffe.<br>User: What is the giraffe doing?<br>AI: The giraffe is standing next to a tree and some rocks. It's not doing much, just hanging around.<br>User: Is the giraffe standing on the rocks?<br>AI: No, the giraffe is not standing on the rocks. It is standing next to them.<br>User: Can you describe the setting in more detail?<br>AI: The picture mainly focuses on the giraffe, a tree, and some rocks. The giraffe is standing right next to the tree. There are rocks scattered around them.<br>User: Are there any elephants in the picture?<br>AI: No, there are no elephants in this picture. Only a single giraffe is present.<br>User: Are there any unique features of the giraffe?<br>AI: As per the details provided in the image, the giraffe is standing and has a spotted pattern on its skin, which is a characteristic feature of giraffes.<br>User: Is the giraffe sitting on the rocks?<br>AI: No, the giraffe is not sitting on the rocks. It's standing by them.<br>User: Is the giraffe eating the tree leaves?<br>AI: There's no indication in the image that the giraffe is eating the leaves of the tree. It's simply standing beside it.<br>User: Where do giraffes usually live?<br>AI: Giraffes are native to Africa and they usually inhabit savannas, grasslands, and open woodlands. However, in this particular image, the exact location isn't specified. |
| <img src="./assert/images/COCO_train2014_000000247884_0.jpg" width="200%"/> | User: Is there a car in the picture?<br>AI: Yes, there is a car in the picture and it appears to be parked.<br>User: What can you tell me about the car?<br>AI: Based on the image, the car is parked, which suggests that it is not currently in use. However, I can't provide specifics about its make, model, or color without more visual information.<br>User: Do you think the car is related to the boy on the skateboard?<br>AI: It's hard to definitively state a connection between the car and the boy on the skateboard based on the image alone. The car may belong to someone who is watching the boy, or it may just be parked in the vicinity where the boy is skateboarding.<br>User: Is the car moving?<br>AI: No, the car isn't moving. It's parked.<br>User: Could the car potentially pose a danger to the skateboarder?<br>AI: Since the car is parked, it's unlikely to pose a direct threat to the skateboarder. However, any vehicle, parked or moving, in the vicinity of skateboarders could potentially become a hazard, especially if the skateboarder loses control. This emphasizes the importance of skateboarding in safe, designated areas.<br>User: Is the car possibly there for a skateboarding event?<br>AI: Based on the information available, I can't definitely say if the car is there for a skateboarding event. It could belong to a spectator or participant, or it could be unrelated to the skateboarding activity. More context would be needed to make a clear conclusion. |

There are three different types of instruction data. The data statistics and download links are as follows.

### Download Links

| Data Type | Baidu CLoud | Google Drive |
| :--- | :---: | :---: |
| COCO_2014_Images | [url](https://cocodataset.org/) | [url](https://cocodataset.org/) |
| Global | [url](https://pan.baidu.com/s/15Ge_lwge-YOxL55_0roOfA?pwd=inok) | [url](https://drive.usercontent.google.com/download?id=1rEzH0RhWqjq8W6zXc-t8Q3Tg3ncB1dpN&export=download&authuser=0&confirm=t&uuid=f574c321-ad4c-438e-94a6-8790db70c58f&at=APZUnTVglRBUCUC6tax-d3OH33Io:1700050876759) |
| Negative | [url](https://pan.baidu.com/s/1wuCkm443ufpG3-xcHVrRNA?pwd=auc7) | [url](https://drive.usercontent.google.com/download?id=1sQurFP7M_Ftd2Q5NSZm41_PCMT4ECd0g&export=download&authuser=0&confirm=t&uuid=fb82922c-0fd0-4b47-a5f1-af70f4d1b300&at=APZUnTUOOoYjM2gAhK79wsUkKUFk:1700051467871) |
| Region | [url](https://pan.baidu.com/s/15m1RMpeirEz83Jsxd8zC0w?pwd=96p5) | [url](https://drive.usercontent.google.com/download?id=1Qbk4cOfTcrsPx7k1rD0E20hTkdhYNfBU&export=download&authuser=0&confirm=t&uuid=6fa256d3-e085-4089-9073-11799a7b3b74&at=APZUnTXdeLntbNQeEWgpD7SvulsM:1700051759650) |
| Region_Images | [url]() | [url]() |


### Data Format

```json
{
    "image_source": "",
    "construction_time": "",
    "annotations": [
      {
        "img_ids": "",
        "instruction_type": "",
        "conversations": []
      },
      
      {
        "img_ids": "",
        "instruction_type": "",
        "conversations": []
      }
    ]
}
```



## 📎 Citation
If you found this repository useful, please consider citing:

```
@article{li2023visionlanguage,
      title={Vision-Language Instruction Tuning: A Review and Analysis}, 
      author={Chen Li and Yixiao Ge and Dian Li and Ying Shan},
      year={2023},
      eprint={2311.08172},
      archivePrefix={arXiv},
      primaryClass={cs.MM}
}
```

## 👍🏻 Acknowledgement

We would like to thank [LLaVA](https://github.com/haotian-liu/LLaVA), [LAVIS](https://github.com/salesforce/LAVIS) and [OpenFlamingo](https://github.com/mlfoundations/open_flamingo) for their well-architcated multi-modal LLMs.
Thanks to [SEED-Bench](https://github.com/AILab-CVC/SEED-Bench) for being an open source and convenient benchmark for evaluating MLLMs.