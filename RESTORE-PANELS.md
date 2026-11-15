# Restore panel backgrounds in lowHD / lowHD 패널 배경 복원

[English](#english) · [한국어](#한국어) · [File reference / 파일 목록](#file-reference)

## English

Choose the panels you want to restore. **Background art** makes a panel easier to read. A **click catcher** stops clicks in the covered area from reaching the game world. You can restore either independently.

1. Close D2R. Keep a backup of the layout files and sprites you plan to change outside the mod directory. Use a clean D2R extraction from the **same game patch** as the reference for the original files.
2. For a normal mod install, work under `Diablo II Resurrected\mods\<mod>\<mod>.mpq\data`. If you applied QoL to extracted data and run with `-direct`, work under `Diablo II Resurrected\Data` and use a separate clean extraction as your reference.
3. In `global/ui/layouts`, open the affected JSON in a text editor and compare it with the clean original. Copy only the listed widget or field. Restore a commented-out widget or replace its inactive placeholder if one is already present. Put each widget in the same parent's `children` array and in the same order relative to neighboring widgets as the original. Preserve commas, escaped backslashes, and the mod's custom widgets. Replacing a whole layout can remove badges, lobby shortcuts, and the in-game Create and Quick Join panels.
4. In `hd/global/ui`, find the exact sprite paths listed for that panel. For each stem, check both `.sprite` and `.lowend.sprite`. In an ordinary `-mod` install, move any matching **0-byte** file out of the mod so the game can load the original asset. If you're using `-direct` or layering extracted data into the mod, replace the empty file with the matching nonempty sprite from your clean extraction. Skip absent and nonempty files. If removing an empty override still leaves the art missing, copy in the matching clean sprite.
5. Relaunch D2R and test the panel on its own. Check its buttons, blank areas, and Escape. If you use Multigate, also check that the relevant badges remain visible and that the corresponding make/join or support workflow still works. If a change causes trouble, restore that panel's backed-up files. Keep a copy of successful edits outside the mod folder because updates can overwrite them.

**Example:** For a visible waypoint panel, start with the two waypoint sprite stems in the table. If clicks through the panel also bother you, restore `ClickCatcher` in `waypointspaneloriginalhd.json` if it is missing.

## 한국어

원하는 패널만 골라 복원할 수 있습니다. **배경 이미지**를 복원하면 패널 내용을 읽기 쉬워집니다. **클릭 차단 위젯(ClickCatcher)** 을 복원하면 패널 빈 곳을 눌렀을 때 클릭이 뒤쪽 게임 화면으로 전달되는 것을 막을 수 있습니다. 두 설정은 각각 적용할 수 있습니다.

1. 디아블로 II: 레저렉션을 종료하세요. 수정할 레이아웃 파일과 스프라이트를 모드 폴더 밖에 백업하세요. 비교에 사용할 원본은 **현재 게임과 같은 패치 버전**에서 깨끗하게 추출한 데이터여야 합니다.
2. 일반 모드 설치라면 `Diablo II Resurrected\mods\<모드 이름>\<모드 이름>.mpq\data`에서 작업하세요. 추출 데이터에 QoL을 덮어씌우고 `-direct`로 실행한다면 `Diablo II Resurrected\Data`에서 작업하고, 비교용 원본은 별도의 폴더에 보관하세요.
3. `global/ui/layouts`에서 수정할 JSON 파일을 텍스트 편집기로 열고 원본과 비교하세요. 아래 표에 나온 위젯 블록이나 필드만 복원하세요. 기존 블록이 주석 처리되어 있다면 주석을 해제하고, 비활성 위젯이 대신 들어 있다면 원본 블록으로 바꾸세요. 원본과 같은 상위 위젯의 `children` 배열에 넣고 주변 위젯과의 순서도 맞추세요. 쉼표, 역슬래시 이스케이프, 모드의 사용자 지정 위젯을 그대로 유지하세요. JSON 전체를 원본으로 덮어쓰면 배지, 대기실 단축키, 게임 내 방 만들기 및 빠른 참가 패널이 사라질 수 있습니다.
4. `hd/global/ui`에서 아래 표에 나온 경로만 확인하세요. 각 항목의 `.sprite`와 `.lowend.sprite`를 모두 확인합니다. 일반적인 `-mod` 설치에서는 일치하는 **0바이트 파일**을 모드 폴더 밖으로 옮기면 게임이 원본을 불러올 수 있습니다. `-direct`로 실행하거나 모드에 추출 데이터를 합쳐 사용하는 경우, 빈 파일을 같은 경로의 정상 원본 스프라이트로 교체하세요. 파일이 없거나 크기가 0바이트가 아니면 건너뛰세요. 빈 파일을 옮긴 뒤에도 배경이 나오지 않으면 해당 경로에 정상 원본을 복사하세요.
5. 게임을 다시 실행한 뒤 해당 패널의 버튼, 빈 영역 클릭, Esc 키를 확인하세요. Multigate를 사용한다면 해당 배지가 보이는지와 방 만들기·참가 또는 지원 기능이 정상 동작하는지도 확인하세요. 문제가 생기면 해당 패널의 백업 파일을 복원하세요. 모드 업데이트로 수정 내용이 덮어써질 수 있으므로 적용한 파일은 모드 폴더 밖에 따로 보관하세요.

**예:** 순간이동진(웨이포인트) 배경을 보이게 하려면 아래 표의 배경 스프라이트 두 항목부터 복원하세요. 클릭이 패널 뒤로 전달되는 것도 막고 싶다면 `waypointspaneloriginalhd.json`에 `ClickCatcher`가 빠져 있는지 확인한 뒤 복원하세요.

## File reference

### Layouts / 레이아웃

Relative to `data/global/ui/layouts/`. Skip layouts absent from your mod and widgets already present and enabled. Arrows indicate nested widgets.

`data/global/ui/layouts/` 기준입니다. 사용 중인 모드에 없는 레이아웃과 이미 활성화된 위젯은 건너뛰세요. 화살표는 상위 위젯과 하위 위젯의 관계를 나타냅니다.

| Panel / 패널 | JSON file | Original widget or field / 복원할 원본 위젯 또는 필드 |
| --- | --- | --- |
| Character sheet / 캐릭터 창 | `characterstatspanelhd.json` | `Background` image and optional unnamed / 배경 및 선택 사항인 이름 없는 `ClickCatcherWidget` (`$PanelClickCatcherRect`) |
| Mercenary / 용병 창 | `hirelinginventorypanelhd.json` | Unnamed / 이름 없는 `ClickCatcherWidget` (`$PanelClickCatcherRect`) |
| Horadric Cube / 호라드림의 함 | `horadriccubelayouthd.json` | `click_catcher` |
| Expansion inventory / 확장판 소지품 | `playerinventoryexpansionlayouthd.json` | `click_catcher` |
| Expansion quest log / 확장판 퀘스트 창 | `questlogpanelexpansionhd.json` | `ClickCatcher` |
| Waypoint / 순간이동진 | `waypointspaneloriginalhd.json` | `ClickCatcher` |
| Shared side-panel regions / 공용 좌우 패널 영역 | `panelborderspanelhd.json` | `LeftAnchor → LeftClickCatcher`, `RightAnchor → RightClickCatcher` |
| Party / 파티 창 | `partypanelhd.json` | `click_catcher` |
| Help / Quick Join · 도움말 / 빠른 참가 | `helppanelhd.json` | `TransparentBG → catcher` (blocks clicks across the screen / 화면 전체의 클릭 통과 차단) |
| Lobby backing / 대기실 배경 | `lobbybackgroundpanelhd.json` | `FullLobbyBackground`, `BottomPanelBackgroundSmall`, `LeftPanel → BottomLeftPanelBackground`, `RightPanel → RightPanelBackground` and `BottomRightPanelBackground`, `CenterPanel → BottomPanelBackground` and `CenterPanelBackground` |
| Main-menu sidebar / 메인 메뉴 왼쪽 배경 | `mainmenubuttonribbonhd.json` | `Ribbon.fields.filename` → `FrontEnd/HD/Final/FrontEnd_LeftPanel` |
| Bottom HUD / 하단 HUD | `hudpanelhd.json` | For opacity, remove the mod-added `transparency` and `backgroundTransparency` keys from `Overlay.fields` when present. Restore `BGClickCatcher` only if you also want to block clicks. / 불투명한 배경을 원하면 `Overlay.fields`에 추가된 두 투명도 항목을 삭제하세요. 클릭 통과도 막으려면 `BGClickCatcher`를 복원하세요. |

The shared side-panel catchers affect more than one panel. Start with the individual panel's catcher when available. Test the rectangular player-count badges separately if you restore the HUD background, especially when using parking. If the restored background covers the badges, revert the HUD change.

공용 좌우 패널 클릭 차단 위젯은 여러 패널에 영향을 줍니다. 개별 패널에 해당하는 위젯이 있다면 먼저 그 위젯부터 복원하세요. 하단 HUD 배경을 복원한 경우, 특히 주차 기능을 사용한다면 직사각형 플레이어 수 배지가 보이는지 확인하세요. 배경이 배지를 가리면 HUD 변경을 되돌리세요.

### Background sprites / 배경 스프라이트

Relative to `data/hd/global/ui/`. Add `.sprite` and `.lowend.sprite` to each stem. The extra lowHDmin rows identify additional blanked artwork in that variant.

`data/hd/global/ui/` 기준입니다. 각 경로 뒤에 `.sprite`와 `.lowend.sprite`를 붙여 확인하세요. lowHDmin 전용 항목은 그 모드에서 추가로 비워 둔 이미지입니다.

| Panel / 패널 | Sprite stems / 스프라이트 경로 |
| --- | --- |
| Character sheet / 캐릭터 창 | `panel/character_sheet/character_background` |
| Advanced stats / 상세 능력치 | `panel/advancedcharactersheet/advancedcharactersheet_bg` |
| Skill tree base / 기술 트리 기본 배경 | `panel/panel_bg` |
| Quest log / 퀘스트 창 | `panel/quest_log/questlog_bg`, `panel/quest_log/qlpanelcover` |
| Party / 파티 창 | `panel/party/party_bg`, `panel/party/gameinformationbackground_bnet` |
| Waypoint / 순간이동진 | `panel/waypoints/waypoints_base`, `panel/waypoints/waypoints_overlay` |
| Lobby Create panel / 대기실 방 만들기 배경 | `lobby/creategame/creategamebg` |
| Main-menu sidebar / 메인 메뉴 왼쪽 배경 | `frontend/hd/final/frontend_leftpanel` |
| Options / 설정 | `panel/options/frontendoptionsbg` |
| Bottom HUD (where blanked) / 하단 HUD (파일이 비어 있을 때) | `panel/hud_02/front_panel` |
| lowHDmin · Skill tree / 기술 트리 | `spells/skill_trees/panel_skilltreebg` |
| lowHDmin · Inventory / 소지품 | `panel/inventory/background`, `panel/inventory/classic_background` |
| lowHDmin · Stash / 보관함 | `panel/stash/stashpanel_bg`, `panel/stash/stashpanel_bg_personal`, `panel/stash/stashpanel_bg_shared`, `panel/stash/classic_stash_panel` |
| lowHDmin · Horadric Cube and mercenary / 호라드림의 함 및 용병 | `panel/horadric_cube/horadriccube_bg`, `panel/hireling/hirelingpanel` |
| lowHDmin · Trade and vendors / 거래 및 상점 | `panel/trade/multiplayertrade_bg`, `panel/vendors/vendorshop_bg`, `panel/vendors/vendorforge_bg` |
