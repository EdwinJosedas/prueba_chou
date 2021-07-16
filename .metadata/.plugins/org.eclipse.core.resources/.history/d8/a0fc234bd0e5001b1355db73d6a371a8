package com.NewExperience;

//import org.junit.After;
import org.junit.Before;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class PruebaTV {
	
	
	
	
	public WebDriver driver;
	
	// para habilitar el check 
	//true = se selecciona el check
		//false = no selecciona el check
		public boolean SelectSignUpEnable = true;
		public boolean OffersEnable = true;

	@Before	
	
	public void setUp() {
		
		System.setProperty("webdriver.chrome.driver", "./src/test/resources/chromedriver/chromedriver.exe");
		driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("http://automationpractice.com/index.php");
		
	}

	@Test
	
	public void testNewEXperience( ) {
		
		driver.findElement(By.className("login")).click();
		driver.findElement(By.id("email_create")).sendKeys("alexisherrerasalazar2@gmail.com");
		driver.findElement(By.id("SubmitCreate")).click();
		try {
			Thread.sleep(10000);
		} catch (InterruptedException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		String pageHeading = driver.findElement(By.className("page-heading")).getText();
		System.out.println("Page Heading: " +pageHeading);
		
		driver.findElement(By.id("id_gender1")).click();
		driver.findElement(By.id("customer_firstname")).sendKeys("Alexis");
		driver.findElement(By.id("customer_lastname")).sendKeys("Herrera Salazar");
		driver.findElement(By.id("passwd")).sendKeys("AlexisHS1992");
		
		WebElement DAYS = driver.findElement(By.name("days"));
		Select selectDays = new Select(DAYS);
		selectDays.selectByValue("28");
		
		WebElement MONTHS = driver.findElement(By.name("months"));
		Select selectMonths = new Select(MONTHS);
		selectMonths.selectByValue("12");
		
		WebElement YEARS = driver.findElement(By.name("years"));
		Select selectYears = new Select(YEARS);
		selectYears.selectByValue("1992");
		
		WebElement CheckNewsletter = driver.findElement(By.id("newsletter"));
		if(SelectSignUpEnable) CheckNewsletter.click();
		
		WebElement CheckOffers = driver.findElement(By.id("optin"));
		if(OffersEnable) CheckOffers.click();
		
		driver.findElement(By.id("company")).sendKeys("Lugares Travel");
		driver.findElement(By.id("address1")).sendKeys("Cra 82 B 42 C 39");
		driver.findElement(By.id("address2")).sendKeys("Floor 3");
		driver.findElement(By.id("city")).sendKeys("Bogota");
		
		WebElement SelState = driver.findElement(By.name("id_state"));
		Select selectState = new Select(SelState);
		selectState.selectByValue("7");
		
		driver.findElement(By.id("postcode")).sendKeys("11111");
		
		WebElement SelCountry = driver.findElement(By.name("id_country"));
		Select selectCountry = new Select(SelCountry);
		selectCountry.selectByVisibleText("United States");
		
		driver.findElement(By.id("other")).sendKeys("Hello World");
		
		driver.findElement(By.id("phone")).sendKeys("1234567");
		
		driver.findElement(By.id("phone_mobile")).sendKeys("12345678910");
	
		driver.findElement(By.id("alias")).clear();
		driver.findElement(By.id("alias")).sendKeys("ALEXISHS123*");
		driver.findElement(By.id("submitAccount")).click();
		
		
		
					
		}
		


	//@After
	//public void tearDown() {
		// TODO Auto-generated method stub
		//driver.quit();
			//}
	
	
	
}
