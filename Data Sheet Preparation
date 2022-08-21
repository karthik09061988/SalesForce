package SalesForce;

import java.io.IOException;

import org.apache.poi.xssf.usermodel.XSSFRow;
import org.apache.poi.xssf.usermodel.XSSFSheet;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;

public class FetchdatafromExcel {
	
	
	public static String[][] testData() throws IOException {
	
		XSSFWorkbook book = new XSSFWorkbook("./TestDataExcel/TestData08082022.xlsx");
		XSSFSheet sheet = book.getSheetAt(0);
		
		//By default it consider the first row as default
		int rowCount = sheet.getLastRowNum();
		System.out.println(rowCount);
		XSSFRow row = sheet.getRow(1);
		
		int cellCount = row.getLastCellNum();
		System.out.println(cellCount);
		
		String[][] data=new String[rowCount][cellCount];
		
		for (int i = 1; i <= rowCount; i++) {
			for (int j = 0; j < cellCount; j++) {
				
				String celldatas = sheet.getRow(i).getCell(j).getStringCellValue();
				data[i-1][j]=celldatas;
				
			}}
		book.close();
		return data;
		
		
		}
	

}
