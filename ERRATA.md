### 정오표
> 잘못된 내용이 없도록 원고의 내용을 수차례 검토했으나, 미처 남아있는 오류로 학습에 불편함을 드려 죄송합니다.
<hr>

#### (200p, 201p) 앙상블 모델 학습 시 학습 데이터 입력 오류
- 앙상블 모델 학습을 위해 fit 메서드 사용 시 X_train, y_train 데이터를 이용해야 하는데, 실수로 전체 데이터인 X, y를 사용했습니다.
- 따라서 ensemble.fit(X, y) 부분을 ensemble.fit(X_train, y_train)으로 바꿔서 실습을 진행해주세요.

#### (303p) 예시 코드에 닫는 소괄호 누락
- 다음 코드의 맨 우측 부분에, 닫는 소괄호가 누락되었습니다.
> conv = nn.Conv2d(1, 64, kernel_size=(3, 3), stride=1, padding=1)

#### (286p) 풀링층 설명 보충
- 풀링층을 사용하면 학습되는 가중치가 줄어든다고 설명했는데, 구체적으로는 특성 맵의 크기가 작아져서 전결합층 부분에서 가중치의 수가 줄게 됩니다.

#### (284p, 292p) 3번째 은닉층 부분에 렐루 함수 누락
- 3번째 은닉층인 전결합층 부분에서 렐루 함수를 사용해야합니다. 즉, self.hidden_layer3 변수를 다음과 같이 변경해 주세요.
> self.hidden_layer3 = nn.Sequential(nn.Linear(128*5*5, 128), nn.ReLU())
