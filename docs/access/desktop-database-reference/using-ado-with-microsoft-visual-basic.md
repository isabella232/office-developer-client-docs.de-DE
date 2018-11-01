---
title: Verwenden von ADO mit Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8644bd4f5b1a19848689adf92dca91ba30f324c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889847"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="cd02e-102">Verwenden von ADO mit Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cd02e-102">Using ADO with Microsoft Visual Basic</span></span>


<span data-ttu-id="cd02e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd02e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd02e-p101">Das Einrichten eines ADO-Projekts und das Schreiben von ADO-Code verläuft bei Verwendung von Visual Basic und Visual Basic für Applikationen ähnlich. In diesem Thema wird die Verwendung von ADO mit Visual Basic und mit Visual Basic für Applikationen behandelt, und etwaige Unterschiede werden genannt.</span><span class="sxs-lookup"><span data-stu-id="cd02e-p101">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications. This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="cd02e-106">Verweisen auf die ADO-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd02e-106">Referencing the ADO Library</span></span>

<span data-ttu-id="cd02e-107">Durch das Projekt muss auf die ADO-Bibliothek verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="cd02e-107">The ADO library must be referenced by your project.</span></span>

<span data-ttu-id="cd02e-108">**So verweisen Sie aus Microsoft Visual Basic auf ADO**</span><span class="sxs-lookup"><span data-stu-id="cd02e-108">**To reference ADO from Microsoft Visual Basic**</span></span>

1.  <span data-ttu-id="cd02e-109">Wählen Sie in Visual Basic im Menü **Projekt** die Option **Verweise** aus.</span><span class="sxs-lookup"><span data-stu-id="cd02e-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2.  <span data-ttu-id="cd02e-p102">Wählen Sie **Microsoft ActiveX Data Objects x.x Library** aus der Liste aus. Überprüfen Sie, ob mindestens die folgenden Bibliotheken ebenfalls ausgewählt sind:</span><span class="sxs-lookup"><span data-stu-id="cd02e-p102">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="cd02e-112">Visual Basic für Applikationen</span><span class="sxs-lookup"><span data-stu-id="cd02e-112">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="cd02e-113">Visual Basic-Laufzeitobjekte und -Prozeduren</span><span class="sxs-lookup"><span data-stu-id="cd02e-113">Visual Basic runtime objects and procedures</span></span>
    
    - <span data-ttu-id="cd02e-114">Visual Basic-Objekte und -Prozeduren</span><span class="sxs-lookup"><span data-stu-id="cd02e-114">Visual Basic objects and procedures</span></span>
    
    - <span data-ttu-id="cd02e-115">OLE-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="cd02e-115">OLE Automation</span></span>

3.  <span data-ttu-id="cd02e-116">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd02e-116">Click **OK**.</span></span>

<span data-ttu-id="cd02e-117">Sie können ADO genauso problemlos mit Visual Basic für Applikationen verwenden, z. B. mit Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cd02e-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

<span data-ttu-id="cd02e-118">**So verweisen Sie aus Microsoft Access auf ADO**</span><span class="sxs-lookup"><span data-stu-id="cd02e-118">**To reference ADO from Microsoft Access**</span></span>

1.  <span data-ttu-id="cd02e-119">Wählen Sie in Microsoft Access ein Modul auf der Registerkarte **Module** im Fenster **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="cd02e-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2.  <span data-ttu-id="cd02e-120">Wählen Sie im Menü **Extras** die Option **Verweise** aus.</span><span class="sxs-lookup"><span data-stu-id="cd02e-120">From the **Tools** menu, select **References...**.</span></span>

3.  <span data-ttu-id="cd02e-p103">Wählen Sie **Microsoft ActiveX Data Objects x.x Library** aus der Liste aus. Überprüfen Sie, ob mindestens die folgenden Bibliotheken ebenfalls ausgewählt sind:</span><span class="sxs-lookup"><span data-stu-id="cd02e-p103">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="cd02e-123">Visual Basic für Applikationen</span><span class="sxs-lookup"><span data-stu-id="cd02e-123">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="cd02e-124">Microsoft Access 11.0-Objektbibliothek (oder höher)</span><span class="sxs-lookup"><span data-stu-id="cd02e-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4.  <span data-ttu-id="cd02e-125">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd02e-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="cd02e-126">Erstellen von ADO-Objekten in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cd02e-126">Creating ADO Objects in Visual Basic</span></span>

<span data-ttu-id="cd02e-127">Zum Erstellen einer Automatisierungsvariablen und einer Instanz eines Objekts für diese Variable können Sie zwei Methoden verwenden: **Dim** oder **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="cd02e-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

