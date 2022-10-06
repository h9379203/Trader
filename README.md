# Trader
주식투자 시스템

## agent.py
 - 에이전트 클래스(Agent)  
 - 주식을 매수하거나 매도하는 추자자 역할  
 - 초기 자본금, 현금 잔고, 주식 잔고라는 상태  
 - 현금 잔고와 주식 잔고의 평가액을 합하면 포트폴리오 가치(PV, Portfolio Value)  
    PV = 주식 잔고 X 현재 주가 + 현금 잔고 (PV > 초기 자본금 ? 수익 : 손실)

## environment.py
 - 환경 클래스(Environment)
 - 에이전트가 투자할 종목의 차트 데이터를 관리

## policy_network.py
 - 정책 신경망 클래스(PolicyNetwork)
 - 특정 시점의 주식 데이터가 제공되었을 때 매수할지 또는 매도할지를 결정하는 에이전트의 뇌와 같은 역할
 - LSTM 신경망으로 구성
 - 매수와 매도 행위에 대해서 PV를 높일 수 있을지의 확률을 계산

## visualizer.py
 - 가시화기 모듈
 - 주식 데이터 학습 과정을 직관적으로 하악하기 위해 환경, 에이전트 상태, 정책 신경망 출력 등을 그림 파일로 시각화

## policy_learner.py
 - 정책 학습기 클래스(PolicyLearner)
 - 에이전트, 환경, 정책 신경망을 가지고 강화학습을 수행하는 몸체

