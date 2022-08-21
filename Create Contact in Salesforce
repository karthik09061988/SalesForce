package SalesForce;

import java.io.IOException;

import org.openqa.selenium.By;
import org.testng.annotations.DataProvider;
import org.testng.annotations.Test;

public class SalesforceAccountcreation extends SalesforceLogin {

@Test(dataProvider = "FetchdatafromExcel")

public void runSalesforceAccountcreation (String FirstName, String LastName, String Email, String Account) throws InterruptedException {
								
					        
		        driver.findElement(By.xpath("//div[@data-aura-rendered-by='439:83;a']")).click();
		        driver.findElement(By.xpath("//input[@placeholder='Search apps and items...']")).sendKeys("Contacts");
		        
		        driver.findElement(By.xpath("//b[text()='Contacts']")).click();
		        
		        Thread.sleep(500);	
		        
		        driver.findElement(By.xpath("//div[text()='New']")).click();
		        driver.findElement(By.xpath("//button[@data-value='--None--']")).click();
		        
		        driver.findElement(By.xpath("//span[text()='Mr.']")).click();
		        
		        driver.findElement(By.xpath("//input[@placeholder='First Name']")).sendKeys(FirstName);
		        driver.findElement(By.xpath("//input[@placeholder='Last Name']")).sendKeys(LastName);
		        driver.findElement(By.xpath("//label[text()='Email']/following::input")).sendKeys(Email);
		      
		        
		        //Account setup
		        driver.findElement(By.xpath("//input[@placeholder='Search Accounts...']")).click();
		        
		      	        
		        driver.findElement(By.xpath(" //span[@title='New Account']")).click();
		        
		        driver.findElement(By.xpath("//input[@class=' input']")).sendKeys(Account);
		        
		        driver.findElement(By.xpath("(//span[text()='Save'])[2]")).click();
		        
		        
		        Thread.sleep(100);	
		        
		        
		        driver.findElement(By.xpath("//button[@class='slds-button slds-button_brand']")).click();
		        		                		     	        
		        String Contactname = driver.findElement(By.xpath("//span[@class='custom-truncate uiOutputText']")).getText();
		        System.out.println(Contactname);
		        
}

@DataProvider(name="FetchdatafromExcel")
//public String[][] sendData() throws IOException {
	public String[][] readData() throws IOException {
	
	return FetchdatafromExcel.testData();
		     		    }
		    
		}
