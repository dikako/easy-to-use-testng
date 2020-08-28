# easy-to-use-testng
Easy to use TestNG &amp; Allure Report

*Requirment:*
* Install Allure Report https://docs.qameta.io/allure/
* IDE Eclipse, Intellij, VsCode etc IDE For Java.
* Install Docker https://docs.docker.com/get-docker/
* Selenium Grid On Docker File `docker-compose.yml` 

*Directory*
* `src/test/java/config` > Folder location for all Your Config
* `src/test/java/object` > Folder location for all function reuseable
* `src/test/java/testcases` > Folder location for all Your Testcases
* `src/test/java/utility` > Folder location for all Your Read Excel,csv etc.

*How To use*
#### `src/test/java/config/Setup.java`
* `@BeforeMethod` Before your test run, For Setup your  preferences Browser Setting
* `@AfterMethod` After your Test run, For Setup Close Browser & Take Screenshoot your test

#### `src/test/java/config/Url.java`
* Change `String baseUrl = "Your BASE URL"`
* Function `defaultUrl` For visit your `baseUrl` setup
* Function `urls` For visit any page your web

#### `src/test/java/object/Alert.java`
#### Validate Text Single Element
* Function `byId` Validate text with selector `ID`
* Function `byClass` Validate text with selector `CLASSNAME`
* Function `byXpath` Validate text with selector `XPATH`
* Function `byCss` Validate text with selector `CSS SELECTOR`
* Function `byTagName` Validate text with selector `TAG NAME`
* Function `byLinkText` Validate text with selector `LINK TEXT`
* Function `byName` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Alert;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Alert alert = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Validate Text")
    alert.byId("Your ID Selector", "Your Expected Text Valdiate");
  }
}
```
#### Validate Element Display Single Element
* Function `byIdDisplay` Validate text with selector `ID`
* Function `byClassDisplay` Validate text with selector `CLASSNAME`
* Function `byXpathDisplay` Validate text with selector `XPATH`
* Function `byCssDisplay` Validate text with selector `CSS SELECTOR`
* Function `byTagDisplay` Validate text with selector `TAG NAME`
* Function `byLinkTextDisplay` Validate text with selector `LINK TEXT`
* Function `byNameDisplay` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Alert;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Alert alert = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Validate Element Display")
    
    // true = for element display
    // false = for element not display
    alert.byIdDisplay("Your ID Selector", true);
  }
}
```

#### Get Text Single Element
* Function `byIdGetText` Validate text with selector `ID`
* Function `byClassGetText` Validate text with selector `CLASSNAME`
* Function `byXpathGetText` Validate text with selector `XPATH`
* Function `byCssGetText` Validate text with selector `CSS SELECTOR`
* Function `byTagGetText` Validate text with selector `TAG NAME`
* Function `byLinkGetText` Validate text with selector `LINK TEXT`
* Function `byNameGetText` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Alert;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Alert alert = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Get Text")
 
    alert.byIdDisplay("Your ID Selector");
  }
}
```
