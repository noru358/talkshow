# TALKSHOW PROJECT BIBLE

## 한 줄 정의

한국 인터넷 커뮤니티의 실제 인간 반응과 말투를 원재료로 삼아, 반복되는 3명의 캐릭터가 떠드는 짧은 저복잡도 2D 토크쇼.

## 편집 원칙

1. 커뮤니티 글을 읽어주는 채널이 아니다. 본문은 떡밥, 댓글과 답글은 인간 반응 코퍼스다.
2. 본문·미디어·댓글·답글 관계를 원형으로 수집한다.
3. 좋은 인간 댓글은 입말화·축약·주어 명확화만 허용하고 매끈하게 고치지 않는다.
4. 해석 가능한 뜬금포, 정색, 침묵, 웃음은 GOLD가 될 수 있다.
5. 보통 3인이고 역할은 비트마다 바뀐다. 제3자는 말 없이 댓글창의 인간화를 담당할 수 있다.
6. 고정 정체성은 외형뿐 아니라 **목소리**를 포함한다. 공개본에 회차별 랜덤 음성을 쓰지 않는다.
7. QC는 제작 결함을 잡는다. 재미를 평균화하는 재작성기가 아니다.
8. 성과 데이터는 다음 GOLD/소재 선택을 교정하지만, 조회수만으로 원문을 자동 채택하거나 대사를 자동 개작하지 않는다.

## Writing engine

`SOURCE PACK → SOURCE GATE → GOLD EXTRACTION → CASTING → LIGHT ADAPTATION → BRIDGE only if essential`

### Source gate

다음 중 하나면 콘티 전에 보류/폐기한다.

- 댓글·답글 관계를 복원할 수 없다.
- 원문 설명 비용이 인간 GOLD보다 크다.
- 두 개 이상의 독립적으로 강한 인간 beat가 없다.
- 재미를 살리려면 AI 연결 대사가 30%를 넘는다.
- 반응이 일반적인 “ㅋㅋ/맞말”뿐이고 고유한 관점이나 사회적 변화가 없다.
- 공개 리스크를 가리면 비트의 존재 이유가 사라진다.

점수 평균으로 살리지 않는다. kill rule을 하나라도 넘으면 다른 소스를 본다.

### GOLD / adaptation

- GOLD마다 ID, 원문, URL/위치, reply parent, 용도를 기록한다.
- AI-written spoken beat는 전체의 30% 이하.
- source-derived setup도 AI-written으로 센다.
- AI-original comedic payoff는 원칙적으로 0%.
- 분모는 최종 공개본의 provenance-labeled spoken beats다.

## Identity / voice

- 캐릭터별 고정 visual identity와 fixed voice ID를 가진다.
- Seedance native speech는 입 모양·호흡·감정용 performance guide다.
- 최종 공개 음성은 speaker segment별 multilingual voice-to-voice 변환으로 고정한다.
- 분리 실패 구간만 같은 voice ID의 TTS로 보수한다.
- 발음 사전, 욕설 BLEEP, pitch/tempo 허용 범위를 캐릭터별로 유지한다.

## Format

- **최종 배포본:** 9:16
- **현 파일럿 생성 원본:** 잠긴 16:9 3인 master
- 세로본은 16:9 영상을 단순 축소 레터박스하지 않고, 편집 crop/punch-in과 hook/subtitle safe zone으로 재구성한다.
- 좋은 댓글 사슬 하나: 보통 15–22초 / 2 scenes
- 풍부한 원문: 22–35초
- 길이를 채우기 위한 설명·교훈·아웃트로 금지

## 제작과 학습

`Radar/Source → Thread/Gold → Episode Package → User Manual Production → Defect QC → Distribution/Performance Learning`

- 사용자는 TopView 생성, 선택, 최종 편집, 게시를 담당한다.
- ChatGPT는 상류 패키지, defect QC, 성과 해석을 담당한다.
- 성과 기록은 platform, publish time, version, hook, length, GOLD types, interaction device, views, retention, rewatch, shares, comments, follower conversion을 포함한다.
- 다음 회차에서는 한 번에 한 가설만 바꾼다.

## 장기 원칙

포맷 검증 후 캐릭터/배경/표정/입모양/포즈를 자산화하고 episode spec으로 조립한다. 파일럿 동안 자동 prompt rewrite, 자동 reference selection, 자동 TopView 실행은 중지한다.
