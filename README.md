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
    alert.byId("Your Selector", "Your Expected Text Validate");
  }
}
```

#### Validate Text By Index Element
* Function `byIdByIndex` Validate text with selector `ID`
* Function `byClassByIndex` Validate text with selector `CLASSNAME`
* Function `byXpathByIndex` Validate text with selector `XPATH`
* Function `byCssByIndex` Validate text with selector `CSS SELECTOR`
* Function `byTagByIndex` Validate text with selector `TAG NAME`
* Function `byLinkTextByIndex` Validate text with selector `LINK TEXT`
* Function `byNameByIndex` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Validate Text  BY Index")
 
    alert.byIdByIndex("Your Selector", index, "Your Expected Text Validate");
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
    alert.byIdDisplay("Your Selector", true);
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
    
    url.urls("/Your Page Need Get Text");
 
    alert.byIdGetText("Your Selector");
  }
}
```

#### Get Text By Index Element
* Function `byIdGetTextIndex` Validate text with selector `ID`
* Function `byClassGetTextIndex` Validate text with selector `CLASSNAME`
* Function `byXpathGetTextIndex` Validate text with selector `XPATH`
* Function `byCssGetTextIndex` Validate text with selector `CSS SELECTOR`
* Function `byTagGetTextIndex` Validate text with selector `TAG NAME`
* Function `byLinkTextGetTextIndex` Validate text with selector `LINK TEXT`
* Function `byNameGetTextIndex` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Get Text By Index");
 
    alert.byIdGetTextIndex("Your Selector", index, "Your Expected Text Validate");
  }
}
```

#### Return Text Single Element
* Function `byIdReturnText` Validate text with selector `ID`
* Function `byClassReturnText` Validate text with selector `CLASSNAME`
* Function `byXpathReturnText` Validate text with selector `XPATH`
* Function `byCssReturnText` Validate text with selector `CSS SELECTOR`
* Function `byTagReturnText` Validate text with selector `TAG NAME`
* Function `byLinkTextReturnText` Validate text with selector `LINK TEXT`
* Function `byNameReturnText` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Return Text");
 
    alert.byIdRetunText("Your Selector");
  }
}
```

#### Return Text By Index Element
* Function `byIdReturnTextIndex` Validate text with selector `ID`
* Function `byClassReturnTextIndex` Validate text with selector `CLASSNAME`
* Function `byXpathReturnTextIndex` Validate text with selector `XPATH`
* Function `byCssReturnTextIndex` Validate text with selector `CSS SELECTOR`
* Function `byTagReturnTextIndex` Validate text with selector `TAG NAME`
* Function `byLinkTextReturnTextIndex` Validate text with selector `LINK TEXT`
* Function `byNameReturnTextIndex` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Return Text By Index");
 
    alert.byIdReturnTextIndex("Your Selector", index);
  }
}
```

#### Validate Text Contains Single Element
* Function `byIdContains` Validate text with selector `ID`
* Function `byClassContains` Validate text with selector `CLASSNAME`
* Function `byXpathContains` Validate text with selector `XPATH`
* Function `byCssContains` Validate text with selector `CSS SELECTOR`
* Function `byTagContains` Validate text with selector `TAG NAME`
* Function `byLinkTextContains` Validate text with selector `LINK TEXT`
* Function `byNameContains` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Validate Text Contains");
 
    alert.byIdContains("Your Selector", "Your Expected Text Validate");
  }
}
```

#### Validate Text Contains By Index Element
* Function `byIdContainsIndex` Validate text with selector `ID`
* Function `byClassContainsIndex` Validate text with selector `CLASSNAME`
* Function `byXpathContainsIndex` Validate text with selector `XPATH`
* Function `byCssContainsIndex` Validate text with selector `CSS SELECTOR`
* Function `byTagNameContainsIndex` Validate text with selector `TAG NAME`
* Function `byLinkTextContainsIndex` Validate text with selector `LINK TEXT`
* Function `byNameContainsIndex` Validate text with selector `Name`
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
    
    url.urls("/Your Page Need Validate Text Contains BY Index");
 
    alert.byIdContainsIndex("Your Selector", index, "Your Expected Text Validate");
  }
}
```

#### Validate Url 
* Function `urlValidate` For Return Url
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
    
    url.urls("/Your Page Need Validate Text  BY Index");
 
    alert.urlValidate("Expected Your Url");
  }
}
```

#### `src/test/java/object/Button.java`
#### Click Button Single Element
* Function `byId` Validate text with selector `ID`
* Function `byClass` Validate text with selector `CLASSNAME`
* Function `byXpath` Validate text with selector `XPATH`
* Function `byCss` Validate text with selector `CSS SELECTOR`
* Function `byTag` Validate text with selector `TAG NAME`
* Function `byLinkText` Validate text with selector `LINK TEXT`
* Function `byName` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Button;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Button button = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Click Button");
    button.byId("Your Selector");
  }
}
```

#### Click Button By Index Element
* Function `byIdByIndex` Validate text with selector `ID`
* Function `byClassByIndex` Validate text with selector `CLASSNAME`
* Function `byXpathByIndex` Validate text with selector `XPATH`
* Function `byCssByIndex` Validate text with selector `CSS SELECTOR`
* Function `byTagByIndex` Validate text with selector `TAG NAME`
* Function `byLinkTextByIndex` Validate text with selector `LINK TEXT`
* Function `byNameByIndex` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Button;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Button button = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Click Button By Index");
    button.byIdByIndex("Your Selector", index);
  }
}
```

#### Validate Button Enable or Disabled Element
* Function `byIdEnabled` Validate text with selector `ID`
* Function `byClassEnabled` Validate text with selector `CLASSNAME`
* Function `byXpathEnabled` Validate text with selector `XPATH`
* Function `byCssEnabled` Validate text with selector `CSS SELECTOR`
* Function `byTagEnabled` Validate text with selector `TAG NAME`
* Function `byLinkTextEnabled` Validate text with selector `LINK TEXT`
* Function `byNameEnabled` Validate text with selector `Name`
####  Below Sample Code
```
package testcases;
import object.Button;
import config.Setup;
import config.Url;

public class objectAlert extends Setup {
 
  public void testName() {
    Button button = PageFactory.initElements(driver, Alert.class);
    Url url = new Url(driver);
    
    url.urls("/Your Page Need Click Button By Index");
    button.byIdEnabled("Your Selector", true or false);
  }
}
```
