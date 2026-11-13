# toklink-promo

톡링크 앱 대화 화면 위 홍보 줄의 목록입니다. 앱이 `promo.json` 을 받아 6초마다 돌아가며 보여 줍니다.
**이 저장소는 공개입니다. 단가·계약 같은 내부 정보는 넣지 마세요.**

## promo.json 항목

| 칸 | 뜻 |
|---|---|
| id | 항목 이름표(영문·숫자, 64자 이내) |
| title | 굵게 보이는 이름(40자 이내) |
| cta | 이름 뒤에 붙는 안내(40자 이내, 비워도 됨) |
| url | 누르면 열리는 **https** 주소 |
| thumb | 왼쪽 작은 그림의 https 주소(없으면 기본 그림) |
| langs | 보일 앱 화면 언어: `ko` `en` `ja` `zh` |
| sponsored | `true` 면 `광고` 딱지가 붙음(광고주 항목) |
| start / end | 보이는 기간(`2026-12-01` 형식, 기기 날짜 기준, 둘 다 선택) |

- 항목은 20개까지. 틀린 항목은 그 항목만 건너뜁니다. 파일 전체가 틀리면 앱은 저장해 둔 마지막 정상 목록을 씁니다.
- `items` 를 `[]` 로 두면 홍보 줄이 사라집니다.
- 바꾼 뒤 앱에 반영되기까지 몇 분 걸릴 수 있습니다(깃허브 캐시).

## 광고주 항목 예

```json
{
  "id": "shop-2026-12",
  "title": "상품 이름",
  "cta": "보러 가기",
  "url": "https://shop.example.com/promo",
  "thumb": "https://raw.githubusercontent.com/sooeunkim7112-bit/toklink-promo/main/img/shop.jpg",
  "langs": ["ko"],
  "sponsored": true,
  "start": "2026-12-01",
  "end": "2026-12-31"
}
```
