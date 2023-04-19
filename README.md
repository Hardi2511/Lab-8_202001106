# Lab-8_202001106

HARDI SANGHANI
202001106

## Que 1 - 6:

Boa.java File: <br/>

package Lab8_p; 

public class Boa { 

	private String name; 
	private int length; // the length of the boa, in feet 
	private String favoriteFood; 
	public Boa (String name, int length, String favoriteFood){ 
	this.name = name; 
	this.length = length; 
	this.favoriteFood = favoriteFood; 
	 } 
	 // returns true if this boa constrictor is healthy <br/>
	public boolean isHealthy(){
	return this.favoriteFood.equals("granola bars");
	 }
	// returns true if the length of this boa constrictor is
	// less than the given cage length
	public boolean fitsInCage(int cageLength){
	return this.length < cageLength;
	 }
	
	// produces the length of the Boa in inches
	public int lengthInInches(){
		return length*12;//feets to inches
	 // you need to write the body of this method
	}
}

BoaTest.java File: <br/>

package Lab8_p;

import static org.junit.Assert.*;  
import org.junit.Before;  
import org.junit.Test;
public class BoaTest2 {	  
	private Boa jen,ken;    
	@Before  
	public void setUp() throws Exception {  
		jen = new Boa("Jennifer", 2, "grapes");  
		ken = new Boa ("Kenneth", 3, "granola bars");  
	}  
	@Test  
 	public void testIsHealthy() {  
		jen = new Boa("Jennifer", 2, "");  
		ken = new Boa ("Kenneth", 3, "granola bars");   
		assertFalse(jen.isHealthy());  
		assertTrue(ken.isHealthy());  
	}  
	@Test  
	public void testFitsInCage() {  
		jen = new Boa("Jennifer", 5, "grapes");  
		ken = new Boa ("Kenneth", 6, "granola bars");  
		assertTrue(jen.fitsInCage(6));  
		assertTrue(jen.fitsInCage(7));  
	}  
	
	@Test  
	public void testlengthInInches() {  
		jen =new Boa("hello",1,"granola bars");  
		ken=new Boa("kenn",2,"grapes");  
		assertEquals(12,jen.lengthInInches());  
		assertEquals(24,ken.lengthInInches());  
	}  
}  

(7) New Method lengthInInches():  
// produces the length of the Boa in inches  
	public int lengthInInches(){  
		return length*12;//feets to inches  
	}  
  
![Screenshot (1724)](https://user-images.githubusercontent.com/123552037/233049896-9b7438ce-18df-4f7b-bce0-637dd9b72afc.png)
