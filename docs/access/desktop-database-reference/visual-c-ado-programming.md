---
title: Visual C++-ADO-Programmierung
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7478a90e3c6242c68a1325b08e998f4c76a62f3d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944662"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="cae5e-102">Visual C++-ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="cae5e-102">Visual C++ ADO programming</span></span>


<span data-ttu-id="cae5e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cae5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cae5e-104">In der ADO-API-Referenz wird die Funktionalität der ADO-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit einer Microsoft Visual Basic ähnlichen Syntax beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cae5e-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="cae5e-105">Obwohl die Zielgruppe alle Benutzer sind, verwendet ADO-Programmierer verschiedene Sprachen wie Visual Basic, Visual C++ (mit und ohne die \*\* \#importieren\*\* Richtlinie), und Visual J++ (mit dem ADO/WFC-Klasse-Paket).</span><span class="sxs-lookup"><span data-stu-id="cae5e-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="cae5e-106">Um dieser Vielfalt gerecht zu werden, bieten die [ADO für Visual C++-Syntaxindizes](using-ado-with-microsoft-visual-c.md) eine Visual C++-sprachspezifische Syntax mit Verknüpfungen zu allgemeinen Beschreibungen der Funktionalität, der Parameter, außergewöhnlichen Verhaltensweisen usw. in der API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="cae5e-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="cae5e-p102">ADO wird mit COM-Schnittstellen (Component Object Model) implementiert. In bestimmten Programmiersprachen ist es jedoch einfacher für Programmierer mit COM zu arbeiten als in anderen. Beispielsweise werden nahezu alle Details der Verwendung von COM implizit für Visual Basic-Programmierer behandelt, wohingegen Visual C++-Programmierer die Details selbst ermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="cae5e-110">In den folgenden Abschnitten werden Details für C und C++-Programmierer verwenden von ADO zusammengefasst und die \*\* \#importieren\*\* Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="cae5e-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="cae5e-111">Der Schwerpunkt liegt auf den speziellen Datentypen für COM (**Variant**, **BSTR**und **SafeArray**) und Fehlerbehandlung (\_com\_Fehler).</span><span class="sxs-lookup"><span data-stu-id="cae5e-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="cae5e-112">Mithilfe der \#-Compilerdirektive importieren</span><span class="sxs-lookup"><span data-stu-id="cae5e-112">Using the \#import Compiler Directive</span></span>

<span data-ttu-id="cae5e-113">Die \*\* \#importieren\*\* Visual C++-Compilerdirektive vereinfacht die Arbeit mit der ADO-Methoden und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cae5e-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="cae5e-114">Die Richtlinie akzeptiert den Namen einer Datei mit einer Typbibliothek, wie der ADO-DLL (Msado15.dll), und generiert Headerdateien mit Typedef-Deklarationen, intelligente Zeiger für Schnittstellen und aufgezählte Konstanten.</span><span class="sxs-lookup"><span data-stu-id="cae5e-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="cae5e-115">Jede Schnittstelle ist gekapselte oder eingebunden, in einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="cae5e-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="cae5e-p105">Für jeden Vorgang in einer Klasse (also ein Methoden- oder Eigenschaftenaufruf) gibt es eine Deklaration, um den Vorgang direkt aufzurufen (also die "Rohform" des Vorgangs), und eine Deklaration, um den Rohvorgang aufzurufen und einen COM-Fehler auszulösen, wenn der Vorgang nicht erfolgreich ausgeführt wird. Wenn es sich bei dem Vorgang um eine Eigenschaft handelt, wird normalerweise mit einer Compilerdirektive eine alternative Syntax für den Vorgang erstellt, die der Syntax von Visual Basic ähnelt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="cae5e-118">Vorgänge, die den Wert einer Eigenschaft abzurufen, weisen Namen des Formulars, \**Abrufen \*\*\* Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="cae5e-119">Vorgänge, die den Wert einer Eigenschaft festgelegt haben Namen des Formulars, \**platzieren \*\*\* Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="cae5e-120">Vorgänge, die den Wert einer Eigenschaft mit einem Zeiger auf ein ADO-Objekt festgelegt haben Namen des Formulars, \**PutRef \*\*\* Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="cae5e-121">Sie können eine Eigenschaft mit Aufrufen in der folgenden Form abrufen oder festlegen:</span><span class="sxs-lookup"><span data-stu-id="cae5e-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="cae5e-122">Verwenden von Eigenschaftendirektiven</span><span class="sxs-lookup"><span data-stu-id="cae5e-122">Using Property Directives</span></span>

<span data-ttu-id="cae5e-123">Die \*\* \_ \_declspec(property...)\*\* -Compilerdirektive ist eine Erweiterung der Microsoft-spezifischen C-Sprache, die eine Funktion, die als eine Eigenschaft verwendet, um eine alternative Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="cae5e-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="cae5e-124">Daher können Sie festlegen oder Abrufen von Werten einer Eigenschaft so ähnlich zu Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cae5e-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="cae5e-125">Beispielsweise können Sie festlegen und Abrufen eine Eigenschaft auf diese Weise:</span><span class="sxs-lookup"><span data-stu-id="cae5e-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="cae5e-126">Der Code muss nicht wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="cae5e-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="cae5e-127">Der Compiler generiert den entsprechenden \*\*Get \*\**-*, **Put**-, oder \**PutRef \*\*\* Eigenschaft* Anruf basierend auf welche alternative Syntax deklariert ist, und gibt an, ob die Eigenschaft wird gelesenen oder geschriebenen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="cae5e-128">Die \*\* \_ \_declspec(property...)\*\* -Compilerdirektive kann nur **get**, **put**oder **get** und **put** alternative Syntax für eine Funktion deklarieren.</span><span class="sxs-lookup"><span data-stu-id="cae5e-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="cae5e-129">Schreibgeschützte Vorgänge weisen lediglich eine Erklärung **erhalten möchten** . lesegeschützte Vorgänge weisen lediglich eine Erklärung **zu platzieren** . Vorgänge, die Lese- und Schreibvorgang sind verfügen sowohl **get** und **put** -Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="cae5e-130">Es sind nur zwei Deklarationen mit dieser Richtlinie möglich. Jede Eigenschaft kann jedoch drei Eigenschaftenfunktionen haben: \**Abrufen \*\*\* Eigenschaft*, \**zu platzieren \*\*\* Eigenschaft*, und \**PutRef \*\*\* Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="cae5e-131">In diesem Fall weisen nur zwei Formen der Eigenschaft die alternative Syntax.</span><span class="sxs-lookup"><span data-stu-id="cae5e-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="cae5e-132">Beispielsweise wird der **ActiveConnection** -Eigenschaft für das **Command** -Objekt mit einer alternativen Syntax für deklariert \**Abrufen \*\*\* ActiveConnection* und \**PutRef \*\*\* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="cae5e-133">Die **PutRef**- Syntax ist eine gute Wahl, da in der Praxis Sie in der Regel werden ein geöffnetes **Connection** -Objekt (d. h., ein **Connection** -Objektzeiger) in dieser Eigenschaft aufnehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="cae5e-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="cae5e-134">Andererseits, hat das **Recordset** -Objekt **Abrufen**-, **Put**-, und \**PutRef \*\*\* ActiveConnection* Vorgänge, aber keine alternative Syntax.</span><span class="sxs-lookup"><span data-stu-id="cae5e-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="cae5e-135">Auflistungen, GetItem-Methode und Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cae5e-135">Collections, the GetItem Method, and the Item Property</span></span>

<span data-ttu-id="cae5e-p111">ADO definiert mehrere Auflistungen, einschließlich **Fields**, **Parameters**, **Properties** und **Errors**. In Visual C++ gibt die **GetItem(***index***)**-Methode ein Member der Auflistung zurück. *Index* ist ein **Variant**-Wert, der eigentliche Wert ist ein numerischer Index des Members in der Auflistung oder eine Zeichenfolge mit dem Namen des Members.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p111">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**. In Visual C++, the **GetItem(***index***)** method returns a member of the collection. *Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="cae5e-139">Die \*\* \_ \_declspec(property...)\*\* -Compilerdirektive deklariert die **Item** -Eigenschaft als eine alternative Syntax für jede Auflistung grundlegende **'GetItem()'** -Methode.</span><span class="sxs-lookup"><span data-stu-id="cae5e-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="cae5e-140">Für die alternative Syntax werden eckige Klammern verwendet, und sie ähnelt einem Arrayverweis.</span><span class="sxs-lookup"><span data-stu-id="cae5e-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="cae5e-141">Im Allgemeinen sehen die beiden Formen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="cae5e-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="cae5e-142">Ein Feld eines **Recordset** -Objekts, mit dem Namen ***Rs***, abgeleitet aus der **Authors** -Tabelle der **Pubs** -Datenbank beispielsweise weisen Sie einen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="cae5e-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="cae5e-143">Verwenden Sie die Eigenschaft **Item()** Zugriff auf das dritte **Feld** der **Fields** -Auflistung des **Recordset** -Objekts (Sammlungen von 0 indiziert werden, sofern das dritte Feld den Namen ***au\_Fname***).</span><span class="sxs-lookup"><span data-stu-id="cae5e-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="cae5e-144">Rufen Sie dann die **Value()** -Methode für das **Field** -Objekt einen String-Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="cae5e-145">Dies kann in Visual Basic auf die folgenden vier Arten ausgedrückt werden (die beiden letzten Formen gelten nur für Visual Basic, in anderen Sprachen gibt es keine Entsprechungen):</span><span class="sxs-lookup"><span data-stu-id="cae5e-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="cae5e-146">Die Entsprechung in Visual C++ zu den ersten beiden Formen lautet:</span><span class="sxs-lookup"><span data-stu-id="cae5e-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="cae5e-147">\-oder -(die alternative Syntax für die **Value** -Eigenschaft wird ebenfalls dargestellt)</span><span class="sxs-lookup"><span data-stu-id="cae5e-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="cae5e-148">COM-spezifische Datentypen</span><span class="sxs-lookup"><span data-stu-id="cae5e-148">COM-Specific Data Types</span></span>

<span data-ttu-id="cae5e-p114">Im Allgemeinen weisen alle Visual Basic-Datentypen, die Sie in der ADO-API-Referenz finden, eine Visual C++-Entsprechung auf. Dazu gehören Standarddatentypen wie **unsigned char** für **Byte** in Visual Basic, **short** für **Integer** und **long** für **Long**. Mithilfe der Syntaxindizes können Sie genau feststellen, was für die Operanden einer bestimmten Methode oder Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="cae5e-152">Ausnahmen zu dieser Regel bilden die Datentypen, die nur für COM gelten: **Variant**, **BSTR** und **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="cae5e-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

## <a name="variant"></a><span data-ttu-id="cae5e-153">Variant</span><span class="sxs-lookup"><span data-stu-id="cae5e-153">Variant</span></span>

<span data-ttu-id="cae5e-p115">Variant ist ein strukturierter Datentyp, der ein Wertmember und ein Datentypmember enthält. Ein Variant-Wert kann eine Vielzahl anderen Datentypen enthalten, u. a. einen anderen Variant-Wert, einen BSTR- oder Boolean-Wert, einen IDispatch- oder IUnknown-Zeiger, eine Währung und ein Datum. COM bietet außerdem Methoden, die die Konvertierung von Datentypen vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="cae5e-157">Die \*\* \_Variant\_t\*\* -Klasse kapselt und verwaltet den **Variant** -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cae5e-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="cae5e-158">Wenn der ADO-API-Referenz besagt, eine Methode dass oder Operanden Eigenschaft einen Wert übernimmt, sie in der Regel bedeutet, dass übergebene Wert ist eine \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="cae5e-159">Diese Regel ist explizit True, wenn der ADO-API-Referenz in den Themen im Abschnitt **Parameter** besagt, einen Operand dass **Variant**.</span><span class="sxs-lookup"><span data-stu-id="cae5e-159">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**.</span></span> <span data-ttu-id="cae5e-160">Eine Ausnahme ist, wenn die Dokumentation ausdrücklich darauf hinweist, dass der Operand einen standard-Datentyp, wie **lange** oder **Byte**oder eine Enumeration übernimmt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-160">One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration.</span></span> <span data-ttu-id="cae5e-161">Eine weitere Ausnahme ist, wenn der Operand eine **Zeichenfolge**akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="cae5e-161">Another exception is when the operand takes a **String**.</span></span>

## <a name="bstr"></a><span data-ttu-id="cae5e-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="cae5e-162">BSTR</span></span>

<span data-ttu-id="cae5e-p117">**BSTR** (**B**asic **STR**ing) ist ein strukturierter Datentyp, der eine Zeichenfolge und die Länge der Zeichenfolge enthält. COM bietet Methoden zum Zuordnen, Ändern und Freigeben eines **BSTR**-Werts.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="cae5e-165">Die \*\* \_Bstr\_t\*\* -Klasse kapselt und verwaltet den **BSTR** -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cae5e-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="cae5e-166">Wenn der ADO-API-Referenz besagt, eine Methode dass oder Eigenschaft einen **String** -Wert übernimmt, bedeutet der Wert wird in Form von einer \*\* \_Bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

## <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="cae5e-167">Umwandeln von \_Variant\_t und \_Bstr\_t-Klassen</span><span class="sxs-lookup"><span data-stu-id="cae5e-167">Casting \_variant\_t and \_bstr\_t Classes</span></span>

<span data-ttu-id="cae5e-168">Häufig ist es nicht erforderlich, explizit Code eine \*\* \_Variant\_t\*\* oder \*\* \_Bstr\_t\*\* als Argument für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cae5e-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="cae5e-169">Wenn die \*\* \_Variant\_t\*\* oder \*\* \_Bstr\_t\*\* Klasse hat einen Konstruktor, der den Datentyp des Arguments entspricht, und klicken Sie dann der Compiler generiert den entsprechenden \*\* \_Variant\_t\*\* oder \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="cae5e-170">Wenn das Argument jedoch nicht eindeutig ist, wenn also der Datentyp des Arguments mit mehr als einem Konstruktor übereinstimmt, müssen Sie das Argument mit dem entsprechenden Datentyp umwandeln, um den richtigen Konstruktor aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="cae5e-171">Beispielsweise lautet die Deklaration für die **Recordset::Open** -Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cae5e-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="cae5e-172">Das ActiveConnection-Argument übernimmt einen Verweis auf ein \*\* \_Variant\_t\*\*, den Sie als Verbindungszeichenfolge oder als Zeiger auf ein geöffnetes **Connection** -Objekt codieren können.</span><span class="sxs-lookup"><span data-stu-id="cae5e-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="cae5e-173">Die richtige \*\* \_Variant\_t\*\* wird implizit konstruiert, wenn Sie eine Zeichenfolge, z. B. übergeben "DSN = Pubs; Uid = sa; Pwd =;", oder einen Zeiger wie "(IDispatch \*) pConn".</span><span class="sxs-lookup"><span data-stu-id="cae5e-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="cae5e-174">Oder Sie können explizit code eine \*\* \_Variant\_t\*\* mit einem Zeiger wie "\_Variant-Wert\_t ((IDispatch \*) pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="cae5e-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="cae5e-175">Die Cast (IDispatch \*), wird die Mehrdeutigkeit mit einem anderen Konstruktor, der einen Zeiger auf eine IUnknown-Schnittstelle akzeptiert aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="cae5e-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="cae5e-p120">Eine wichtige, aber selten erwähnte Tatsache ist, dass ADO eine IDispatch-Schnittstelle ist. Wenn ein Zeiger auf ein ADO-Objekt als ein Variant-Wert übergeben werden muss, muss dieser Zeiger als ein Zeiger auf eine IDispatch-Schnittstelle umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="cae5e-178">Im letzte Fall codes explizit das zweite boolesche Argument des Konstruktors mit dem optional, Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="cae5e-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="cae5e-179">Dieses Argument wird vom **Variant** Konstruktor rufen Sie die **AddRef**-Methode () dafür, dass von ADO automatisch die \*\* \_Variant\_t::Release\*\*()-Methode, wenn der ADO-Methode oder Eigenschaft Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cae5e-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

## <a name="safearray"></a><span data-ttu-id="cae5e-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="cae5e-180">SafeArray</span></span>

<span data-ttu-id="cae5e-181">**SafeArray** ist ein strukturierter Datentyp, der ein Array anderer Datentypen enthält.</span><span class="sxs-lookup"><span data-stu-id="cae5e-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="cae5e-182">**SafeArray** ist *sicherer* bezeichnet, da sie Informationen zu den Grenzen der einzelnen Arraydimension und schränkt den Zugriff auf Elemente innerhalb dieser Grenzen Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="cae5e-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="cae5e-183">Wenn in der ADO-API-Referenz angegeben ist, dass eine Methode oder Eigenschaft ein Array übernimmt oder zurückgibt, bedeutet dies, dass die Methode oder Eigenschaft einen **SafeArray** -Wert übernimmt oder zurückgibt, kein systemeigenes C/C++-Array.</span><span class="sxs-lookup"><span data-stu-id="cae5e-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="cae5e-p123">Für den zweiten Parameter der **OpenSchema** -Methode des **Connection** -Objekts ist z. B. ein Array von **Variant** -Werten erforderlich. Diese **Variant** -Werte müssen als Elemente eines **SafeArray** -Werts übergeben werden, und dieser **SafeArray** -Wert muss als Wert eines anderen **Variant** -Werts festgelegt werden. Dieser andere **Variant** -Wert wird als zweites Argument von **OpenSchema** übergeben.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="cae5e-187">Als weiteres Beispiel ist das erste Argument der **Find** -Methode ein **Variant** -Wert, dessen Wert ein eindimensionaler **SafeArray** -Wert ist. Jedes optionale erste und zweite Argument von **AddNew** ist ein eindimensionaler **SafeArray** -Wert, und der Rückgabewert der **GetRows** -Methode ist ein **Variant** -Wert, dessen Wert ein zweidimensionaler **SafeArray** -Wert ist.</span><span class="sxs-lookup"><span data-stu-id="cae5e-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="cae5e-188">Fehlende und Standardparameter</span><span class="sxs-lookup"><span data-stu-id="cae5e-188">Missing and Default Parameters</span></span>

<span data-ttu-id="cae5e-p124">Bei Visual Basic sind fehlende Parameter in Methoden zulässig. Die **Open** -Methode des **Recordset** -Objekts weist z. B. fünf Parameter auf, aber Sie können Zwischenparameter überspringen und nachstehende Parameter auslassen. Ein standardmäßiger **BSTR** - oder **Variant** -Wert wird je nach Datentyp des fehlenden Operanden ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="cae5e-192">In der C/C++ müssen alle Operanden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cae5e-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="cae5e-193">Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp eine Zeichenfolge ist, geben Sie eine \*\* \_Bstr\_t\*\* mit einer leeren Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cae5e-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="cae5e-194">Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp **Variant-Wert**ist, geben Sie eine \*\* \_Variant\_t\*\* mit einem Wert von Verschiebung\_E\_PARAMNOTFOUND und einen Typ von VT\_Fehler.</span><span class="sxs-lookup"><span data-stu-id="cae5e-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="cae5e-195">Alternativ angeben die Entsprechung \*\* \_Variant\_t\*\* -Konstante, **VtMissing**, das von bereitgestellt wird die \*\* \#importieren\*\* Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="cae5e-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="cae5e-p126">Drei Methoden bilden Ausnahmen zur üblichen Verwendung von **vtMissing**. Dies sind die **Execute** -Methoden der Objekte **Connection** - und **Command** -Objekte sowie die **NextRecordset** -Methode des **Recordset** -Objekts. Im Folgenden sind deren Signaturen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cae5e-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="cae5e-p127">Die Parameter *RecordsAffected* und *Parameters* sind Zeiger auf einen **Variant**-Wert. *Parameters* ist ein Eingabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, der einen Parameter oder ein Array von Parametern enthält, der bzw. das den ausgeführten Befehl ändert. *RecordsAffected* ist ein Ausgabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, an den die Anzahl der von der Methode betroffenen Zeilen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="cae5e-202">Geben Sie in das **Command** -Objekt **Execute** -Methode an, dass keine Parameter angegeben werden, indem Sie *Parameter* entweder \&VtMissing (was empfohlen wird) oder auf einen null-Zeiger (d. h., **NULL** oder 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="cae5e-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="cae5e-203">Wenn der *Parameter* auf null-Zeiger festgelegt ist, wird die Methode intern ersetzt das Äquivalent von **VtMissing**und schließt dann den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cae5e-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="cae5e-204">Geben Sie in den Methoden an, dass die Anzahl der betroffenen Datensätze nicht zurückgegeben werden soll, indem Sie *RecordsAffected* auf null-Zeiger festlegen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="cae5e-205">In diesem Fall ist der NULL-Zeiger kein fehlender Parameter, sondern ein Kennzeichen dafür, dass die Methode die Anzahl betroffener Datensätze verwerfen soll.</span><span class="sxs-lookup"><span data-stu-id="cae5e-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="cae5e-206">Deshalb können Sie für diese drei Methoden z. B. folgenden Code schreiben:</span><span class="sxs-lookup"><span data-stu-id="cae5e-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="cae5e-207">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="cae5e-207">Error Handling</span></span>

<span data-ttu-id="cae5e-208">In COM geben die meisten Vorgänge einen HRESULT-Rückgabecode, der angibt, ob eine Funktion erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="cae5e-209">Die \*\* \#importieren\*\* Richtlinie generiert Wrappercode um jede "unformatierte" Methode oder Eigenschaft und überprüft den zurückgegebenen HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cae5e-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="cae5e-210">Wenn das HRESULT einen Fehler angibt, löst der Code einen COM-Fehler durch Aufrufen von \_com\_Problem\_errorex() mit dem HRESULT-Rückgabecode als Argument.</span><span class="sxs-lookup"><span data-stu-id="cae5e-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="cae5e-211">Com-Error-Objekte abgefangen werden können, **versuchen Sie es**-**catch** -Block.</span><span class="sxs-lookup"><span data-stu-id="cae5e-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="cae5e-212">(Aus Gründen der Effizienz catch einen Verweis auf ein \*\* \_com\_Fehler\*\* -Objekt.)</span><span class="sxs-lookup"><span data-stu-id="cae5e-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="cae5e-p131">Bedenken Sie, dass es sich dabei um ADO-Fehler handelt: Sie resultieren daraus, dass der ADO-Vorgang fehlschlägt. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="cae5e-215">Die \*\* \#importieren\*\* Richtlinie erstellt nur Fehler dadurch für Methoden und Eigenschaften, die in der ADO-DLL deklariert.</span><span class="sxs-lookup"><span data-stu-id="cae5e-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="cae5e-216">Sie können jedoch den gleichen Mechanismus für die Fehlerbehandlung nutzen, indem Sie ein eigenes Makro oder eine Inlinefunktion für die Fehlerüberprüfung schreiben.</span><span class="sxs-lookup"><span data-stu-id="cae5e-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="cae5e-217">Beispiele finden Sie im Thema [Visual C++-Erweiterungen](visual-c-extensions-for-ado.md) oder im Code in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="cae5e-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="cae5e-218">Visual C++-Entsprechungen für Visual Basic-Konventionen</span><span class="sxs-lookup"><span data-stu-id="cae5e-218">Visual C++ Equivalents of Visual Basic Conventions</span></span>

<span data-ttu-id="cae5e-219">Im Folgenden finden Sie eine Zusammenfassung verschiedener Konventionen in der ADO-Dokumentation, codiert in Visual Basic, sowie deren Entsprechungen in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="cae5e-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

## <a name="declaring-an-ado-object"></a><span data-ttu-id="cae5e-220">Deklarieren eines ADO-Objekts</span><span class="sxs-lookup"><span data-stu-id="cae5e-220">Declaring an ADO Object</span></span>

<span data-ttu-id="cae5e-221">In Visual Basic wird eine ADO-Objektvariable (in diesem Fall für ein **Recordset** -Objekt) wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="cae5e-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="cae5e-222">Die Klausel "ADODB. Recordset-Objekt"ist die ProgID des **Recordset** -Objekts an, wie in der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="cae5e-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="cae5e-223">Eine neue Instanz eines **Record** -Objekts wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="cae5e-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="cae5e-224">\-oder -</span><span class="sxs-lookup"><span data-stu-id="cae5e-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="cae5e-225">In Visual C++ die \*\* \#importieren\*\* Richtlinie generiert intelligente Zeiger-Typ-Deklarationen für alle ADO-Objekte.</span><span class="sxs-lookup"><span data-stu-id="cae5e-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="cae5e-226">Beispielsweise eine Variable, die auf zeigt eine \*\* \_Recordset\*\* -Objekt ist vom Typ \*\* \_RecordsetPtr\*\*, und wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="cae5e-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="cae5e-227">Eine Variable, die auf eine neue Instanz des zeigt eine \*\* \_Recordset\*\* Objekt wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="cae5e-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="cae5e-228">\-oder -</span><span class="sxs-lookup"><span data-stu-id="cae5e-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="cae5e-229">\-oder -</span><span class="sxs-lookup"><span data-stu-id="cae5e-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="cae5e-230">Nachdem die **CreateInstance** -Methode aufgerufen wurde, kann die Variable wie folgt verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="cae5e-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="cae5e-231">Beachten Sie, dass in einem Fall der "." Operator wird verwendet, als wäre der Variablen eine Instanz einer Klasse (Rs. CreateInstance), und in einem anderen Fall die "-\>" Operator wird verwendet, als wären die Variable einen Zeiger auf eine Schnittstelle (Rs -\>öffnen).</span><span class="sxs-lookup"><span data-stu-id="cae5e-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="cae5e-232">Eine Variable kann auf zwei Arten verwendet werden, da die "-\>" Operator wird überladen, um eine Instanz einer Klasse wie ein Zeiger auf eine Schnittstelle Verhalten kann.</span><span class="sxs-lookup"><span data-stu-id="cae5e-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="cae5e-233">Mitglied private-Klasse die Instanzvariable enthält einen Zeiger auf die \*\* \_Recordset\*\* Schnittstelle. die "-\>" Operator zurückgibt, Zeiger; und der zurückgegebene Zeiger greift auf die Mitglieder der \*\* \_Recordset\*\* Objekt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="cae5e-234">Codieren eines fehlenden Parameters - "Variant"</span><span class="sxs-lookup"><span data-stu-id="cae5e-234">Coding a Missing Parameter</span></span>

<span data-ttu-id="cae5e-235">Wenn Sie einen fehlenden **String** -Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden aus.</span><span class="sxs-lookup"><span data-stu-id="cae5e-235">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="cae5e-236">Sie müssen den Operanden in Visual C++ angeben.</span><span class="sxs-lookup"><span data-stu-id="cae5e-236">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="cae5e-237">Code ein \*\* \_Bstr\_t\*\* , die eine leere Zeichenfolge als Wert hat.</span><span class="sxs-lookup"><span data-stu-id="cae5e-237">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="cae5e-238">Codieren eines fehlenden Parameters - "Variant"</span><span class="sxs-lookup"><span data-stu-id="cae5e-238">Coding a Missing Parameter</span></span>

<span data-ttu-id="cae5e-239">Wenn Sie einen fehlenden **Variant** Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden.</span><span class="sxs-lookup"><span data-stu-id="cae5e-239">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="cae5e-240">Sie müssen alle Operanden in Visual C++ angeben.</span><span class="sxs-lookup"><span data-stu-id="cae5e-240">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="cae5e-241">Codieren ein fehlenden Parameters **Variant-Wert** mit einer \*\* \_Variant\_t\*\* legen Sie den speziellen Wert, Verschiebung\_E\_PARAMNOTFOUND und Typ, VT\_Fehler.</span><span class="sxs-lookup"><span data-stu-id="cae5e-241">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="cae5e-242">Geben Sie alternativ **VtMissing**, die Entsprechung ist vordefinierte Konstante von bereitgestellt wird, die \*\* \#importieren\*\* Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="cae5e-242">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="cae5e-243">\-oder verwenden Sie-</span><span class="sxs-lookup"><span data-stu-id="cae5e-243">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a><span data-ttu-id="cae5e-244">Deklarieren eines Variant-Werts</span><span class="sxs-lookup"><span data-stu-id="cae5e-244">Declaring a Variant</span></span>

<span data-ttu-id="cae5e-245">In Visual Basic wird ein **Variant** -Wert wie folgt mit der **Dim** -Anweisung deklariert:</span><span class="sxs-lookup"><span data-stu-id="cae5e-245">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="cae5e-246">Deklarieren Sie eine Variable als Typ in Visual C++ \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-246">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="cae5e-247">Einige schematische Darstellung \*\* \_Variant\_t\*\* Deklarationen sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-247">A few schematic **\_variant\_t** declarations are shown below.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cae5e-p139">[!HINWEIS] Diese Deklarationen geben Ihnen lediglich eine ungefähre Vorstellung davon, was Sie in Ihrem eigenen Programm codieren können. Weitere Informationen finden Sie in den Beispielen unten und in der Visual C++-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="cae5e-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span></P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a><span data-ttu-id="cae5e-250">Verwenden von Arrays von Variant-Werten</span><span class="sxs-lookup"><span data-stu-id="cae5e-250">Using Arrays of Variants</span></span>

<span data-ttu-id="cae5e-251">In Visual Basic können Arrays von **Variant** -Werten mit der **Dim** -Anweisung codiert werden. Sie können dazu auch die **Array** -Funktion verwenden, wie im folgenden Beispielcode dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cae5e-251">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

<span data-ttu-id="cae5e-252">Im folgenden Visual C++-Beispiel veranschaulicht die Verwendung von **SafeArray** mit verwendet eine \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-252">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cae5e-253">[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="cae5e-253">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="cae5e-254">Auch hier wird die TESTHR()-Inlinefunktion definiert, um den vorhandenen Mechanismus für die Fehlerbehandlung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-254">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2.  <span data-ttu-id="cae5e-p140">Sie benötigen nur ein eindimensionales Array, sodass Sie **SafeArrayCreateVector** verwenden können, statt der allgemeinen **SAFEARRAYBOUND** -Deklaration und der **SafeArrayCreate** -Funktion. Der Code würde wie folgt aussehen, wenn **SafeArrayCreate** verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="cae5e-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  <span data-ttu-id="cae5e-257">Das Schema, identifiziert durch die enumerierte Konstante **AdSchemaColumns**, vier Einschränkungsspalten zugeordnet ist: Tabelle\_Katalog, Tabelle\_SCHEMA, Tabelle\_Namen und Spalte\_NAME.</span><span class="sxs-lookup"><span data-stu-id="cae5e-257">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="cae5e-258">Aus diesem Grund wird ein Array von **Variant** -Werten mit vier Elementen erstellt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-258">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="cae5e-259">Klicken Sie dann einen Einschränkungswert, die die dritte Spalte, Tabelle entspricht\_NAME angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cae5e-259">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="cae5e-260">Das **Recordset-Objekt** , das zurückgegeben wird besteht aus mehreren Spalten, die eine, die Teilmenge der Einschränkungsspalten ist.</span><span class="sxs-lookup"><span data-stu-id="cae5e-260">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="cae5e-261">Die Werte der Einschränkungsspalten für jede Zeile zurückgegebene muss die entsprechende Einschränkungswerte identisch.</span><span class="sxs-lookup"><span data-stu-id="cae5e-261">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4.  <span data-ttu-id="cae5e-262">Mit **SAFEARRAY** vertraut sind möglicherweise überrascht sein, dass **SafeArrayDestroy()** nicht vor dem Exit aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cae5e-262">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="cae5e-263">Tatsächlich wird **SafeArrayDestroy()** Aufrufen in diesem Fall eine Laufzeit-Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cae5e-263">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="cae5e-264">Der Grund dafür besteht darin, dass der Destruktor für VtCriteria soll ( **VariantClear aufgerufen werden**) Wenn der \*\* \_Variant\_t\*\* wechselt außerhalb des Gültigkeitsbereichs, **SafeArray**freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cae5e-264">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="cae5e-265">Aufrufen von **SafeArrayDestroy**, ohne manuell löschen der \*\* \_Variant-Wert\_t\*\*, würde den Destruktor versuchen, einen ungültigen **SafeArray** Zeiger zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cae5e-265">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="cae5e-266">Wenn **SafeArrayDestroy** aufgerufen wird, würde der Code wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="cae5e-266">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    <span data-ttu-id="cae5e-267">Es ist jedoch viel einfacher, lassen Sie die \*\* \_Variant\_t\*\* **SafeArray**verwalten.</span><span class="sxs-lookup"><span data-stu-id="cae5e-267">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>

<!-- end list -->

```cpp 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
#include <stdio.h> 
 
// Note 1 
inline void TESTHR( HRESULT _hr ) 
 { if FAILED(_hr) _com_issue_error(_hr); } 
 
void main(void) 
{ 
 CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 _ConnectionPtr pCn("ADODB.Connection"); 
 _variant_t vtTableName("authors"), 
 vtCriteria; 
 long ix[1]; 
 SAFEARRAY *pSa = NULL; 
 
 pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
 adConnectUnspecified); 
// Note 2, Note 3 
 pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
 if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
 
// Specify TABLE_NAME in the third array element (index of 2). 
 
 ix[0] = 2; 
 TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
 
// There is no Variant constructor for a SafeArray, so manually set the 
// type (SafeArray of Variant) and value (pointer to a SafeArray). 
 
 vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
 vtCriteria.parray = pSa; 
 
 pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
 
 long limit = pRs->GetFields()->Count; 
 for (long x = 0; x < limit; x++) 
 printf("%d: %s\n", x+1, 
 ((char*) pRs->GetFields()->Item[x]->Name)); 
// Note 4 
 pRs->Close(); 
 pCn->Close(); 
 } 
 catch (_com_error &e) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
 printf("Source = %s\n", (char*) e.Source()); 
 printf("Description = %s\n", (char*) e.Description()); 
 } 
 CoUninitialize(); 
} 
```

## <a name="using-property-getputputref"></a><span data-ttu-id="cae5e-268">Verwenden der Get/Put/PutRef-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cae5e-268">Using Property Get/Put/PutRef</span></span>

<span data-ttu-id="cae5e-269">In Visual Basic wird der Name einer Eigenschaft nicht dadurch qualifiziert, ob sie abgerufen oder zugewiesen wird bzw. ob ihr ein Verweis zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cae5e-269">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

<span data-ttu-id="cae5e-270">In diesem Visual C++-Beispiel wird gezeigt, **Abrufen**/**platzieren**/\**PutRef \*\*\* Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="cae5e-270">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>


> [!NOTE]
> <span data-ttu-id="cae5e-271">[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="cae5e-271">The following notes correspond to commented sections in the code example.</span></span>



1.  <span data-ttu-id="cae5e-272">In diesem Beispiel werden zwei Arten von einem fehlenden Zeichenfolgenargument: eine explizite Konstante, **StrMissing**und eine Zeichenfolge, die der Compiler erstellen einen temporären \*\* \_Bstr\_t\*\* vorhanden, die für den Bereich der **Open** -Methode.</span><span class="sxs-lookup"><span data-stu-id="cae5e-272">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2.  <span data-ttu-id="cae5e-273">Es ist nicht erforderlich, das Umwandeln des Operanden von Rs -\>PutRefActiveConnection(cn) an (IDispatch \*), da der Operand bereits ist (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="cae5e-273">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="using-getitemx-and-itemx"></a><span data-ttu-id="cae5e-274">Mithilfe von "GetItem(x)" und "Item\[x\]</span><span class="sxs-lookup"><span data-stu-id="cae5e-274">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="cae5e-275">Mit diesem Visual Basic-Beispiel wird die standardmäßige und die alternative Syntax für **Item()** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-275">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

<span data-ttu-id="cae5e-276">Mit diesem Visual C++-Beispiel wird **Item** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-276">This Visual C++ example demonstrates **Item**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cae5e-277">[!HINWEIS] Der folgende Hinweis entspricht kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="cae5e-277">The following note corresponds to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="cae5e-278">Wenn mit **Item** auf die Auflistung zugegriffen wird, muss der Index **2** in **long** umgewandelt werden, damit ein geeigneter Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cae5e-278">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="cae5e-279">Umwandeln von ADO-Objektzeigern mit "(IDispatch \*)"</span><span class="sxs-lookup"><span data-stu-id="cae5e-279">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="cae5e-280">Im folgenden Visual C++-Beispiel veranschaulicht die Verwendung (IDispatch \*) zu Cast ADO-Objektzeigern veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cae5e-280">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cae5e-281">[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="cae5e-281">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="cae5e-282">Geben Sie ein geöffnetes **Connection** -Objekt in einer explizit codierten- **Variant**.</span><span class="sxs-lookup"><span data-stu-id="cae5e-282">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="cae5e-283">Wandeln sie mit (IDispatch \*), damit der richtige Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cae5e-283">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="cae5e-284">Auch explizit festlegen, die zweite \*\* \_Variant\_t\*\* Parameter auf den Standardwert **true**, so dass der Referenzzähler Objekt am Ende des Vorgangs **Open** korrekt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-284">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2.  <span data-ttu-id="cae5e-285">Der Ausdruck (\_Bstr\_t), wird nicht umgewandelt, aber ein \*\* \_Variant-Wert\_t\*\* Operator, der extrahiert ein \*\* \_Bstr\_t\*\* Zeichenfolge aus der zurückgegebene **Wert** **Variant-Wert** .</span><span class="sxs-lookup"><span data-stu-id="cae5e-285">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="cae5e-286">Der Ausdruck (Char\*), wird nicht umgewandelt, aber ein \*\* \_Bstr\_t\*\* Operator, der einen Zeiger in die gekapselte Zeichenfolge in extrahiert ein \*\* \_Bstr\_t\*\* Objekt.</span><span class="sxs-lookup"><span data-stu-id="cae5e-286">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="cae5e-287">In diesem Abschnitt werden einige nützliche Verhaltensweisen von veranschaulicht \*\* \_Variant\_t\*\* und \*\* \_Bstr\_t\*\* Operatoren.</span><span class="sxs-lookup"><span data-stu-id="cae5e-287">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
    ```

