# selenium-Java-flow-using-POM-and-Test-NG
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
