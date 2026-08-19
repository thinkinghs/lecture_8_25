# KISTI 실무 교육 · 대용량 연구 데이터 전처리·분석 자동화



## 폴더 구성

```
C:\kisti-lab\
  pyproject.toml            필요한 패키지 목록
  uv.lock                   설치할 정확한 버전 기록 (직접 수정하지 않습니다)
  .python-version           이 과정이 사용하는 Python 버전 (3.14)
  README.md                 이 문서
  data\
    sensor_readings.csv     실습 데이터 (약 20만 행 / 14개 컬럼)
  outputs\                  분석 결과물이 저장되는 폴더
```

`uv sync` 를 실행하면 `.venv` 폴더가 새로 생깁니다. 숨김 폴더라 탐색기에 보이지 않아도 정상입니다.

## 실습 데이터

여러 관측 지점의 환경 센서 기록을 흉내 낸 **합성 데이터**입니다. 실제 관측값이 아닙니다.

실제 연구 데이터에서 흔히 나타나는 문제를 의도적으로 심어 두었습니다.
1교시에서는 이 문제들을 **찾아내는 것**까지 하고, 고치는 작업은 2교시에서 다룹니다.

| 컬럼 | 설명 |
| --- | --- |
| `record_id` | 레코드 일련번호 |
| `station_id` | 관측 지점 코드 (ST-01 ~ ST-12) |
| `station_name` | 관측 지점명 |
| `measured_at` | 측정 시각 |
| `temperature_c` | 기온 (°C) |
| `humidity_pct` | 상대습도 (%) |
| `pressure_hpa` | 기압 (hPa) |
| `wind_speed_ms` | 풍속 (m/s) |
| `wind_direction` | 풍향 |
| `pm10_ugm3` | 미세먼지 PM10 (µg/m³) |
| `pm25_ugm3` | 초미세먼지 PM2.5 (µg/m³) |
| `rainfall_mm` | 강수량 (mm) |
| `battery_pct` | 장비 배터리 잔량 (%) |
| `status` | 장비 상태 |

파일 인코딩은 UTF-8입니다. Excel에서 바로 열면 한글이 깨져 보일 수 있으나 정상이며,
Claude Code로 읽을 때는 문제가 없습니다.

## 문제가 생기면

| 증상 | 대처 |
| --- | --- |
| `uv` 를 찾을 수 없음 | 터미널을 껐다 켠 뒤 다시 시도 |
| `uv sync` 가 중간에 멈춤 | 같은 명령을 다시 실행 (받은 부분은 건너뜁니다) |
| 폴더가 `C:\kisti-lab\kisti-lab` 로 이중 | 안쪽 폴더를 `C:\` 로 옮기고 빈 바깥 폴더 삭제 |
