# 스탠바이독 개인정보처리방침

**최종 수정일:** 2026년 10월 19일
**앱 패키지:** `com.hermes.standby`

> **요약**
> 스탠바이독 자체는 사용자의 정보를 수집하거나 서버로 보내지 않습니다.
> 설정 화면에 Google AdMob 광고가 표시되며, 광고를 위해 Google이 기기 식별자 등 일부 정보를 수집합니다(1·4·5항).
> 알림 내용, 사진, 센서 값은 광고 SDK에 전달되지 않고 기기 안에서만 처리됩니다.

---

## 1. 수집하는 개인정보

개발자는 개인정보를 수집하지 않습니다. 앱이 통신하는 개발자 서버가 없고, 회원 가입·로그인·계정이 없습니다. 분석 도구와 크래시 리포트 도구를 포함하지 않습니다.

다만 앱에 포함된 Google Mobile Ads SDK(AdMob)가 광고 게재, 분석, 부정 클릭 방지를 위해 아래 정보를 자동으로 수집해 Google에 전송합니다. 전송은 TLS로 암호화됩니다.

| 정보 | 내용 |
|---|---|
| IP 주소 | 기기의 대략적인 위치 추정에 쓰일 수 있음 |
| 앱 사용 기록 | 앱 실행, 탭, 광고 시청 |
| 진단 정보 | 앱 실행 시간, 응답 없음 비율, 전력 사용량 |
| 기기 식별자 | 안드로이드 광고 ID, 앱 세트 ID |

