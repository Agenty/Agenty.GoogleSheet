# Agenty.GoogleSheet

Agenty Google sheet script to fetch agent result in google sheet automatically using popular [ImportJSON](https://github.com/bradjasper/ImportJSON) library.

`GetAgentResult.gs` adds an `=GetAgentResult()` function to your Google spreadsheet, allowing quick agent result importing from [Agenty API](https://www.agenty.com/docs/api). To use go to `Tools` > `Script Editor` and add the `GetAgentResult.gs` file. Now in your spreadsheet you can access the `GetAgentResult()` function. Use it like this:

    =GetAgentResult("agent id here",  "api key here",  "/result/ProductName,/result/ProductPrice")
    
Or without field names definition explicitly:
 
    =GetAgentResult("agent id here",  "api key here",  "/result/")
     
**Function**

    GetAgentResult()

**Parameters**

| Name |  Description|
|--|--|
| `AgentId` |  A unique identifier of your agent (Maximum 10 character)|
| `APIKey` |  A valid Agenty API Key ([Get it from here](https://www.agenty.com/), if you don't have one)|
| `Fields` |  Comma separated fields to import in sheet (no space allowed). Be sure to use `/result/` before field name because Agenty always display the agent result in a array named "result"|


**Credit**
This library uses the ImportJSON project. See the author, contributor, issues details [here](https://github.com/bradjasper/ImportJSON).
