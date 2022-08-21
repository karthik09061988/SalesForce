package SalesForce;

		import java.io.IOException;

import java.time.Duration;
		import org.openqa.selenium.By;
		import org.openqa.selenium.chrome.ChromeDriver;
		import org.openqa.selenium.chrome.ChromeOptions;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.DataProvider;
import org.testng.annotations.Parameters;
import org.testng.annotations.Test;

import io.github.bonigarcia.wdm.WebDriverManager;

		public class SalesforceLogin {
			
			public ChromeDriver driver;
			//public String excelFileName;			
				
			
@Parameters({"url","username","password"})
@BeforeMethod

		    public void preCondition (String url, String username, String password) throws InterruptedException {
		        // TODO Auto-generated method stub

		        //Open Chrome browser
		    	WebDriverManager.chromedriver().setup();
		        ChromeOptions opt=new ChromeOptions();
		        opt.addArguments("disable-notification");
		        driver = new ChromeDriver(opt);
		        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(30));
		        System.out.println(driver); 
		        driver.manage().window().maximize();
		        
		        //Login to Salesforce
		        
		        driver.get(url);
		        driver.findElement(By.id("username")).sendKeys(username);
		        driver.findElement(By.id("password")).sendKeys(password);
		        driver.findElement(By.id("Login")).click(); 
}
				

				@AfterMethod
				public void postCondition() {
				driver.close();

}
		}
