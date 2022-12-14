### **클라우드 기반 파이썬 네트워크 정보시스템 과정 팀 프로젝트 "트리어스(TreeEarth)"**   
#### 트리어스(TreeEarth)는 "환경"을 주제로, 진행중인 환경보호 캠페인 소개와 참가 신청, 산불 같은 자연재해로 피해를 입은 환경을 복구 및 보호하기 위한 활동을 지원하는 후원 참여, 반려식물/나무와 부자재를 판매하고 구매함으로써 수익금 일부를 환경보호 활동에 사용하는 서비스를 제공하는 웹 사이트 입니다.   
![트리어스 로고](https://user-images.githubusercontent.com/110509005/193780027-42f1e326-9810-44f2-a22e-07dcfb1c3378.png)   
* * *   
* **관리자 기능과 사용자 기능을 구분한 MVC패턴 기반으로 구현**      
* **프로젝트 개발 기간 : 2022.07.19 ~ 2022.09.07**   
* **개발 인원 : 총 8명**   
* **사용 언어 : Java / JSP / JavaScript / jQuery / CSS3 / HTML5**      
* **개발 Tool : Eclipse**   
* **서버 : Apache Tomcat**   
* **데이터베이스 및 형상 관리 : MySQL / GitHub**   
* * *   
### **1. 관리자 기능 구현**   
> * 관리자 유스케이스 다이어그램   
![슬라이드9](https://user-images.githubusercontent.com/110509005/193634227-76274254-4ae7-4b58-8800-0d661d8d7eca.PNG)   
   
> * 사이트의 메인화면 입니다.   
![슬라이드17](https://user-images.githubusercontent.com/110509005/193634576-7e126f18-a075-449f-a8d7-30821f3ad513.PNG)   
   
> * 관리자 계정인 'admin'으로 로그인을 한 후 계정을 클릭하면 관리자 페이지로 이동합니다.   
판매하는 상품과 회원들의 주문 관리, 캠페인과 후원, 커뮤니티, 회원목록을 관리 할 수 있습니다.   
![슬라이드18](https://user-images.githubusercontent.com/110509005/193635101-186ae2d0-5b11-4535-952c-acb68a2fedfc.PNG)   

> * 상품 관리에서는 스토어에 판매하는 상품을 등록하고 등록 한 상품 목록들을 관리합니다.   
상품 등록 버튼을 클릭하면 판매할 상품의 이름과 가격, 상세 내용, 태그를 작성할 수 있는 폼으로 이동하며 상품 사진 첨부와 반려식물/나무/부자재 등 세 개의 분류 목록을 선택할 수 있습니다.   
![슬라이드19](https://user-images.githubusercontent.com/110509005/193636877-3acebdc0-db3e-4126-863f-812ee45bc82a.PNG)   

> * 등록 된 상품 목록 버튼을 클릭하면 스토어에 등록한 모든 상품의 목록을 조회할 수 있습니다.   
상품을 선택하면 그 상품의 상세페이지로 이동합니다.   
![슬라이드20](https://user-images.githubusercontent.com/110509005/193637594-c8efae51-8faf-4b65-a967-be1338d5ef1b.PNG)   
![슬라이드21](https://user-images.githubusercontent.com/110509005/193637632-93f1ffbd-7e9c-42c6-8ad0-5f73180667ef.PNG)   

> * 주문 관리의 주문목록 버튼을 클릭하면 회원들이 스토어에서 구매한 상품에 대한 주문 정보를 조회할 수 있습니다.   
![슬라이드22](https://user-images.githubusercontent.com/110509005/193639264-b8e0d762-30bd-401c-a323-7847cb3c8aa4.PNG)   

> * 캠페인 목록에서 캠페인 공고 작성 버튼을 클릭하면 공고를 등록할 수 있는 폼 페이지로 이동합니다.   
캠페인 신청자 목록에서는 캠페인 공고에 참가 신청을 한 회원들의 신청 내역을 확인할 수 있습니다.   
![슬라이드23](https://user-images.githubusercontent.com/110509005/193640678-dab6a9a6-f317-40a8-aa23-464c66b098ef.PNG)   
![슬라이드24](https://user-images.githubusercontent.com/110509005/193640716-caed8cbf-be46-4508-b38a-8d797304901e.PNG)   

> * 진행하는 후원을 등록하고 회원들의 후원 내역을 조회할 수 있습니다.   
![슬라이드25](https://user-images.githubusercontent.com/110509005/193641712-382a66fd-69cf-4e07-b657-4ca1121ede4e.PNG)   
![슬라이드26](https://user-images.githubusercontent.com/110509005/193641734-b9c6fa68-2f31-4e52-9a6f-bba03891f226.PNG)   

> * 커뮤니티에서 캠페인 참여후기와 자유게시판의 게시글 중 신고받은 게시글들을 조회하고 관리할 수 있습니다.   
![슬라이드27](https://user-images.githubusercontent.com/110509005/193642878-27151c73-ba47-4b4b-b12b-d541d58bc833.PNG)   

> * 회원 목록 버튼을 클릭하면 회원들의 아이디, 이름, 주소, 이메일 등의 가입 정보를 확인할 수 있습니다.   
![슬라이드28](https://user-images.githubusercontent.com/110509005/193643474-1f59b34d-a8bc-496a-a063-159fc18343e0.PNG)   
   
### **2. 사용자(user) 기능 구현**   
> * 사용자 유스케이스 다이어그램   
![트리어스_최종본10](https://user-images.githubusercontent.com/110509005/193846979-585ee79e-5f9c-4f65-8ed9-fe6fba07a1f2.png)   

> * 사용자 회원가입 기능입니다. 사이트 상단 오른쪽의 로그인을 클릭하면 로그인 및 회원가입 팝업창이 나타납니다. 팝업창에서 '회원가입'을 클릭하면 가입 페이지로 이동합니다.   
가입 약관 체크, 이메일 본인 인증, 회원 정보 입력을 통해 회원가입을 진행 할 수 있습니다.              
![트리어스_최종본2](https://user-images.githubusercontent.com/110509005/193781215-e20c5909-7963-48f4-9964-ac72f615b5c7.png)   
![슬라이드31](https://user-images.githubusercontent.com/110509005/193784175-84b3aeac-4a57-4066-8235-0a5757721199.PNG)   
![슬라이드32](https://user-images.githubusercontent.com/110509005/193784223-359b0bb0-3768-447a-b6e1-82eeab5f5296.PNG)   

> * 회원가입이 완료되면 회원 계정으로 로그인을 할 수 있습니다.   
로그인 팝업창에서 카카오계정과 연동하여 로그인을 할 수 있습니다.      
![트리어스_최종본3](https://user-images.githubusercontent.com/110509005/193785708-9d8cd6d9-ffac-447e-afc6-4beaaad7ae5f.png)

> * 캠페인 참가 신청 기능입니다.   
캠페인 카테고리에서 진행중인 환경보호 활동 캠페인을 볼 수 있으며 참가 신청 버튼을 클릭하면 신청서를 작성할 수 있습니다.   
![슬라이드34](https://user-images.githubusercontent.com/110509005/193789938-7de30447-6f9b-4396-bfaf-5f09f62eaafe.PNG)   
> * 지원이 완료되면 캠페인 참가 내역 페이지로 이동합니다.   
![슬라이드35](https://user-images.githubusercontent.com/110509005/193792857-5418c90b-c039-4edd-a97c-55358636e134.PNG)   

> * 환경보호 활동에 후원할 수 있는 후원하기 기능입니다.   
진행중인 후원과 목표 금액, 진행률 등을 볼 수 있으며 후원하기 버튼을 클릭하면 후원 페이지 팝업창이 열립니다.   
직접 금액을 입력하거나 지정된 금액 버튼으로 선택할 수 있습니다.   
후원을 클릭하면 결제 시스템이 연결됩니다. 결제가 완료되면 후원 내역을 조회할 수 있습니다.   
![슬라이드36](https://user-images.githubusercontent.com/110509005/194534380-ab597be0-b671-4624-a775-b270722ec3f0.PNG)   
![슬라이드37](https://user-images.githubusercontent.com/110509005/193813840-1bc151e7-19a4-4f9c-9df3-26f5bb506c38.PNG)   
![슬라이드38](https://user-images.githubusercontent.com/110509005/193813897-a86cc4b9-6686-4fa8-a75d-843bc2fc8ae1.PNG)   

> * 반려식물/나무/부자재를 구매할 수 있는 스토어 입니다.   
판매하는 상품 목록들을 조회할 수 있으며 상품을 클릭하면 구매 페이지로 이동합니다.   
원하는 상품 수량을 선택하고 구매하기 버튼을 클릭하면 주문 페이지로 이동, 결제 시스템을 통해 결제를 할 수 있습니다.   
결제가 완료되면 주문 내역 페이지에서 주문 정보를 확인할 수 있습니다.   
![트리어스_최종본4](https://user-images.githubusercontent.com/110509005/193818976-ceac4212-8d08-4bbb-b170-c77d7e48042d.png)   
![슬라이드39](https://user-images.githubusercontent.com/110509005/193819033-061fc83b-9ebc-4b1f-872e-67f8a414fc92.PNG)   
![슬라이드40](https://user-images.githubusercontent.com/110509005/194504414-e12838b0-95f9-4f23-9d70-560f11c8b590.PNG)   
![슬라이드41](https://user-images.githubusercontent.com/110509005/193819097-6b28bd51-205f-4b16-9809-e9aff5927a5b.PNG)   
> * 상품 위시리스트 담기 기능입니다. 상품을 위시리스트에 담으면 위시리스트 페이지로 이동합니다.   
![슬라이드42](https://user-images.githubusercontent.com/110509005/193821694-9b6c84d9-a878-48a1-9fdc-898037d9a95b.PNG)   
> * 장바구니 담기 기능으로 상품을 장바구니에 담을수도 있습니다. 장바구니 페이지에서 담겨진 상품 주문이 가능합니다.   
![슬라이드43](https://user-images.githubusercontent.com/110509005/193823983-d79e4118-500a-4b3d-afab-3cf0df1f40e7.PNG)   

> * 공지사항, 캠페인 후기, 반려나무 성장일기, 자유게시판, Q&A 기능을 이용할 수 있는 커뮤니티 입니다.   
공지사항을 볼 수 있으며 캠페인 후기글을 등록할 수 있습니다.   
반려나무 성장일기에서는 직접 키우는 식물관련 게시글을 작성할 수 있습니다.   
자유게시판에서 자유롭게 게시글을 등록하고 볼 수 있습니다. Q&A에서 문의글을 등록할 수 있습니다.      
![트리어스_최종본13](https://user-images.githubusercontent.com/110509005/194469156-4c4ddcad-ce2c-4a92-a8aa-3f86c8bcd828.png)   
![트리어스_최종본14](https://user-images.githubusercontent.com/110509005/194469209-91fa8fc4-9690-41c3-808b-7b91c5a8202d.png)   
![트리어스_최종본15](https://user-images.githubusercontent.com/110509005/194469687-59ca3ecc-a21b-4639-a9e4-bdd3c526d040.png)   
![트리어스_최종본16](https://user-images.githubusercontent.com/110509005/194469319-e3a4a6de-a2d9-49b5-a5ec-00ae3bb4e44b.png)    
![트리어스_최종본9](https://user-images.githubusercontent.com/110509005/193833489-80b812d4-7c12-4763-b64a-08025ea34683.png)   
![트리어스_최종본17](https://user-images.githubusercontent.com/110509005/194469414-eac03c98-7dfb-4944-8a6c-e7f871671fd9.png)   

> * 자신의 계정을 클릭하여 마이페이지 기능을 이용할 수 있습니다. 회원정보 수정은 계정 아이디와 비밀번호를 통해 가능합니다.    
![트리어스_최종본18](https://user-images.githubusercontent.com/110509005/194469839-81145c85-874a-4371-b954-ddc968a03d99.png)   
![슬라이드48](https://user-images.githubusercontent.com/110509005/193834948-00ed8715-cc3e-409d-9d48-f8c4730a855b.PNG)   

* * *   
**<프로젝트 소감>**   
처음에는 팀원들과 함께 처음으로 하는 팀 프로젝트를 열심히 해서 완성하자는 다짐을 했던 한편, 과연 내가 끝까지 잘 해낼 수 있을까 하는 불안한 마음을 가지고 시작했습니다.   
하지만 팀원들과 꾸준히 회의를 하면서 소통하고 문제가 생기면 함께 원인을 파악하여 해결해나가면서 잘 할수있을거라는 자신감이 생겼습니다.   
지금까지 배웠던 것들을 활용하여 직접 스스로 코드를 구현하면서 생각했던대로 기능이 구현되면 신기하기도 하고 뿌듯하기도 하였습니다. 비록 어렵고 막혔던 부분도 있었지만 다른 팀원들의 도움을 받아서 해결하기도 하였고, 다른 팀원의 어려움을 도와주기도 하였습니다.   
팀 프로젝트를 하면서 커뮤니케이션 능력과 함께 문제 원인을 파악하고 해결해나가는 협동심을 배우고 키울 수 있었으며, 기한 내에 완성된 결과물을 만들었다는 성취감을 느낄 수 있었던 좋은 경험이였습니다.   
* * *   
### 환경보호 캠페인 사이트 "트리어스(TreeEarth)"






