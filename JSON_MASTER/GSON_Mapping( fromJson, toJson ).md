# json -> object 는 fromJson
# object -> json 은 toJson

```java
public class Animal {
    private int nLeg;
    private String name;
}
```

```JAVA
public class AnimalTest {
 
    @Test
    public void testJson() {
        Gson gson = new Gson();
 
        String json = "{\"nLeg\":4, \"name\": \"Bill\"}";
        
        // animal 객체로 변경
        Animal animal = gson.fromJson(json, Animal.class);
        // jsonObject로 변경
        JsonObject jsonObject = gson.fromJson(json, JsonObject.class);
        
        
        String reJson = gson.toJson(animal);
        System.out.println(reJson);
    }
}
```
