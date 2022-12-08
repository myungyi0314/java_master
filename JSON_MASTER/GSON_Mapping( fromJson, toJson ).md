# json -> object 는 fromJson
# object -> json 은 toJson

```JAVA
public class AnimalTest {
 
    @Test
    public void testJson() {
        Gson gson = new Gson();
 
        String json = "{\"nLeg\":4, \"name\": \"Bill\"}";
        Animal animal = gson.fromJson(json, Animal.class);
        System.out.println(animal);
 
        String reJson = gson.toJson(animal);
        System.out.println(reJson);
    }
}
```
