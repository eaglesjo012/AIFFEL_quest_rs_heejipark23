# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 박희지
- 리뷰어 : 이민


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**

    <img width="991" height="154" alt="image" src="https://github.com/user-attachments/assets/bfe58b82-71a5-43c9-b139-b47749fbe44d" />

    세 루브릭(30분 내 베이스라인, SimpleBaseline 구현, 두 모델 비교)이 모두 실행 결과로 확인된다. 다만 3장에서 만든 ptrecord 파이프라인은 실제 학습에는 쓰이지 않고 "생성·검증 전용"으로만 남아있어 확인이 필요하다.

    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**

    <img width="1273" height="1281" alt="image" src="https://github.com/user-attachments/assets/aa34cd6e-a34d-4da8-8c11-bd0bfe649448" />

    가장 복잡한 재귀 구조인 HourglassModule이 docstring만으로 up/low branch 역할과 재귀 종료 조건, skip connection 위치까지 설명되어 있어 코드를 바로 이해할 수 있었다.

        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**

    <img width="1455" height="1280" alt="image" src="https://github.com/user-attachments/assets/c0344868-8527-41c6-99f7-febe0114de23" />

    에러 발생-해결 로그는 없지만, "SimpleBaseline이 loss는 낮은데 PCKh는 낮은 이유"를 직접 가설로 세우고 diagnose_heatmaps 함수를 새로 작성해 검증한 뒤 절반만 채택하는 정직한 결론을 냈다.

        
- [x]  **4. 회고를 잘 작성했나요?**
      <img width="1484" height="822" alt="image" src="https://github.com/user-attachments/assets/d589fa4e-fde8-43d2-b6c0-a2e3241113ab" />

    배운 점·아쉬운 점이 수치 근거와 함께 기록되어 있고, 원 논문과 반대로 나온 결과를 두고 성급히 결론짓지 않는 태도가 돋보였다.

        
- [x]  **5. 코드가 간결하고 효율적인가요?**

    <img width="1163" height="1305" alt="image" src="https://github.com/user-attachments/assets/42cbd7ec-294e-46cf-85af-8f8af8dccc1d" />

    train_model(model_fn, tag, ...)이 모델 생성 함수만 바꿔 끼우는 구조라, 학습 루프 코드를 한 번만 작성해 두 모델에 동일하게 재사용했다.


# 회고(참고 링크 및 코드 개선)
```
model_fn을 인자로 받는 train_model 패턴이 인상 깊어 다음 모델 비교 과제에도 적용해볼 만하다.
```

