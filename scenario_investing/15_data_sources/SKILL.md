---
name: 실시간 데이터 모니터링 소스
description: 시나리오 투자에 필요한 핵심 지표의 실시간 데이터 소스와 확인 주기. FRED, TradingView, OECD 등.
---

# 실시간 데이터 모니터링 소스

시나리오 투자의 전조현상과 국면 판단에 필요한 **핵심 지표별 데이터 소스**.

## 1순위 지표 (매주 확인)

| 지표 | 소스 | URL | 확인 주기 |
|------|------|-----|---------|
| **ISM 제조업 지수** | ISM / FRED | https://fred.stlouisfed.org/series/MANEMP | 매월 1일 |
| **장단기 금리차 (10Y-2Y)** | FRED | https://fred.stlouisfed.org/series/T10Y2Y | 매일 |
| **미국 달러 지수 (DXY)** | TradingView | `TVC:DXY` | 매일 |
| **원달러 환율 (USDKRW)** | TradingView | `FX:USDKRW` | 매일 |
| **VIX (공포 지수)** | TradingView | `CBOE:VIX` | 매일 |
| **S&P500** | TradingView | `SP:SPX` | 매일 |
| **코스피** | TradingView / 네이버금융 | `KRX:KOSPI` | 매일 |

## 2순위 지표 (격주 확인)

| 지표 | 소스 | URL | 확인 주기 |
|------|------|-----|---------|
| **신용 스프레드 (회사채-국채)** | FRED | https://fred.stlouisfed.org/series/BAA10Y | 매주 |
| **한미 금리차** | FRED (US10Y) + 한국은행 (KR10Y) | 비교 계산 | 매주 |
| **OECD 선행지수** | OECD | https://data.oecd.org/leadind/composite-leading-indicator-cli.htm | 매월 |
| **M2 유동성** | FRED | https://fred.stlouisfed.org/series/M2SL | 매월 |
| **미국 기준금리 (Fed Funds)** | FRED | https://fred.stlouisfed.org/series/FEDFUNDS | FOMC 후 |
| **한국 수출** | 산업통상자원부 | https://www.motie.go.kr | 매월 1일 |
| **SOX 반도체 지수** | TradingView | `NASDAQ:SOX` | 매주 |

## 3순위 지표 (월간 확인)

| 지표 | 소스 | URL |
|------|------|-----|
| **GDP 성장률** | FRED | https://fred.stlouisfed.org/series/GDP |
| **산업 생산 지수** | FRED | https://fred.stlouisfed.org/series/INDPRO |
| **미국 CPI** | FRED | https://fred.stlouisfed.org/series/CPIAUCSL |
| **TED 스프레드** | FRED | https://fred.stlouisfed.org/series/TEDRATE |
| **CNN Fear & Greed** | CNN | https://edition.cnn.com/markets/fear-and-greed |
| **신용융자 잔고** | 금융투자협회 | https://freesis.kofia.or.kr |

## 전조현상 TOP 9 ↔ 데이터 매핑

| TOP 9 | 모니터링 지표 | 위험 신호 |
|-------|-----------|---------|
| #1 원화 약세 | USDKRW | 급등 추세 전환 |
| #2 금리 상승 3년차 | Fed Funds Rate | 인상 시작 후 3년 경과 |
| #3 신용 금리차 역전 | BAA10Y (FRED) | 급등 |
| #4 자산 동시 상승 | SPX + 유가 + 금 + 채권 | 4개 동시 상승 |
| #5 제오지산수 3년차 | ISM + 산업생산 + OECD CLI + GDP + 한국수출 | 천장 도달 |
| #6 신용융자 급증 | 금융투자협회 | 급증 |
| #7 유동성 감소 | M2SL (FRED) | 증가율 둔화 |
| #8 상승각도 + 거래량 | SPX/KOSPI 차트 | 급등 후 거래량 폭증 |
| #9 공포 지표 급등 | VIX + TED + CNN F&G | VIX 30+, TED 급등 |

## TradingView 워치리스트 추천 구성
```
DXY, USDKRW, US10Y, US02Y, SPX, IXIC, SOX, KOSPI,
VIX, GC1!(금), CL1!(유가), BTC/USD
```
