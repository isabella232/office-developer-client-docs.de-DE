---
<span data-ttu-id="322c3-101"><<<<<<< HEAD-Titel: Count-Eigenschaft Beispiel) (VJ++) TOCTitle: Count-Eigenschaft Beispiel) (VJ++) === Titel: Count-Eigenschaft Beispiel) (VJ++) TOCTitle: Count-Eigenschaft Beispiel) (VJ++)</span><span class="sxs-lookup"><span data-stu-id="322c3-101"><<<<<<< HEAD title: Count Property Example (VJ++) TOCTitle: Count Property Example (VJ++) ======= title: Count property example (VJ++) TOCTitle: Count property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="322c3-102">Master Ms:assetid: 749de00a-7530-ea04-558c-34277c4d2f61 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249478(v=office.15) Ms:contentKeyID: 48545666 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="322c3-102">master ms:assetid: 749de00a-7530-ea04-558c-34277c4d2f61 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249478(v=office.15) ms:contentKeyID: 48545666 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="322c3-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="322c3-103"><<<<<<< HEAD</span></span>
# <a name="count-property-example-vj"></a><span data-ttu-id="322c3-104">Count Property Example (VJ++)</span><span class="sxs-lookup"><span data-stu-id="322c3-104">Count Property Example (VJ++)</span></span>
=======
# <a name="count-property-example-vj"></a><span data-ttu-id="322c3-105">Count-Eigenschaft Beispiel) (VJ++)</span><span class="sxs-lookup"><span data-stu-id="322c3-105">Count property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="322c3-106">master</span><span class="sxs-lookup"><span data-stu-id="322c3-106">master</span></span>


<span data-ttu-id="322c3-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="322c3-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="322c3-108">Dieses Beispiel veranschaulicht die [Count](count-property-ado.md) -Eigenschaft mit zwei Sammlungen in der ***Employees*** -Datenbank.</span><span class="sxs-lookup"><span data-stu-id="322c3-108">This example demonstrates the [Count](count-property-ado.md) property with two collections in the ***Employees*** database.</span></span> <span data-ttu-id="322c3-109">Die Eigenschaft ruft die Anzahl der Objekte in der Auflistung ab und legt den oberen Grenzwert für Schleifen, die diese Auflistungen aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="322c3-109">The property obtains the number of objects in each collection, and sets the upper limit for loops that enumerate these collections.</span></span> <span data-ttu-id="322c3-110">Eine andere Möglichkeit, diese Auflistungen aufgezählt werden ohne Verwendung der **Count** -Eigenschaft wäre Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="322c3-110">Another way to enumerate these collections without using the **Count** property would be to use statements.</span></span>

```java 
 
// BeginCountJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class CountX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 CountX(); 
 System.exit(0); 
 } 
 
 // CountX function 
 
 static void CountX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstEmployees = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 int intLoop; 
 int intDisplaySize = 20; 
 int recCount=0; 
 
 try 
 { 
 rstEmployees = new Recordset(); 
 
 // Open recordset with data from Employees table. 
 rstEmployees.open("employee", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Print information about Fields collection. 
 System.out.println(rstEmployees.getFields().getCount() + 
 " Fields in Employees"); 
 for ( intLoop = 0; intLoop < 
 rstEmployees.getFields().getCount(); intLoop++) 
 { 
 System.out.println("\t" + 
 rstEmployees.getFields().getItem(intLoop).getName()); 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Print information about Properties collection. 
 System.out.println(rstEmployees.getProperties().getCount() + 
 " Properties in Employees"); 
 for ( intLoop = 0; intLoop < 
 rstEmployees.getProperties().getCount(); intLoop++) 
 { 
 System.out.println("\t" + 
 rstEmployees.getProperties().getItem(intLoop).getName()); 
 recCount++; 
 if ( recCount >= intDisplaySize) 
 { 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 recCount = 0; 
 } 
 } 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if (rstEmployees.getActiveConnection()==null) 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 // As passing a Recordset, check for null pointer first. 
 if (rstEmployees != null) 
 { 
 PrintProviderError(rstEmployees.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
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
 if (rstEmployees != null) 
 if (rstEmployees.getState() == 1) 
 rstEmployees.close(); 
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
 
// EndCountJ 
```

