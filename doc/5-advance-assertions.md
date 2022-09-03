# Advance Assertions
* Postman internally uses chai testing framework

* **Parsing response body**:
    * JSON -> `pm.response.json()`
    * XML -> `xml2json(responseBody)`
    * HTML -> `cheerio(pm.response.text())` cheerio allows us to work with DOM 
    * Plain text -> `pm.response.text()`
    * CSV -> `csv-parse/lib/sync` is the built in library for this. 

## Chai Assertion Library 
* Chai is a simple behavior driven human understandable assertion library. eg: `expect([]).to.be.an('array').that.is.empty`
* [Chai Docs](https://www.chaijs.com/api/bdd/)

## Assertions 
* Adding error message to reports.
```js
pm.test("Your test name", function(){
    pm.expect(100).to.eql(100, 'Text which will be included in output/report if this test fails')
})
```
* Working with objects and array and strings
```js
pm.test("Testing object", function(){
    let a = {
        "name" : "abhishek"
    }
    let b = {
        "name" : "abhishek"
    }

    pm.expect(a).to.eql(b) //test passes
    pm.expect(a).to.equal(b) //test fails as it will check if object has same reference. 
    pm.expect(a).to.not.equal(b) // test passes

    let c = let b = {
        "name" : "abhishek", 
        "userName" : "abhishek01"
    }
    pm.expect(a).to.eql(c) //test fails
    pm.expect(a).to.not.eql(c) //test passes

    pm.expect([]).to.be.empty // test passes
    pm.expect([1, 2, 3]).to.include(4) // test fails
    pm.expect(2).to.be.oneOf([1,2,3]) // test passes

    // String & Regex 
    pm.expect('Abhishek Gautam').to.match(/^Abhishek/); //pass 

})
```