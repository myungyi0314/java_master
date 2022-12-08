# Parsing 이란 ? 
1. 문장이 이루고 있는 구성 성분을 분해하고 분해된 성분의 위계 관계를 분석하여 구조를 결정하는 것
2. 웹페이지에서 원하는 데이터를 추출하여 가공하기 쉬운 상태로 바꾸는 것
3. 데이터를 조립해 원하는 데이터를 빼내는 것
4. 어떤 data를 원하는 form으로 만들어 내는 것


```JSON
{
	"status":"1",
	"message":"OK",
	"result":
	[
		{
		"Number":"1",
		"Stamp":"A123",
		"hash":"0xa8948b23fe3",
		"Name":"Apple"
                 },
                {
                "Number":"2",
		"Stamp":"A124",
		"hash":"0xf146b23d537",
		"Name":"Lemon"
                 }
         ]
}
```
# Parsing 작업
```JAVA
String status = jsonObject.get("status").getAsString();
String message = jsonObject.get("message").getAsString();

// result의 {}, {}가 각각의 Array로 받아올 수 있고, 각각의 Array를 Element로 분리가 가능하다.
// result에 {}가 2개 이기 때문에 size는 2가 되고, 0과 1의 인덱스를 가진 데이터로 나눌 수 있다.
JsonArray jsonArray = jsonObject.getAsJsonArray("result");
JsonElement jsonElement1 = jsonArray.get(0);  -> Apple
JsonElement jsonElement2 = jsonArray.get(1);  -> Lemon
String Name1 = jsonElement1.getAsJsonObject().get("Name").getAsString();
String Name2 = jsonElement2.getAsJsonObject().get("Name").getAsString();

---
[Name1 = Apple]
[Name2 = Lemon]
```
# 데이터 형식
```shell
JsonObject => { {}, {}, [{}, {}, {}] }
JsonArray => [{}, {}, {}]
JsonElement => {} 
```
