---
<span data-ttu-id="a6194-101"><<<<<<< HEAD-Titel: Zugreifen auf Zeilen in einem hierarchischen Recordset TOCTitle: Zugreifen auf Zeilen in einem hierarchischen Recordset Ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) Ms:contentKeyID: 48548104 ms.date: 09/18 / 2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="a6194-101"><<<<<<< HEAD title: Accessing Rows in a Hierarchical Recordset TOCTitle: Accessing Rows in a Hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="a6194-102">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="a6194-102">Accessing Rows in a Hierarchical Recordset</span></span>

<span data-ttu-id="a6194-103">=== Titel: Zugreifen auf Zeilen in einem hierarchischen Recordset TOCTitle: Zugreifen auf Zeilen in einem hierarchischen Recordset Ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) Ms:contentKeyID: 48548104 ms.date: 10/17/2018 Mtps_version: V = Office.15</span><span class="sxs-lookup"><span data-stu-id="a6194-103">======= title: Accessing rows in a hierarchical Recordset TOCTitle: Accessing rows in a hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="a6194-104">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="a6194-104">Accessing rows in a hierarchical Recordset</span></span>
>>>>>>> <span data-ttu-id="a6194-105">master</span><span class="sxs-lookup"><span data-stu-id="a6194-105">master</span></span>

<span data-ttu-id="a6194-106">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6194-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6194-107">Das folgende Beispiel zeigt die notwendigen Schritte zum Zugreifen auf Zeilen in einem hierarchischen [Recordset](recordset-object-ado.md):</span><span class="sxs-lookup"><span data-stu-id="a6194-107">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

<span data-ttu-id="a6194-108"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="a6194-108"><<<<<<< HEAD</span></span>
1.  <span data-ttu-id="a6194-109">Recordset-Objekte aus den Tabellen authors und titleauthor werden nach Autor-Nr. miteinander in Beziehung gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a6194-109">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="a6194-110">In der äußeren Schleife werden der Vor- und Nachname, der Status und die Identifikation jedes Autors angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6194-110">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="a6194-111">Das angefügte **Recordset** für jede Zeile wird aus der **Fields**-Auflistung abgerufen und *rstTitleAuthor* zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a6194-111">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="a6194-112">In der inneren Schleife werden vier Felder aus jeder Zeile im angefügten **Recordset** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6194-112">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a><span data-ttu-id="a6194-113">(Die [StayInSync](stayinsync-property-ado.md)-Eigenschaft wird zu Veranschaulichungszwecken auf FALSE festgelegt - so können Sie die Kapiteländerung in den einzelnen Iterationen der äußeren Schleife explizit sehen.</span><span class="sxs-lookup"><span data-stu-id="a6194-113">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="a6194-114">Das Beispiel ist jedoch effizienter, wenn die Zuweisung in Schritt 3 vor die erste Zeile in Schritt 2 verschoben wird, sodass die Zuweisung nur ein Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6194-114">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="a6194-115">Klicken Sie dann die **StayInSync** -Eigenschaft auf TRUE festgelegt, sodass *RstTitleAuthor* implizit und automatisch in das entsprechende Kapitel geändert wird, wenn *Rst* an eine neue Zeile verschoben wird.)</span><span class="sxs-lookup"><span data-stu-id="a6194-115">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>
=======
1. <span data-ttu-id="a6194-116">Recordset-Objekte aus den Tabellen authors und titleauthor werden nach Autor-Nr. miteinander in Beziehung gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a6194-116">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="a6194-117">In der äußeren Schleife werden der Vor- und Nachname, der Status und die Identifikation jedes Autors angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6194-117">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="a6194-118">Das angefügte **Recordset** für jede Zeile wird aus der **Fields**-Auflistung abgerufen und *rstTitleAuthor* zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a6194-118">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="a6194-119">In der inneren Schleife werden vier Felder aus jeder Zeile im angefügten **Recordset** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6194-119">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="a6194-120">[StayInSync](stayinsync-property-ado.md) -Eigenschaft wird zur Veranschaulichung, auf FALSE festgelegt, damit Sie sehen können, das Kapitel in jeder Iteration der äußeren Schleife explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="a6194-120">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="a6194-121">Das Beispiel ist jedoch effizienter, wenn die Zuweisung in Schritt 3 vor die erste Zeile in Schritt 2 verschoben wird, sodass die Zuweisung nur ein Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6194-121">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="a6194-122">**StayInSync** -Eigenschaft auf TRUE festgelegt, sodass *RstTitleAuthor* implizit und automatisch in das entsprechende Kapitel geändert wird, wenn *Rst* an eine neue Zeile verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a6194-122">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>
>>>>>>> <span data-ttu-id="a6194-123">master</span><span class="sxs-lookup"><span data-stu-id="a6194-123">master</span></span>

<span data-ttu-id="a6194-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a6194-124">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

