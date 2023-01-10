# GSON 객체 생성 방법

#### new Gson()
#### new GsonBuilder.create()

https://hianna.tistory.com/629#gson12-1

## 기본적인 toJson, fromJson 사용법

```JAVA
public class GsonExample {
 
    public static void main(String[] args) {
 
        Gson gson = new Gson();
        String jsonData = "{\"channelCode\":[\"G\",\"B\",\"S\"]}";
        
        // Json key, value 추가
        JsonObject jsonObject = new JsonObject();
        jsonObject.addProperty("name", "anna");
        jsonObject.addProperty("id", 1);
 
        // JsonObject를 String Json 문자열로 변환한다.
        String jsonStr = gson.toJson(jsonObject);
        
        // Json String을 JsonObject 데이터로 변환한다.
        JsonObject convertedObject1 = gson.fromJson(jsonData, JsonObject.class);
        JsonObject convertedObject2 = new Gson().fromJson(jsonData, JsonObject.class); 
        
        // 생성된 Json 문자열 출력
        System.out.println(jsonStr); // {"name":"anna","id":1}
        
    }
}

```

## vo 객체매핑방법

```java
public class JsonTestVO {
    @Test
    public void testJson() {
        Gson gson = new Gson();
        
        // String json = "{\"lastName\":myungYi, \"firstName\": \"carry\", \"age\": 4}";
        
        // @SerializedName("lastInfo") gson anotation으로 키값을 변경하였음
        // 변경된 값으로만 들어가기 때문에 anotation을 지우면 다시 원상태로 객체에 데이터가 맵핑된다.
        String json = "{\"lastInfo\":loveMyung, \"firstInfo\": \"park\", \"age\": 4}";
        MyInfor infor = gson.fromJson(json, MyInfor.class);
        System.out.println(infor);

        String reJson = gson.toJson(infor);
        System.out.println(reJson);   // {"lastInfo":"loveMyung","firstInfo":"park","age":4}
    }
    class MyInfor {
        @SerializedName("lastInfo")
        private String lastName;
        
        @SerializedName("firstInfo")
        private String firstName;
        
        private int age;
    }
}
```

![image](https://user-images.githubusercontent.com/52149400/207106616-0b1896c7-9454-4972-9daa-94305c7506af.png)
