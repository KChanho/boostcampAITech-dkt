![스크린샷 2023-01-03 오후 10 54 23](https://user-images.githubusercontent.com/94108712/210370964-53302c66-868e-46e4-94c5-f0bf23c209b7.png)

<br /> 
<br /> 

# 9️⃣ Naver Boostcamp Ai Tech 4th RecSys level2 

<br /> 
<br /> 

## 👪 Members
| [<img src="https://avatars.githubusercontent.com/u/94108712?v=4" width="200px">](https://github.com/KChanho) | [<img src="https://avatars.githubusercontent.com/u/22442453?v=4" width="200px">](https://github.com/sungsubae) | [<img src="https://avatars.githubusercontent.com/u/28619804?v=4" width="200px">](https://github.com/JJI-Hoon) | [<img src="https://avatars.githubusercontent.com/u/71113430?v=4" width="200px">](https://github.com/sobin98) | [<img src="https://avatars.githubusercontent.com/u/75313644?v=4" width="200px">](https://github.com/dnjstka0307) |
| :--------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------:
|                          [김찬호](https://github.com/KChanho)                           |                            [배성수](https://github.com/sungsubae)                             |                        [이지훈](https://github.com/JJI-Hoon)                           |                          [정소빈](https://github.com/sobin98)                           |                            [조원삼](https://github.com/dnjstka0307)

<br /> 
<br /> 

## 📖 Deep Knowledge Tracing
초등학교, 중학교, 고등학교, 대학교와 같은 교육기관에서 우리는 시험을 늘 봐왔습니다. 시험 성적이 높은 과목은 우리가 잘 아는 것을 나타내고 시험 성적이 낮은 과목은 반대로 공부가 더욱 필요함을 나타냅니다. 시험은 우리가 얼마만큼 아는지 평가하는 한 방법입니다.

하지만 시험에는 한계가 있습니다. 우리가 수학 시험에서 점수를 80점 받았다면 우리는 80점을 받은 학생일 뿐입니다. 우리가 돈을 들여 과외를 받지 않는 이상 우리는 우리 개개인에 맞춤화된 피드백을 받기가 어렵고 따라서 무엇을 해야 성적을 올릴 수 있을지 판단하기 어렵습니다. 이럴 때 사용할 수 있는 것이 DKT입니다!

DKT는 Deep Knowledge Tracing의 약자로 우리의 "지식 상태"를 추적하는 딥러닝 방법론입니다.
![57a525f9-a799-49a5-84f6-3150c8fb6ccb](https://user-images.githubusercontent.com/75313644/206378748-2f2dda49-8e78-4849-ac34-53c38630c18f.png)

<br /> 

### 🏆️ Goal
**한 유저의 시계열적인 학습데이터를 통해 마지막 문제의 정답여부를 예측**

<br /> 

### 📄 Data
- `userID` 사용자의 고유번호. 총 7,442명의 고유 사용자가 있으며, train/test셋은 이 userID를 기준으로 90/10의 비율로 분류.

- `assessmentItemID` 문항의 고유번호. 총 9,454개의 고유 문항이 있으며, 번호 내에 카테고리, 시험지아이디등의 규칙 존재.

- `testId` 시험지의 고유번호. 시험지 내에 여러 문항이 존재합니다. 총 1,537개의 고유한 시험지가 존재.

- `answerCode` 문항을 맞췄는지 여부에 대한 정보. 0과 1은 각각 문제의 오답과 정답 여부. 타겟이 되는 마지막 문제는 -1로 지정.

- `Timestamp` 사용자가 해당문항을 풀기 시작한 시점의 데이터.

- `KnowledgeTag` 문항 당 하나씩 배정되는 태그로, 일종의 중분류 역할. 912개의 고유 태그가 존재.

<br /> 
<br /> 

## 💻 Repository Summary
![Repo-페이지-1 drawio](https://user-images.githubusercontent.com/75313644/206433453-d315cddd-5cdd-477b-958b-b086369f7042.png)

<br /> 
<br /> 

## 🗃 Project Process

<br /> 

### 🤖 Models
문제해결을 위한 모델 탐색이후, 개별 Data Processing이나 Wandb를 통한 Hyer parameter Tuning.
![image](https://user-images.githubusercontent.com/75313644/206642070-d38a37c3-40c9-442b-8603-d7e8d181d7ef.png)

<br /> 

### 📈 Ensemble
계열별로 Public기준의 최적모델을 확인, Prediction의 분포를 시각화해 확인 후, Weight 실험 후 앙상블 진행.
![image](https://user-images.githubusercontent.com/75313644/206643037-bee27388-6dde-474e-a7bb-958128b54724.png)

<br /> 
<br /> 

## 🏅 Result : Public 5th > Privite 3rd

|리더보드| auroc | accuracy | 순위 |
|:--------:|:------:|:------:|:----------:|
|public| 0.8287 | 0.7392 | **5위** |
|private| 0.8522 | 0.7876 | **최종 3위** |

stratified kfold를 통해 일반화 성능을 향상시켜 private에서 더 좋은 성과를 냄.

<br /> 

**상세한 프로젝트 내용은 레포트를 참고해주세요!**