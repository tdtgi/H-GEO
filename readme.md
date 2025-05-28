The problem texts of the dataset are included in ​​FTtrain.json​​ and ​​FTtest.json​​.
# H-GEO
H-GEO is a dataset of images and Chinese text featuring geometry problems, LLM errors, and their corrections. It supports fine-tuning to reduce hallucinations in geometric reasoning.
# JSON structure
```json
{
    "messages": [
      {
        "content": "这是一个数学问题和它的一个错误答案。问题：如图,A、D是⊙O上的两个点,BC是直径,若∠OAC=55°,则∠D的度数是() 错误答案：解：∵OA=OC，∴∠C=∠OAC=55°．∵BC是⊙O的直径，∴∠B=90°．∴∠BOC=180°-∠C-∠B=180°-55°-90°=35°．∴∠D=$\\\\frac{1}{2}$∠BOC=$\\\\frac{1}{2}$×35°=17.5°．故答案为：17.5°．。请结合图片分析这个错误答案，把它拆分成推理和计算两个部分，并指出错误所在的部分，给出错误的语句段落，并给出这道错题的修正。最后给出这道题的正确答案。",
        "role": "user"
      },
      {
        "content": "错误答案推理部分：∵OA=OC，因此∠OAC和∠OCA相等，从而可以计算∠AOC的度数，进而应用圆周角定理求出∠B和∠D的度数。 错误答案的计算部分：∴∠BOC=180°-∠C-∠B=180°-55°-90°=35°．∴∠D=$\\frac{1}{2}$∠BOC=$\\frac{1}{2}$×35°=17.5° 错误所在的部分：calculate 。错误的语句段落：∴∠D=$\\frac{1}{2}$∠BOC=$\\frac{1}{2}$×35°=17.5° 。这道错题的修正：解:∵OA=OC,∴∠OCA=∠OAC=55°,∴∠AOC=180°-∠OCA-∠OAC=70°,由圆周角定理得,∠B=$\\frac{1}{2}$∠AOC=35°,∴∠D=∠B=35°。这道题的正确答案为：解:∵OA=OC,∴∠OCA=∠OAC=55°,∴∠AOC=180°-∠OCA-∠OAC=70°,由圆周角定理得,∠B=\\frac{1}{2}∠AOC=35°,∴∠D=∠B=35° ",
        "role": "assistant"
      }
    ],
    "images": [
      "Data/GeoQA/tetximage/2581.png"
    ]
  }
```
# containing 
- FTtrain.json:3944

- FTtest.json:327

- images:3742

(The original questions for some of the wrong answers are the same.)

# License
This dataset is licensed under the MIT License.