## <a name="dim"></a><span data-ttu-id="cd02e-128">Dim</span><span class="sxs-lookup"><span data-stu-id="cd02e-128">Dim</span></span>

<span data-ttu-id="cd02e-129">Sie können das **New** -Schlüsselwort mit **Dim** zum Deklarieren und Instanziieren von ADO-Objekten in einem einzigem Schritt verwenden:</span><span class="sxs-lookup"><span data-stu-id="cd02e-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="cd02e-130">Alternativ können die **Dim** -Anweisungsdeklaration und die Objektinstanziierung in zwei Schritten erfolgen:</span><span class="sxs-lookup"><span data-stu-id="cd02e-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P><span data-ttu-id="cd02e-131">Es ist nicht erforderlich, das progid ADODB explizit zu verwenden, mit der <STRONG>Dim</STRONG> -Anweisung, vorausgesetzt, dass Sie ordnungsgemäß auf die ADO-Bibliothek in Ihrem Projekt verwiesen haben.</span><span class="sxs-lookup"><span data-stu-id="cd02e-131">It is not required to explicitly use the ADODB progid with the <STRONG>Dim</STRONG> statement, assuming you have properly referenced the ADO library in your project.</span></span> <span data-ttu-id="cd02e-132">Ihre Verwendung stellt jedoch sicher, dass keine Namenskonflikte mit anderen Bibliotheken auftreten.</span><span class="sxs-lookup"><span data-stu-id="cd02e-132">However, using it ensures that you won't have naming conflicts with other libraries.</span></span></P>



<span data-ttu-id="cd02e-133">Wenn Sie z. B. im gleichen Projekt Verweise auf ADO und auf DAO einschließen, schließen Sie wie im folgenden Code einen Qualifizierer ein, um anzugeben, welches Objektmodell beim Instanziieren von **Recordset** -Objekten verwendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="cd02e-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
<span data-ttu-id="cd02e-134">Dim AdoRS als ADODB. Recordset-Objekt</span><span class="sxs-lookup"><span data-stu-id="cd02e-134">Dim adoRS As ADODB.Recordset</span></span>  
  
<span data-ttu-id="cd02e-135">Dim DaoRS als DAO. Recordset-Objekt</span><span class="sxs-lookup"><span data-stu-id="cd02e-135">Dim daoRS As DAO.Recordset</span></span>

## <a name="createobject"></a><span data-ttu-id="cd02e-136">CreateObject</span><span class="sxs-lookup"><span data-stu-id="cd02e-136">CreateObject</span></span>

<span data-ttu-id="cd02e-137">Bei der **CreateObject** -Methode müssen Deklaration und Objektinstanziierung in zwei getrennten Schritten erfolgen:</span><span class="sxs-lookup"><span data-stu-id="cd02e-137">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="cd02e-p105">Mit **CreateObject** instanziierte Objekte sind spät gebunden, d. h., sie sind nicht stark typisiert, und die Vervollständigung von Befehlszeilen ist deaktiviert. Sie können jedoch die Verweise auf die ADO-Bibliothek aus dem Projekt überspringen und bestimmte Versionen von Objekten instanziieren. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cd02e-p105">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled. However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects. For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="cd02e-141">Sie können dies auch erreichen, indem Sie ausdrücklich einen Verweis auf die Typbibliothek von ADO, Version 2.0, erstellen und das Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd02e-141">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="cd02e-142">Das Instanziieren von Objekten mit der **CreateObject** -Methode ist normalerweise langsamer als die Verwendung der **Dim** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="cd02e-142">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="cd02e-143">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="cd02e-143">Handling Events</span></span>

<span data-ttu-id="cd02e-p106">Zum Behandeln von ADO-Ereignissen in Microsoft Visual Basic müssen Sie eine Variable auf Modulebene mithilfe des **WithEvents** -Schlüsselworts deklarieren. Die Variable kann nur als Teil eines Klassenmoduls deklariert werden und muss auf Modulebene deklariert werden. Eine umfassendere Erörterung der Behandlung von ADO-Ereignissen finden Sie unter [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="cd02e-p106">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="cd02e-147">Visual Basic (Beispiele)</span><span class="sxs-lookup"><span data-stu-id="cd02e-147">Visual Basic Examples</span></span>

<span data-ttu-id="cd02e-148">In der ADO-Dokumentation sind viele Visual Basic-Beispiele enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd02e-148">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="cd02e-149">Weitere Informationen finden Sie unter [ADO-Codebeispiele in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="cd02e-149">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

