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
public class logintest{
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
**3. Home page**
public class homepage{
WebDriver driver;
@findBy(XPath ="//input[@text='search']");
WEbElement Serachbox;
public homepage(Webdriver,driver){
this.driver =driver;
pageFactory.initElement(driver,this);
}
public void searchproduct(String product){
serachproduct.sendkeys("Sims");
}
}
**4. Product Page**
Public Class productpage{
WebDriver driver;
@findBy(id="sortdropdown");
WebElement sortdropdown;
@findBy(id ="radiobutton");
Webelement radiobutton;
@findBy(id ="addtocart");
WebElement addtocart;
public productpage (Webdriver driver){
this.driver = driver;
pageFactory.initElement(driver,this);
}
public void sortdropdown {
select sc = new select(sortdropdown);
}
sc.selectbyvisualtext("Price low to High");
public void radiobutton{
radiobutton.click();
}
public void addtocart{
addtocart.clicka();
}
**5. cart Page**
public class cartpage{
Webdriver driver;
@findBy(id="checkout");
WebElement Chacekout;
public cartpage (WebDriver driver){
this.driver = driver;
pageFactory.initElement(driver ,this);
}
public void checkout{
checkoutbtw.click();
}
}
**6. Checkout**
Public class chcekoutpage {
 WebDriver driver;

    @FindBy(id="first-name")
    WebElement firstName;

    @FindBy(id="last-name")
    WebElement lastName;

    @FindBy(id="postal-code")
    WebElement postalCode;

    @FindBy(id="continue")
    WebElement continueBtn;

    @FindBy(id="finish")
    WebElement finishBtn;
    public chcekoutpage(Webdriver driver){
    this.driver = driver;
    pageFactory.initElement(driver,this);
    }
    public void chcekoutpage{
    firstName.sendkeys
