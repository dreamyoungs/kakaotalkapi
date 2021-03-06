# 꿈많은청년들 : KakaoTalk 알림톡/친구톡 API 문서

## 개요

카카오톡 알림톡/친구톡 API 문서입니다. 꿈많은청년들에서 제공하는 version 1.0 알림톡/친구톡입니다.

```
❗️WARNNING: 본 문서는 향후 v2.0 이 출시되면 단계적으로 Deprecate 될 수 있습니다.
v2.0이 출시되면 다양한 방법을 통해 공지할 계획입니다.
```


---

## 계정 생성
https://cloudturing.com 을 통해서 가입후 영업담당자를 통해 승인을 받습니다.

카카오톡 프로필을 등록후 키를 발급 받습니다.

## Webhook / API 작성 방법
* 통신간에는 특별한 암호화 없이 동작하므로 모든 API는 HTTPS를 이용해서 통신해야만 합니다.
* 기본 주소는 https://api.cloudturing.com/v1 으로 시작하게 됩니다.
* 테스트는 cURL을 이용해 주시기 바랍니다.
* 제공되는 샘플 코드는 현재 HTTP만 제공하고 있습니다. 이 부분 양해해 주시기 바랍니다.

---

## API 목록
* [알림톡](./alimtalk.md#알림톡)
    * [메세지](./alimtalk.md#메세지)
        * [알림톡 목록 조회](./alimtalk.md#알림톡-목록-조회)
        * [알림톡 일반 발송](./alimtalk.md#알림톡-일반-발송)
        * [알림톡 전송 취소](./alimtalk.md#알림톡-전송-취소)
        * [알림톡 단건 조회](./alimtalk.md#알림톡-단건-조회)
    * [템플릿](./alimtalk.md#템플릿)
        * [템플릿 리스트 조회](./alimtalk.md#템플릿-리스트-조회)
* [친구톡](./friendtalk.md#친구톡)
    * [이미지](./friendtalk.md#이미지)
        * [이미지 업로드](./friendtalk.md#이미지-업로드)
        * [이미지 파일 리스트](./friendtalk.md#이미지-파일-리스트)
        * [이미지 삭제](./friendtalk.md#이미지-삭제)
    * [메시지](./friendtalk.md#메시지)
        * [친구톡 발송](./friendtalk.md#친구톡-발송)
        * [친구톡 발송 목록 조회](./friendtalk.md#친구톡-발송-목록-조회)
        * [친구톡 발송 취소](./friendtalk.md#친구톡-발송-취소)
        * [친구톡 단건 조회](./friendtalk.md#친구톡-단건-조회)
* [Object](./object.md#Object)
    * [Button Object](./object.md#Button-Object)
---
## API 기본 설명

📣`공통`  
```baseURL : https://api.cloudturing.com/v1  
Default Content-Type : application/json
모든 통신은 `UTF-8` 로 이루어집니다.  
통신시 `Header`에는 `Authorization`를 이용하여 발급된 키를 첨부 하여야 합니다.
```

```
"headers":{
   "Content-Type": "application/json",
   "Authorization": `Bearer 발급된 키`,
}
```

GET/POST/DELETE :  
`Content-Type: application/json`  
File Upload 의 경우에만   
`Content-Type: multipart/form-data`

---