광고 ID는 안드로이드 설정의 광고 메뉴에서 재설정하거나 삭제할 수 있습니다. 자세한 내용은 [Google의 개인정보처리방침](https://policies.google.com/privacy)과 [Google이 파트너 사이트·앱의 정보를 사용하는 방식](https://policies.google.com/technologies/partner-sites)을 참고하세요.

"광고 제거" 구매는 Google Play 결제로 처리됩니다. 결제 정보는 Google이 처리하며 개발자는 받지 않습니다. 앱은 구매 여부만 기기 안에 저장합니다.

## 2. 기기 안에서만 처리되는 정보

앱 기능을 위해 아래 정보를 기기 내부에서 읽거나 저장합니다. 모두 사용자의 기기를 벗어나지 않습니다.

| 정보 | 사용 목적 | 저장 여부 |
|---|---|---|
| 사진 | 대기 화면의 사진 위젯과 폴라로이드 위젯에 표시 | 사진 파일 자체는 복사하지 않습니다. 안드로이드 사진 선택 도구로 사용자가 직접 고른 사진의 *참조 주소*와 자르기 위치만 앱 설정에 저장합니다. |
| 알림 내용 | 대기 화면에 현재 알림을 표시 | **저장하지 않습니다.** 앱이 실행 중인 동안 메모리에만 유지되며, 앱이 종료되거나 알림 접근 권한이 해제되면 즉시 사라집니다. 파일이나 데이터베이스에 기록하지 않습니다. |
| 재생 중인 음악 정보 | 대기 화면의 음악 위젯에 제목·아티스트·앨범 아트 표시 및 재생 제어 | 저장하지 않습니다. 메모리에만 유지됩니다. |
| 조도 센서 값 | 주변 밝기에 따라 화면 밝기와 야간 모드를 자동 조절 | 저장하지 않습니다. |
| 가속도 센서 값 | 기기를 움직였을 때 화면을 깨우는 기능 | 저장하지 않습니다. |
| 충전기 연결 상태 | 충전기를 꽂았을 때 대기 화면을 자동으로 켜는 기능 | 저장하지 않습니다. |
| 앱 설정값 | 시계 모양, 테마, 위젯 배치, 사진 전환 간격 등 사용자 선택 보존 | 기기 내부 앱 저장 공간에 저장합니다. 개인 식별 정보를 포함하지 않습니다. |
| 이용 기간 | 남은 무료 이용 기간, 광고 시청 횟수, 광고 제거 구매 여부 | 기기 내부 앱 저장 공간에 저장합니다. 외부로 보내지 않습니다. |

## 3. 알림 접근 권한에 관하여

스탠바이독은 안드로이드의 알림 접근 권한(`NotificationListenerService`)을 사용합니다. 이 권한은 민감하므로 아래 사항을 명확히 밝힙니다.

- 이 권한은 **선택 사항**입니다. 허용하지 않아도 시계, 사진 등 나머지 기능은 정상 작동합니다.
- 알림 내용은 대기 화면에 **표시하는 목적으로만** 사용합니다.
- 알림 내용을 **수집·저장·분석·전송하지 않습니다.**
- 기기가 잠겨 있을 때는 알림의 제목과 본문을 화면에 표시하지 않습니다. 다른 사람이 잠긴 기기를 보더라도 내용이 노출되지 않습니다.
- 사용자는 언제든 안드로이드 설정에서 이 권한을 해제할 수 있으며, 해제 즉시 앱이 보유한 알림 정보는 모두 삭제됩니다.

## 4. 제3자 제공 및 공유

개발자가 제3자에게 제공하는 정보는 없습니다. 1항의 광고 관련 정보는 Google Mobile Ads SDK가 Google에 직접 전송합니다.

## 5. 광고 및 분석

- 광고는 **설정 화면에만** 표시됩니다. 대기 화면과 잠금 화면에는 광고를 표시하지 않습니다.
- 설정 화면 하단에 배너 광고가 있고, 사용자가 직접 누를 때만 보상형 광고가 재생됩니다. 보상형 광고를 보면 무료 이용 기간이 늘어납니다.
- 유럽 경제 지역·영국 등 동의가 필요한 지역에서는 Google의 동의 화면(UMP)으로 광고 개인정보 선택을 받습니다. 설정 화면의 "광고 개인정보 설정"에서 언제든 바꿀 수 있습니다.
- "광고 제거"를 구매하면 광고가 더 이상 요청되지 않습니다.
- 사용 기록 분석 도구는 포함하지 않습니다.

## 6. 아동의 개인정보

스탠바이독은 13세 미만 아동을 대상으로 하지 않습니다. 개발자는 어떤 연령대의 사용자로부터도 개인정보를 수집하지 않습니다.

## 7. 정보의 삭제

앱이 저장하는 정보는 설정값, 사진 참조 주소, 이용 기간뿐이며 모두 기기 내부에 있습니다. 앱을 삭제하면 함께 삭제됩니다. 앱 내 설정에서 개별 항목을 직접 지울 수도 있습니다. 광고 ID는 안드로이드 설정에서 재설정하거나 삭제할 수 있습니다. 광고 제거 구매 기록은 Google Play 계정에 남아 앱을 다시 설치해도 복원됩니다.

## 8. 권한 목록과 사용 이유

| 권한 | 사용 이유 |
|---|---|
| 다른 앱 위에 표시<br>`SYSTEM_ALERT_WINDOW` | 화면이 꺼진 상태에서 충전기를 꽂았을 때 대기 화면을 띄우기 위해 필요합니다. |
| 포그라운드 서비스<br>`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE` | 화면이 꺼져 있어도 충전기 연결을 감지하기 위해 필요합니다. 이 기능은 기본값이 꺼짐이며, 사용자가 직접 켰을 때만 동작합니다. |
| 알림 표시<br>`POST_NOTIFICATIONS` | 충전 감지 기능이 동작 중임을 알리는 알림을 표시합니다. |
| 배터리 최적화 예외 요청<br>`REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | 제조사 전원 관리가 충전 감지 서비스를 멈추지 않도록, 사용자가 자동 실행 화면에서 배터리 제한 풀기를 누를 때만 예외를 요청합니다. 거절해도 나머지 기능은 동작합니다. |
| 부팅 완료 수신<br>`RECEIVE_BOOT_COMPLETED` | 기기를 재시작한 뒤에도 사용자가 켜둔 충전 감지 기능이 유지되도록 합니다. |
| 알림 접근<br>`BIND_NOTIFICATION_LISTENER_SERVICE` | 대기 화면에 알림과 재생 중인 음악을 표시합니다. 3항 참조. |
| 인터넷, 네트워크 상태<br>`INTERNET`, `ACCESS_NETWORK_STATE` | 설정 화면의 광고를 불러오고 Google Play 결제와 통신합니다. |
| 광고 ID<br>`AD_ID`, `ACCESS_ADSERVICES_*` | Google Mobile Ads SDK가 광고 게재와 측정에 사용합니다. 1·5항 참조. |
| 결제<br>`com.android.vending.BILLING` | "광고 제거" 구매를 Google Play 결제로 처리합니다. |

## 9. 방침 변경

이 방침이 변경되면 이 문서를 갱신하고 상단의 최종 수정일을 고칩니다. 수집 항목이 늘어나는 변경이 생길 경우 앱 업데이트 시 사용자에게 알립니다.

## 10. 문의

개인정보 관련 문의: bju.10147@gmail.com

---
---

# Standby Dock Privacy Policy

**Last updated:** October 19, 2026
**Package:** `com.hermes.standby`

> **Summary**
> Standby Dock itself collects no user data and sends nothing to any server of ours.
> The settings screen shows Google AdMob ads, and Google collects some data such as device identifiers to serve them (sections 1, 4 and 5).
> Notification content, photos and sensor readings are never passed to the ad SDK; they stay on the device.

---

## 1. Data We Collect

The developer collects no personal data. There is no developer server, no account and no sign-in. The app contains no analytics or crash reporting SDKs.

The Google Mobile Ads SDK (AdMob) included in the app automatically collects the following and sends it to Google for advertising, analytics and fraud prevention. It is encrypted in transit with TLS.

| Data | Detail |
|---|---|
| IP address | May be used to estimate the general location of the device |
| App interactions | App launches, taps, ad views |
| Diagnostics | App launch time, hang rate, energy usage |
| Device identifiers | Android advertising ID, app set ID |

The advertising ID can be reset or deleted in the ads menu of Android settings. See [Google's Privacy Policy](https://policies.google.com/privacy) and [How Google uses information from sites or apps that use its services](https://policies.google.com/technologies/partner-sites).

The "Remove ads" purchase is handled by Google Play Billing. Google processes the payment; the developer never receives payment details. The app stores only whether the purchase was made, on the device.

## 2. Data Processed On-Device Only

| Data | Purpose | Retention |
|---|---|---|
| Photos | Displayed in the photo and polaroid widgets | Photo files are never copied. Only the URI reference chosen by the user through the Android Photo Picker, plus crop coordinates, are stored in app settings. |
| Notification content | Shown on the standby screen | **Not stored.** Held in memory only while the app runs; cleared when the app stops or notification access is revoked. Never written to disk. |
| Media playback metadata | Title, artist, album art and transport controls in the music widget | Not stored. Memory only. |
| Ambient light sensor | Automatic brightness and night mode | Not stored. |
| Accelerometer | Motion-to-wake feature | Not stored. |
| Charger connection state | Launching the standby screen when a charger is plugged in | Not stored. |
| App settings | Preserving clock style, theme, widget layout and intervals | Stored in app-private storage on the device. Contains no personally identifying information. |
| Usage pass | Free time remaining, number of ads watched, whether ads were removed | Stored in app-private storage on the device. Never sent off the device. |

## 3. Notification Access

- Notification access is **optional**. All other features work without it.
- Notification content is used **solely for on-screen display**.
- It is **never collected, stored, analyzed, or transmitted**.
- While the device is locked, notification titles and bodies are withheld from the display.
- Revoking the permission in Android settings immediately clears all notification data held by the app.

## 4. Sharing With Third Parties

The developer shares nothing with third parties. The advertising data in section 1 is sent by the Google Mobile Ads SDK directly to Google.

## 5. Advertising and Analytics

- Ads appear **only on the settings screen**, never on the standby screen or the lock screen.
- A banner sits at the bottom of the settings screen. A rewarded ad plays only when the user taps for one, and adds free days.
- Where consent is required (such as the EEA and the UK), Google's consent form (UMP) collects the user's ad privacy choices, which can be changed at any time under "Ad privacy choices" in settings.
- After "Remove ads" is purchased, no more ads are requested.
- The app contains no analytics.

## 6. Children's Privacy

Standby Dock is not directed at children under 13. The developer collects no personal data from users of any age.

## 7. Data Deletion

All stored data is local app settings, photo URI references and the usage pass. Uninstalling the app removes it. Individual items can also be cleared from within the app's settings. The advertising ID can be reset or deleted in Android settings. The "Remove ads" purchase stays with the Google Play account and is restored after reinstalling.

## 8. Permissions

| Permission | Reason |
|---|---|
| `SYSTEM_ALERT_WINDOW` | Required to show the standby screen when a charger is connected while the screen is off. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE` | Required to detect charger connection while the screen is off. Off by default; only runs when the user enables it. |
| `POST_NOTIFICATIONS` | Shows the notification indicating the charge watcher is running. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Asks for an exemption only when the user taps the battery step on the auto-start screen, so the device's power management does not stop the charge watcher. Everything else works if the user declines. |
| `RECEIVE_BOOT_COMPLETED` | Keeps the user-enabled charge watcher running after a device restart. |
| `BIND_NOTIFICATION_LISTENER_SERVICE` | Displays notifications and current media on the standby screen. See section 3. |
| `INTERNET`, `ACCESS_NETWORK_STATE` | Loads the ads on the settings screen and talks to Google Play Billing. |
| `AD_ID`, `ACCESS_ADSERVICES_*` | Used by the Google Mobile Ads SDK to serve and measure ads. See sections 1 and 5. |
| `com.android.vending.BILLING` | Processes the "Remove ads" purchase through Google Play Billing. |

## 9. Changes

Changes are published by updating this document and its date. Any change that adds collected data will be announced in the app update.

## 10. Contact

bju.10147@gmail.com
