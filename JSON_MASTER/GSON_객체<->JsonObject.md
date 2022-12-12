# GSON 객체 생성 방법

#### new Gson()
#### new GsonBuilder.create()

https://hianna.tistory.com/629#gson12-1

```JAVA
public class GsonExample {
 
    public static void main(String[] args) {
 
        Gson gson = new Gson();
        String jsonData = "{\"channelCode\":[\"G\",\"B\",\"S\"]}";
        
        // Json key, value 추가
        JsonObject jsonObject = new JsonObject();
        jsonObject.addProperty("name", "anna");
        jsonObject.addProperty("id", 1);
 
        // JsonObject를 Json 문자열로 변환한다.
        String jsonStr = gson.toJson(jsonObject);
        
        // Json String을 JsonObject 데이터로 변환한다.
        JsonObject convertedObject1 = gson.fromJson(jsonData, JsonObject.class);
        JsonObject convertedObject2 = new Gson().fromJson(jsonData, JsonObject.class); 
        
        // 생성된 Json 문자열 출력
        System.out.println(jsonStr); // {"name":"anna","id":1}
        
    }
}

```
