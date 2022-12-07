```JAVA
import com.google.gson.Gson;
import com.google.gson.JsonObject; 

public void test() {
    	int[] arr = {1,2,3};
        JsonObject jsonObject = new JsonObject();   
        Gson gson = new Gson();
        
        jsonObject.add("array", gson.toJsonTree(arr));   // // jsonObject.add("array", gson.toJsonTree(arr));
        jsonObject.toString();
```
