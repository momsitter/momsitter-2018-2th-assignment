# Momsitter 2018 Backend Coding Assignment

## Description

맘편한세상 백앤드 개발자 지원자를 위한 코딩과제입니다. 본 과제에서는 몇가지 간단한 기능을 구현하게 됩니다.

## Tools

아래는 본 과제에서 사용할 수 있는 몇가지 툴의 예시입니다.
과제구현에 직접적인 솔루션이 되는 라이브러리 등은 본 과제에서는 제한됩니다.
지원자분이 특정 툴을 사용해도 되는지에 대한 여부는 담당자에게 자유롭게 질의해주시면 됩니다.

* [Node](https://github.com/nodejs/node)
* [Express](https://github.com/expressjs/express)
* [Django](https://tutorial.djangogirls.org/en/django_models/)

## Requirements

프로필 이미지를 제공하기 위한 API 를 구현하는 문제입니다.
(이미지는 [더미 이미지](./dummy-image.png) 를 사용하셔도 되고, 다른 원하는 이미지를 사용하셔도 됩니다.)

* 프로필 이미지 제공을 위한 API URL 설계 및 구현

다음은 request 예시 입니다.
imageId 에 상관없이 같은 더미 이미지를 제공하면 됩니다.
(Route 명이나 방법등은 자유입니다!)

| Method | Route |
|--------|--------|
| GET  | /profile/image/:imageId |

다음은 response 예시 입니다.

| Key | Value |
|--------|--------|
|cache-control |max-age=290304000, public |
|status |200|
|content-length |10860|
|content-type |image/jpeg|
|last-modified|Sun, 18 Feb 2018 08:20:39 GMT|

* Authenticate
 * Passport 혹은 OAuth 등을 이용하여 valid 한 token 를 가지고 있는 사용자에 한에 이미지를 제공해야 합니다. 어떤 라이브러리 & 인증 로직을 사용하는지는 자유입니다!
 * [cloudimage](https://docs.cloudimage.io/go/cloudimage-documentation/en/operations/) 와 같은 token 로직 혹은 HTTP/2 pseudo-header 등을 사용하는 로직도 가능합니다.
* 쿼리 스트링을 이용하여 리사이징 기능을 사용할 수 있도록 구현
 * 이미지 라이브러리는 어떤것을 사용해도 무방합니다.

다음은 30번 프로필 이미지를 가로 세로 크기는 100px 으로 리사이징 하여 제공하는 API 예시 입니다.

| Method | Route |
|--------|--------|
| GET  | /profile/image/30?resize=true&width=100&height=100 |


## Bonus (Optional)

보너스 항목은 의무적으로 구현해야 하는 사항은 아닙니다!
하지만 개선되어야 할 점, 추가되면 좋을 기능, 그 밖의 지원자분의 아이디어 등을 추가적으로 구현했을 때
평가 기준에 더하여 보너스 포인트를 받을 수 있는 점입니다. 아래는 예시입니다.

* 캐시 컨트롤에 대한 고려
* 예외 케이스에 대한 고려
* 성능을 개선 시킬 수 있는 점에 대한 고려
* 요구사항에 리스팅되지 않은 추가적인 기능
* 그 밖의 과제에 플러스 요인이 될 수 있는 요소 (너무나 다양합니다)

## Evaluation Criteria

지원자분이 구현한 코드를 바탕으로 어떤점이 잘되었고 어떤점이 미흡한지 체크해보게 됩니다.
API 의 구동 여부를 살펴보기 위해선 [Postman](https://www.getpostman.com/) 혹은 [curl](https://curl.haxx.se/) 을 사용합니다.

1. 주어진 요구사항을 만족하는가
2. 재사용성, 퍼포먼스, 확장 가능성 등
3. 코드의 가독성
4. 주석 및 문서화

## Help & Support

맘편한세상 개발팀은 인더스트리의 많은 문제들이 개인의 힘에 더해서 팀원의 힘으로 해결 할 수 있으며,
또한 그렇게 되어야 하는 것들이 많다고 생각합니다.
코딩의 직접적인 솔루션에 대한 도움을 어려울 수 있지만 그 밖의 어려움이나 도움이 필요할 때는 언제든지
담당자에게 연락을 주세요.
어쩌면 지원자분이 생각하는 아이디어가 구상만으로 그치기에는 너무나도 아까울 수 있습니다. :)

## Feedback

맘편한세상은 항상 지원자분의 의견을 듣고 개선해나가기 위해 끊임없이 노력하고 있습니다.
코딩과제를 수행하시면서 생각하신 의견이 있으시다면 언제든지 저희 담당자에게 알려주시면 감사하겠습니다!