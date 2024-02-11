# Stack Overflow Question Classifier

## Overview
This classifier receives as input various questions from Stack Overflow, and based on its contents it classifies regarding the programming language it is reffering to.
For this dataset, only 4 programming languages were used, those being Python, Java, Javascript and C#.

## Results
* Accuracy = 73%

## Example
Classes: ['Python', 'Java', 'Javascript', 'Csharp']
```
examples = [
  "define class Class: raises an error", #python
  "Why does array.splice() not work?", #javascript
  "system out println does not print the whole object" #java
]

export_model.predict(examples)
```

```
array([[0.5715747 , 0.50944954, 0.50808805, 0.42675626],
       [0.5194486 , 0.44043493, 0.57837814, 0.4638172 ],
       [0.5129216 , 0.45258072, 0.5503089 , 0.49067435]], dtype=float32)
```
As can be seen, the first text is classified as Python, the second as Javascript and the third as Javascript.
