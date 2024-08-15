

Classification Model: Deep Convolitional Model (2D-CNN)
======================================================
Model: "sequential"
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┓
┃ Layer (type)                         ┃ Output Shape                ┃         Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━┩
│ conv2d (Conv2D)                      │ (None, 30, 216, 32)         │             320 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ batch_normalization                  │ (None, 30, 216, 32)         │             128 │
│ (BatchNormalization)                 │                             │                 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ max_pooling2d (MaxPooling2D)         │ (None, 15, 108, 32)         │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dropout (Dropout)                    │ (None, 15, 108, 32)         │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ conv2d_1 (Conv2D)                    │ (None, 15, 108, 32)         │           9,248 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ batch_normalization_1                │ (None, 15, 108, 32)         │             128 │
│ (BatchNormalization)                 │                             │                 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ max_pooling2d_1 (MaxPooling2D)       │ (None, 7, 54, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dropout_1 (Dropout)                  │ (None, 7, 54, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ conv2d_2 (Conv2D)                    │ (None, 7, 54, 32)           │           9,248 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ batch_normalization_2                │ (None, 7, 54, 32)           │             128 │
│ (BatchNormalization)                 │                             │                 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ max_pooling2d_2 (MaxPooling2D)       │ (None, 3, 27, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dropout_2 (Dropout)                  │ (None, 3, 27, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ conv2d_3 (Conv2D)                    │ (None, 3, 27, 32)           │           9,248 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ batch_normalization_3                │ (None, 3, 27, 32)           │             128 │
│ (BatchNormalization)                 │                             │                 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ max_pooling2d_3 (MaxPooling2D)       │ (None, 1, 13, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dropout_3 (Dropout)                  │ (None, 1, 13, 32)           │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ flatten (Flatten)                    │ (None, 416)                 │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dense (Dense)                        │ (None, 128)                 │          53,376 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dropout_4 (Dropout)                  │ (None, 128)                 │               0 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dense_1 (Dense)                      │ (None, 16)                  │           2,064 │
└──────────────────────────────────────┴─────────────────────────────┴─────────────────┘
 Total params: 251,538 (982.57 KB)
 Trainable params: 83,760 (327.19 KB)
 Non-trainable params: 256 (1.00 KB)
 Optimizer params: 167,522 (654.39 KB)
 
Epoch Results:
  Epoch 1/100 
    Accuracy: 0.2276475727558136 - Loss: 2.1686925888061523
  Epoch 2/100 
    Accuracy: 0.3088107705116272 - Loss: 1.7895910739898682
  Epoch 3/100 
    Accuracy: 0.3819444477558136 - Loss: 1.6262516975402832
  Epoch 4/100 
    Accuracy: 0.4338107705116272 - Loss: 1.506516695022583
  Epoch 5/100 
    Accuracy: 0.4700520932674408 - Loss: 1.3983497619628906
  Epoch 6/100 
    Accuracy: 0.49609375 - Loss: 1.3227490186691284
  Epoch 7/100 
    Accuracy: 0.513671875 - Loss: 1.275539755821228
  Epoch 8/100 
    Accuracy: 0.5505642294883728 - Loss: 1.200803279876709
  Epoch 9/100 
    Accuracy: 0.5670573115348816 - Loss: 1.1504520177841187
  Epoch 10/100 
    Accuracy: 0.6009114384651184 - Loss: 1.0686497688293457
  Epoch 11/100 
    Accuracy: 0.6180555820465088 - Loss: 1.016761302947998
  Epoch 12/100 
    Accuracy: 0.6278212070465088 - Loss: 0.9752399921417236
  Epoch 13/100 
    Accuracy: 0.6473524570465088 - Loss: 0.9339731931686401
  Epoch 14/100 
    Accuracy: 0.662109375 - Loss: 0.9079882502555847
  Epoch 15/100 
    Accuracy: 0.6710069179534912 - Loss: 0.8713351488113403
  Epoch 16/100 
    Accuracy: 0.6898871660232544 - Loss: 0.8319925665855408
  Epoch 17/100 
    Accuracy: 0.6955295205116272 - Loss: 0.802574872970581
  Epoch 18/100 
    Accuracy: 0.7200520634651184 - Loss: 0.7589942216873169
  Epoch 19/100 
    Accuracy: 0.7358940839767456 - Loss: 0.7212258577346802
  Epoch 20/100 
    Accuracy: 0.7291666865348816 - Loss: 0.7189460396766663
  Epoch 21/100 
    Accuracy: 0.7508680820465088 - Loss: 0.6823564171791077
  Epoch 22/100 
    Accuracy: 0.7506510615348816 - Loss: 0.6736315488815308
  Epoch 23/100 
    Accuracy: 0.7690972089767456 - Loss: 0.6429782509803772
  Epoch 24/100 
    Accuracy: 0.7730034589767456 - Loss: 0.6084344387054443
  Epoch 25/100 
    Accuracy: 0.7825520634651184 - Loss: 0.5810645222663879
  Epoch 26/100 
    Accuracy: 0.7803819179534912 - Loss: 0.5917316675186157
  Epoch 27/100 
    Accuracy: 0.7947048544883728 - Loss: 0.5497120022773743
  Epoch 28/100 
    Accuracy: 0.7944878339767456 - Loss: 0.5609114170074463
  Epoch 29/100 
    Accuracy: 0.8038194179534912 - Loss: 0.5252879858016968
  Epoch 30/100 
    Accuracy: 0.8098958134651184 - Loss: 0.5108927488327026
  Epoch 31/100 
    Accuracy: 0.8220486044883728 - Loss: 0.48486486077308655
  Epoch 32/100 
    Accuracy: 0.8209635615348816 - Loss: 0.48551416397094727
  Epoch 33/100 
    Accuracy: 0.8229166865348816 - Loss: 0.47556236386299133
  Epoch 34/100 
    Accuracy: 0.8313801884651184 - Loss: 0.45062902569770813
  Epoch 35/100 
    Accuracy: 0.845703125 - Loss: 0.4288301467895508
  Epoch 36/100 
    Accuracy: 0.8422309160232544 - Loss: 0.42734450101852417
  Epoch 37/100 
    Accuracy: 0.8391926884651184 - Loss: 0.4248054325580597
  Epoch 38/100 
    Accuracy: 0.8634982705116272 - Loss: 0.39185577630996704
  Epoch 39/100 
    Accuracy: 0.8446180820465088 - Loss: 0.4330112338066101
  Epoch 40/100 
    Accuracy: 0.8587239384651184 - Loss: 0.3892257809638977
  Epoch 41/100 
    Accuracy: 0.8524305820465088 - Loss: 0.4024307429790497
  Epoch 42/100 
    Accuracy: 0.8576388955116272 - Loss: 0.39835745096206665
  Epoch 43/100 
    Accuracy: 0.8671875 - Loss: 0.35962188243865967
  Epoch 44/100 
    Accuracy: 0.8706597089767456 - Loss: 0.35180604457855225
  Epoch 45/100 
    Accuracy: 0.8726128339767456 - Loss: 0.35620009899139404
  Epoch 46/100 
    Accuracy: 0.8754340410232544 - Loss: 0.3442575931549072
  Epoch 47/100 
    Accuracy: 0.8836805820465088 - Loss: 0.32977479696273804
  Epoch 48/100 
    Accuracy: 0.8687065839767456 - Loss: 0.3475000858306885
  Epoch 49/100 
    Accuracy: 0.8856337070465088 - Loss: 0.3119128942489624
  Epoch 50/100 
    Accuracy: 0.8765190839767456 - Loss: 0.3390929400920868
  Epoch 51/100 
    Accuracy: 0.8825954794883728 - Loss: 0.3278539478778839
  Epoch 52/100 
    Accuracy: 0.8904079794883728 - Loss: 0.3129017651081085
  Epoch 53/100 
    Accuracy: 0.8871527910232544 - Loss: 0.32359012961387634
  Epoch 54/100 
    Accuracy: 0.8914930820465088 - Loss: 0.3135612905025482
  Epoch 55/100 
    Accuracy: 0.8949652910232544 - Loss: 0.29775893688201904
  Epoch 56/100 
    Accuracy: 0.8932291865348816 - Loss: 0.30473315715789795
  Epoch 57/100 
    Accuracy: 0.89453125 - Loss: 0.2957630455493927
  Epoch 58/100 
    Accuracy: 0.8927951455116272 - Loss: 0.28953486680984497
  Epoch 59/100 
    Accuracy: 0.8984375 - Loss: 0.28861334919929504
  Epoch 60/100 
    Accuracy: 0.9064670205116272 - Loss: 0.2702443301677704
  Epoch 61/100 
    Accuracy: 0.9012587070465088 - Loss: 0.280288964509964
  Epoch 62/100 
    Accuracy: 0.9027777910232544 - Loss: 0.2671239376068115
  Epoch 63/100 
    Accuracy: 0.9021267294883728 - Loss: 0.2769562005996704
  Epoch 64/100 
    Accuracy: 0.9019097089767456 - Loss: 0.2748531103134155
  Epoch 65/100 
    Accuracy: 0.9021267294883728 - Loss: 0.27483728528022766
  Epoch 66/100 
    Accuracy: 0.9019097089767456 - Loss: 0.2758308947086334
  Epoch 67/100 
    Accuracy: 0.9053819179534912 - Loss: 0.26034748554229736
  Epoch 68/100 
    Accuracy: 0.9147135615348816 - Loss: 0.25204694271087646
  Epoch 69/100 
    Accuracy: 0.9095051884651184 - Loss: 0.2476922869682312
  Epoch 70/100 
    Accuracy: 0.90234375 - Loss: 0.26203134655952454
  Epoch 71/100 
    Accuracy: 0.912109375 - Loss: 0.2545202970504761
  Epoch 72/100 
    Accuracy: 0.912109375 - Loss: 0.24261538684368134
  Epoch 73/100 
    Accuracy: 0.9125434160232544 - Loss: 0.24000437557697296
  Epoch 74/100 
    Accuracy: 0.912109375 - Loss: 0.24737058579921722
  Epoch 75/100 
    Accuracy: 0.9223090410232544 - Loss: 0.2247176468372345
  Epoch 76/100 
    Accuracy: 0.9188368320465088 - Loss: 0.22756655514240265
  Epoch 77/100 
    Accuracy: 0.9181857705116272 - Loss: 0.23565565049648285
  Epoch 78/100 
    Accuracy: 0.908203125 - Loss: 0.2456911951303482
  Epoch 79/100 
    Accuracy: 0.9227430820465088 - Loss: 0.22069236636161804
  Epoch 80/100 
    Accuracy: 0.916015625 - Loss: 0.2262197583913803
  Epoch 81/100 
    Accuracy: 0.9259982705116272 - Loss: 0.21022091805934906
  Epoch 82/100 
    Accuracy: 0.9164496660232544 - Loss: 0.23381249606609344
  Epoch 83/100 
    Accuracy: 0.9188368320465088 - Loss: 0.21435970067977905
  Epoch 84/100 
    Accuracy: 0.9201388955116272 - Loss: 0.22457586228847504
  Epoch 85/100 
    Accuracy: 0.9236111044883728 - Loss: 0.21246285736560822
  Epoch 86/100 
    Accuracy: 0.9344618320465088 - Loss: 0.19217202067375183
  Epoch 87/100 
    Accuracy: 0.9266493320465088 - Loss: 0.20815107226371765
  Epoch 88/100 
    Accuracy: 0.9286024570465088 - Loss: 0.19867929816246033
  Epoch 89/100 
    Accuracy: 0.9273003339767456 - Loss: 0.19958265125751495
  Epoch 90/100 
    Accuracy: 0.9288194179534912 - Loss: 0.20925898849964142
  Epoch 91/100 
    Accuracy: 0.9281684160232544 - Loss: 0.20068345963954926
  Epoch 92/100 
    Accuracy: 0.9325087070465088 - Loss: 0.18965286016464233
  Epoch 93/100 
    Accuracy: 0.931640625 - Loss: 0.19581907987594604
  Epoch 94/100 
    Accuracy: 0.931640625 - Loss: 0.19850033521652222
  Epoch 95/100 
    Accuracy: 0.9303385615348816 - Loss: 0.19677171111106873
  Epoch 96/100 
    Accuracy: 0.9283854365348816 - Loss: 0.19703605771064758
  Epoch 97/100 
    Accuracy: 0.9264323115348816 - Loss: 0.21304568648338318
  Epoch 98/100 
    Accuracy: 0.9290364384651184 - Loss: 0.20761099457740784
  Epoch 99/100 
    Accuracy: 0.9268662929534912 - Loss: 0.20005935430526733
  Epoch 100/100 
    Accuracy: 0.9322916865348816 - Loss: 0.1886705756187439
Test loss: 0.3957310914993286
Test accuracy: 0.8763889074325562


XGBoost Model Summary
======================================================
Model Parameters:
objective: multi:softmax
num_class: 8
booster: gbtree
eta: 0.2
max_depth: 7
eval_metric: merror

Number of boosting rounds (epochs): 150

Feature Importance (by weight):
f0: 728.0
f1: 670.0
f2: 935.0
f3: 770.0
f4: 905.0
f5: 808.0
f6: 665.0
f7: 878.0
f8: 268.0
f9: 209.0
f10: 228.0
f11: 241.0
f12: 176.0
f13: 211.0
f14: 255.0
f15: 281.0

Test accuracy with XGBoost: 0.9076388888888889


PREDICTION FOR THE AUDIO: THE_LION_KING.WAV 
Total Duration 50.00 seconds
======================================================
Time-Stamp start: 0.00/50.00 seconds
Time-Stamp end: 2.50/50.00 seconds
The emotion predicted: calm

Time-Stamp start: 2.50/50.00 seconds
Time-Stamp end: 5.00/50.00 seconds
The emotion predicted: sad

Time-Stamp start: 5.00/50.00 seconds
Time-Stamp end: 7.50/50.00 seconds
The emotion predicted: happy

Time-Stamp start: 7.50/50.00 seconds
Time-Stamp end: 10.00/50.00 seconds
The emotion predicted: happy

Time-Stamp start: 10.00/50.00 seconds
Time-Stamp end: 12.50/50.00 seconds
The emotion predicted: calm

Time-Stamp start: 12.50/50.00 seconds
Time-Stamp end: 15.00/50.00 seconds
The emotion predicted: fearful

Time-Stamp start: 15.00/50.00 seconds
Time-Stamp end: 17.50/50.00 seconds
The emotion predicted: sad

Time-Stamp start: 17.50/50.00 seconds
Time-Stamp end: 20.00/50.00 seconds
The emotion predicted: calm

Time-Stamp start: 20.00/50.00 seconds
Time-Stamp end: 22.50/50.00 seconds
The emotion predicted: angry

Time-Stamp start: 22.50/50.00 seconds
Time-Stamp end: 25.00/50.00 seconds
The emotion predicted: calm

Time-Stamp start: 25.00/50.00 seconds
Time-Stamp end: 27.50/50.00 seconds
The emotion predicted: fearful

Time-Stamp start: 27.50/50.00 seconds
Time-Stamp end: 30.00/50.00 seconds
The emotion predicted: surprise

Time-Stamp start: 30.00/50.00 seconds
Time-Stamp end: 32.50/50.00 seconds
The emotion predicted: angry

Time-Stamp start: 32.50/50.00 seconds
Time-Stamp end: 35.00/50.00 seconds
The emotion predicted: angry

Time-Stamp start: 35.00/50.00 seconds
Time-Stamp end: 37.50/50.00 seconds
The emotion predicted: disgust

Time-Stamp start: 37.50/50.00 seconds
Time-Stamp end: 40.00/50.00 seconds
The emotion predicted: disgust

Time-Stamp start: 40.00/50.00 seconds
Time-Stamp end: 42.50/50.00 seconds
The emotion predicted: fearful

Time-Stamp start: 42.50/50.00 seconds
Time-Stamp end: 45.00/50.00 seconds
The emotion predicted: fearful

Time-Stamp start: 45.00/50.00 seconds
Time-Stamp end: 47.50/50.00 seconds
The emotion predicted: neutral

Time-Stamp start: 47.50/50.00 seconds
Time-Stamp end: 50.00/50.00 seconds
The emotion predicted: angry

