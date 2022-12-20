```java

    String test = "{\"id\":\"gamsalog\",\"type\":\"NONE\",\"expireDay\":330,\"searchable\":true,\"shardSize\":2,\"replicaSize\":0,\"refreshInterval\":\"1s\"}";
    
    JsonObject jsonObject = gson.fromJson(test, JsonObject.class);
    
    JsonObject addJsonKeyDownloadPledge = new JsonObject();
    addJsonKeyDownloadPledge.add("downloadPledge", gson.toJsonTree(jsonObject.getAsJsonObject()));
    
    
    result  == {"downloadPledge":{"originName":"ㄷ","reason":"ㅅㄷㄴㅅ","destructionDate":"2022/12/14","recvExternalCompany":"ㄷㄷㄷㄷ"}}
    
    downloadPledge 키가 붙는다.

```
