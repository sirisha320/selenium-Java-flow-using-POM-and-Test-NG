# selenium-Java-flow-using-POM-and-Test-NG
**1. Base Test**
public basetest{
protected Webdriver driver;
@Beforemethod
public void setup(){
driver = new ChromeDriver();
driver.manage().window().maximize();
driver.manage().timeouts().implicitlywait(driver,duration.ofseconds(10));
Webelementwait wait = new webelementwait(driver,duration.ofseconds(10));
driver.get("http.path");
}
@Aftermethod
public void teardown () {
driver.quit();
}
}
**2. Login Flow**
public logintest{
Webdriver driver;
@findBy(id="username");
WebElement username;
@findBy("id="password");
WebElement password;
@findBy("id="loginbtw");
WebElement loginbtw;
public Loginpage(Webdriver driver) {
this.driver = driver;
pageFactory.initElement(String user,string pass){
username.sendkeys(user);
password.sendkeys(122);
Loginbtw.click();
}
}
