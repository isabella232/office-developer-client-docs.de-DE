---
<<<<<<< HEAD-Titel: optimieren-Eigenschaft Beispiel) (VJ++) TOCTitle: optimieren-Eigenschaft Beispiel) (VJ++) === Titel: Optimize-Eigenschaft-Beispiel) (VJ++) TOCTitle: Optimize-Eigenschaft-Beispiel) (VJ++)
>>>>>>> Master Ms:assetid: d4ac9ae3-3304-addf-0292-7af4ed4fdbc2 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250067(v=office.15) Ms:contentKeyID: 48547949 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="optimize-property-example-vj"></a>Optimize-Eigenschaft (Beispiel) (VJ++)
=======
# <a name="optimize-property-example-vj"></a>Optimize-Eigenschaft-Beispiel) (VJ++)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht die [Field](field-object-ado.md) -Objekt dynamische Optimize-Eigenschaft. Das ***Zip*** -Feld der ***Authors*** -Tabelle in der ***Pubs*** -Datenbank wird nicht indiziert. [Optimize](optimize-property-dynamic-ado.md) -Eigenschaft auf **True** festlegen, im Feld ***Zip*** autorisiert ADO einen Index zu erstellen, der die [Find](find-method-ado.md) -Methode die Leistung verbessert.

```java 
 
// BeginOptimizeJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class OptimizeX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 OptimizeX(); 
 System.exit(0); 
 } 
 
 // OptimizeX function 
 
 static void OptimizeX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 rstAuthors = new Recordset(); 
 rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 // Enable index creation. 
 rstAuthors.open("SELECT * FROM Authors", 
 strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 rstAuthors.getField("zip").getProperties(). 
 getItem("Optimize").setBoolean(true); // Create the index. 
 rstAuthors.find("zip = '94595'"); // Find Akiko Yokomoto. 
 System.out.println(rstAuthors.getField("au_fname").getString() + 
 " " + rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("address").getString() + " " + 
 rstAuthors.getField("city").getString() + " " + 
 rstAuthors.getField("state").getString() + " "); 
 rstAuthors.getField("zip").getProperties(). 
 getItem("Optimize").setBoolean(false); // Delete the index. 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndOptimizeJ 
```
