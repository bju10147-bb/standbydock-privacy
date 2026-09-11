# 스탠바이독 개인정보처리방침

**최종 수정일:** 2026년 9월 11일
**앱 패키지:** `com.hermes.standby`

> **요약**
> 스탠바이독은 사용자의 어떤 정보도 수집하지 않고, 어떤 정보도 기기 밖으로 전송하지 않습니다.
> 이 앱에는 인터넷 접속 권한 자체가 없어, 기술적으로 외부 전송이 불가능합니다.

---

## 1. 수집하는 개인정보

**없습니다.**

스탠바이독은 개인정보를 수집하거나 서버로 전송하지 않습니다. 회원 가입, 로그인, 계정이 없습니다. 분석 도구, 광고 SDK, 크래시 리포트 도구를 포함하지 않습니다.

앱의 안드로이드 매니페스트에 `android.permission.INTERNET` 권한이 선언되어 있지 않습니다. 운영체제가 이 앱의 네트워크 통신을 차단하므로, 설령 의도하지 않은 코드가 있더라도 정보가 외부로 나갈 수 없습니다.

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

## 3. 알림 접근 권한에 관하여

스탠바이독은 안드로이드의 알림 접근 권한(`NotificationListenerService`)을 사용합니다. 이 권한은 민감하므로 아래 사항을 명확히 밝힙니다.

- 이 권한은 **선택 사항**입니다. 허용하지 않아도 시계, 사진 등 나머지 기능은 정상 작동합니다.
- 알림 내용은 대기 화면에 **표시하는 목적으로만** 사용합니다.
- 알림 내용을 **수집·저장·분석·전송하지 않습니다.**
- 기기가 잠겨 있을 때는 알림의 제목과 본문을 화면에 표시하지 않습니다. 다른 사람이 잠긴 기기를 보더라도 내용이 노출되지 않습니다.
- 사용자는 언제든 안드로이드 설정에서 이 권한을 해제할 수 있으며, 해제 즉시 앱이 보유한 알림 정보는 모두 삭제됩니다.

## 4. 제3자 제공 및 공유

제공하거나 공유하는 정보가 없습니다. 앱이 통신하는 서버가 존재하지 않습니다.

## 5. 광고 및 분석

광고를 게재하지 않으며, 사용 기록 분석 도구를 포함하지 않습니다.

## 6. 아동의 개인정보

스탠바이독은 어떤 연령대의 사용자로부터도 개인정보를 수집하지 않으므로, 아동의 개인정보 또한 수집하지 않습니다.

## 7. 정보의 삭제

앱이 저장하는 정보는 설정값과 사진 참조 주소뿐이며 모두 기기 내부에 있습니다. 앱을 삭제하면 함께 삭제됩니다. 앱 내 설정에서 개별 항목을 직접 지울 수도 있습니다.

## 8. 권한 목록과 사용 이유

| 권한 | 사용 이유 |
|---|---|
| 다른 앱 위에 표시<br>`SYSTEM_ALERT_WINDOW` | 화면이 꺼진 상태에서 충전기를 꽂았을 때 대기 화면을 띄우기 위해 필요합니다. |
| 포그라운드 서비스<br>`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE` | 화면이 꺼져 있어도 충전기 연결을 감지하기 위해 필요합니다. 이 기능은 기본값이 꺼짐이며, 사용자가 직접 켰을 때만 동작합니다. |
| 알림 표시<br>`POST_NOTIFICATIONS` | 충전 감지 기능이 동작 중임을 알리는 알림을 표시합니다. |
| 전체 화면 알림<br>`USE_FULL_SCREEN_INTENT` | Android 13 이하 기기에서, 위 오버레이 권한이 없을 때의 대체 경로로만 사용합니다. Android 14 이상에서는 요청하지 않습니다. |
| 부팅 완료 수신<br>`RECEIVE_BOOT_COMPLETED` | 기기를 재시작한 뒤에도 사용자가 켜둔 충전 감지 기능이 유지되도록 합니다. |
| 알림 접근<br>`BIND_NOTIFICATION_LISTENER_SERVICE` | 대기 화면에 알림과 재생 중인 음악을 표시합니다. 3항 참조. |

## 9. 방침 변경

이 방침이 변경되면 이 문서를 갱신하고 상단의 최종 수정일을 고칩니다. 수집 항목이 늘어나는 변경이 생길 경우 앱 업데이트 시 사용자에게 알립니다.

## 10. 문의

개인정보 관련 문의: bju.10147@gmail.com

---
---

# StandByDock Privacy Policy

**Last updated:** September 11, 2026
**Package:** `com.hermes.standby`

> **Summary**
> StandByDock collects no user data and transmits nothing off the device.
> The app does not declare the internet permission, so network transmission is technically impossible.

---

## 1. Data We Collect

**None.**

StandByDock does not collect or transmit personal data. There are no accounts, no sign-in, no analytics SDKs, no advertising SDKs, and no crash reporting SDKs.

The app manifest does not declare `android.permission.INTERNET`. The operating system blocks all network access for this app.

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

## 3. Notification Access

- Notification access is **optional**. All other features work without it.
- Notification content is used **solely for on-screen display**.
- It is **never collected, stored, analyzed, or transmitted**.
- While the device is locked, notification titles and bodies are withheld from the display.
- Revoking the permission in Android settings immediately clears all notification data held by the app.

## 4. Sharing With Third Parties

Nothing is shared. The app communicates with no server.

## 5. Advertising and Analytics

The app serves no ads and contains no analytics.

## 6. Children's Privacy

The app collects no personal data from users of any age, including children.

## 7. Data Deletion

All stored data is local app settings and photo URI references. Uninstalling the app removes it. Individual items can also be cleared from within the app's settings.

## 8. Permissions

| Permission | Reason |
|---|---|
| `SYSTEM_ALERT_WINDOW` | Required to show the standby screen when a charger is connected while the screen is off. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SPECIAL_USE` | Required to detect charger connection while the screen is off. Off by default; only runs when the user enables it. |
| `POST_NOTIFICATIONS` | Shows the notification indicating the charge watcher is running. |
| `USE_FULL_SCREEN_INTENT` | Used only on Android 13 and below, as a fallback when the overlay permission is absent. Not requested on Android 14 or higher. |
| `RECEIVE_BOOT_COMPLETED` | Keeps the user-enabled charge watcher running after a device restart. |
| `BIND_NOTIFICATION_LISTENER_SERVICE` | Displays notifications and current media on the standby screen. See section 3. |

## 9. Changes

Changes are published by updating this document and its date. Any change that adds collected data will be announced in the app update.

## 10. Contact

bju.10147@gmail.com
