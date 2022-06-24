# 🌏 만국박람회
> 기간: 2022-06-13 ~ 2022-06-24
> 
> 팀원: [Finnn](https://github.com/finnn1), [Kiwi](https://github.com/kiwi1023)
> 
> 리뷰어: [Charlie](https://github.com/kcharliek)

# 목차
* [프로젝트 소개](#프로젝트-소개)
    * [개발환경 및 라이브러리](#개발환경-및-라이브러리)
* [구현내용](#구현내용)
* [키워드](#키워드)
* [핵심경험](#핵심경험)
* [기능설명](#기능설명)
    * [STEP 1](https://github.com/finnn1/ios-exposition-universelle/blob/STEP1/Docs/STEP01.md)

# 프로젝트 소개
만국박람회(World's Fair)를 iOS 어플리케이션으로 구현해보는 프로젝트입니다.
다양한 작품들과 해당 작품에 대한 상세한 설명을 볼 수 있습니다.

### 개발환경 및 라이브러리
[![swift](https://img.shields.io/badge/swift-5.6-orange)]()
[![xcode](https://img.shields.io/badge/Xcode-13.3-blue)]()

# UML
![](https://i.imgur.com/lv0w1TS.png)

# 구현내용

| 앱 실행 예시 | 접근성 작동 예시 |
| -------- | -------- |
| ![](https://i.imgur.com/YcqIodV.gif) | ![](https://i.imgur.com/Ewx5BHc.gif)
# 키워드


`JSON`, `Codable`, `Navigation`, `Table View`, `Functional Programming`, `Delegation`, `MVC`, `Design Patterns`

# 핵심경험
- [x] Codable을 채택하여 JSON 데이터와 매칭할 모델
 타입 구현
- [x] 스네이크 케이스 또는 축약형인 JSON 키 값을 스위프트의 네이밍에 맞게 변환
- [x] 테이블뷰의 Delegate와 Data Source의 역할의 이해
- [x] 테이블뷰의 셀의 재사용 이해
- [x] 테이블뷰의 전반적인 동작 방식의 이해
- [x] 주어진 JSON 데이터를 파싱하여 테이블뷰에 표시
- [x] 내비게이션 컨트롤러를 활용한 화면 전환
- [x] 뷰 컨트롤러 사이의 데이터 전달
- [x] 오토 레이아웃을 적용하여 다양한 기기에 대응
- [x] Word Wrapping / Line Wrapping / Line Break 방식의 이해
- [x] 접근성(Accessibility)의 개념과 필요성 이해
- [x] Dynamic Types를 통해 텍스트 접근성 향상

# 기능설명
## Models
### Expo
> Expo의 정보를 parsing 받기 위한 구조체입니다.
### Entry
> 작품들의 정보를 parsing 받기 위한 구조체입니다.
> 작품 이미지의 정보는 `string` 값이지만, 해당 구조체를 확장하여 외부에서는 간편하게 `UIImageView` 타입으로 받을 수 있도록 했습니다.
### JSONDecoder+Extension
> `JSON` 파일을 Parsing하기 위한 메서드를 정의하기 위한 파일입니다.
> 기존 `JSONDecoder` 타입을 확장해서 특정한 JSON 파일을 parsing 받을 수 있도록 했습니다.

## Views
### MainUIScrollView
> 앱 실행시 처음 보일, 만국박람회의 설명에 관한 화면이 띄워지는 Main View 입니다.
### ItemTableViewCell
> 작품 리스트의 Table에 쓰일 Custom Cell View 입니다.
### ItemDescriptionUIScrollView
> 작품의 상세페이지에 쓰일 View 입니다.

## Controller
### MainViewController
> MainUIScrollView를 관리하는 ViewController 입니다.
### ItemTableViewController
> 작품의 목록이 띄워질 TabelViewController 입니다.
### ItemDescriptionViewController
> ItemDescriptionUIScrollView을 관리하는 ViewController 입니다.
