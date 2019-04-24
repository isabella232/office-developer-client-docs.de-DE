---
title: Visual C++ ADO-Programmierung
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302772"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="a05d7-102">Visual C++ ADO-Programmierung</span><span class="sxs-lookup"><span data-stu-id="a05d7-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="a05d7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a05d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a05d7-104">In der ADO-API-Referenz wird die Funktionalität der ADO-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit einer Microsoft Visual Basic ähnlichen Syntax beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="a05d7-105">Obwohl die Zielgruppe alle Benutzer ist, verwenden ADO-Programmierer unterschiedliche Sprachen wie Visual Basic, Visual C++ (mit und ohne die \*\* \#Import\*\* -Direktive) und Visual J++ (mit dem Class-Paket ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="a05d7-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="a05d7-106">Um dieser Vielfalt gerecht zu werden, bieten die [ADO für Visual C++-Syntaxindizes](using-ado-with-microsoft-visual-c.md) eine Visual C++-sprachspezifische Syntax mit Verknüpfungen zu allgemeinen Beschreibungen der Funktionalität, der Parameter, außergewöhnlichen Verhaltensweisen usw. in der API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="a05d7-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="a05d7-p102">ADO wird mit COM-Schnittstellen (Component Object Model) implementiert. In bestimmten Programmiersprachen ist es jedoch einfacher für Programmierer mit COM zu arbeiten als in anderen. Beispielsweise werden nahezu alle Details der Verwendung von COM implizit für Visual Basic-Programmierer behandelt, wohingegen Visual C++-Programmierer die Details selbst ermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="a05d7-110">In den folgenden Abschnitten werden die Details für C-und C++-Programmierer mit ADO und der \*\* \#Import\*\* -Direktive zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a05d7-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="a05d7-111">Der Schwerpunkt liegt auf Datentypen, die für COM (**Variant**, **BSTR**und **SAFEARRAY**) spezifisch sind,\_und\_Fehlerbehandlung (com-Fehler).</span><span class="sxs-lookup"><span data-stu-id="a05d7-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="a05d7-112">Verwenden der \#Import Compiler-Direktive</span><span class="sxs-lookup"><span data-stu-id="a05d7-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="a05d7-113">Die Compiler-Direktive Visual C++ \*\* \#importieren\*\* vereinfacht das Arbeiten mit den ADO-Methoden und-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a05d7-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="a05d7-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span><span class="sxs-lookup"><span data-stu-id="a05d7-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="a05d7-115">Each interface is encapsulated, or wrapped, in a class.</span><span class="sxs-lookup"><span data-stu-id="a05d7-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="a05d7-p105">Für jeden Vorgang in einer Klasse (also ein Methoden- oder Eigenschaftenaufruf) gibt es eine Deklaration, um den Vorgang direkt aufzurufen (also die "Rohform" des Vorgangs), und eine Deklaration, um den Rohvorgang aufzurufen und einen COM-Fehler auszulösen, wenn der Vorgang nicht erfolgreich ausgeführt wird. Wenn es sich bei dem Vorgang um eine Eigenschaft handelt, wird normalerweise mit einer Compilerdirektive eine alternative Syntax für den Vorgang erstellt, die der Syntax von Visual Basic ähnelt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="a05d7-118">Vorgänge, die den Wert einer Eigenschaft abrufen, haben Namen des Formulars, \*\*Get \* \* *-Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="a05d7-119">Vorgänge, die den Wert einer Eigenschaft festlegen, haben Namen des Formulars, \*\*Put \* \* *-Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="a05d7-120">Vorgänge, die den Wert einer Eigenschaft mit einem Zeiger auf ein ADO-Objekt festlegen, haben die Namen des Formulars, \*\*PutRef \* \* *-Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="a05d7-121">Sie können eine Eigenschaft mit Aufrufen in der folgenden Form abrufen oder festlegen:</span><span class="sxs-lookup"><span data-stu-id="a05d7-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="a05d7-122">Verwenden von Eigenschafts Direktiven</span><span class="sxs-lookup"><span data-stu-id="a05d7-122">Using property directives</span></span>

<span data-ttu-id="a05d7-123">\*\* \_Die \_declspec (Property...)\*\* -Compiler-Direktive ist eine Microsoft-spezifische C-Spracherweiterung, die eine Funktion deklariert, die als Eigenschaft verwendet wird, um eine alternative Syntax zu haben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="a05d7-124">Daher können Sie Werte einer Eigenschaft ähnlich wie bei Visual Basic festlegen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="a05d7-125">Sie können z. B. wie folgt eine Eigenschaft festlegen und abrufen:</span><span class="sxs-lookup"><span data-stu-id="a05d7-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="a05d7-126">Der Code muss nicht wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="a05d7-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="a05d7-127">Der Compiler generiert den entsprechenden \*\*Get \*\*\* \* \*-, **Put**-oder \*\*PutRef \* \* *-Eigenschafts* Aufruf basierend darauf, welche Alternative Syntax deklariert wird und ob die Eigenschaft gelesen oder geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="a05d7-128">\*\* \_Die \_declspec (Property...)\*\* -Compiler-Direktive kann **nur Get**-, **Put**-oder **Get** -und **Put** -alternative Syntax für eine Funktion deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a05d7-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="a05d7-129">Schreibgeschützte Vorgänge haben nur eine **Get** -Deklaration; schreibgeschützte Vorgänge haben nur eine **Put** -Deklaration; sowohl Lese-als auch Schreibvorgänge haben sowohl **Get** -als auch **Put** -Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="a05d7-130">Nur zwei Deklarationen sind mit dieser Direktive möglich; jede Eigenschaft kann jedoch drei Eigenschaftsfunktionen aufweisen: \*\*Get \*\*\* \* Property, \*\*Put \*\*\* \* Property und \**PutRef \* \* \* Property*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="a05d7-131">In diesem Fall haben nur zwei Formen der Eigenschaft die alternative Syntax.</span><span class="sxs-lookup"><span data-stu-id="a05d7-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="a05d7-132">Beispielsweise wird die **ActiveConnection** -Eigenschaft des **Command** -Objekts mit einer alternativen Syntax für \*\*Get \* \*\* \* \* ActiveConnection und \**PutRef \* \* \* ActiveConnection*deklariert.</span><span class="sxs-lookup"><span data-stu-id="a05d7-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="a05d7-133">Die **PutRef**-Syntax ist eine gute Wahl, weil Sie in der Praxis üblicherweise in diese Eigenschaft ein offenes **Connection**-Objekt aufnehmen (d. h. einen **Connection**-Objektzeiger).</span><span class="sxs-lookup"><span data-stu-id="a05d7-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="a05d7-134">Andererseits verfügt das **Recordset** -Objekt über **Get**-, **Put**-und \**PutRef \* \* \* ActiveConnection* -Operationen, jedoch keine alternative Syntax.</span><span class="sxs-lookup"><span data-stu-id="a05d7-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="a05d7-135">Auflistungen, die GetItem-Methode und die Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a05d7-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="a05d7-136">ADO definiert mehrere Auflistungen, einschließlich **Fields**, **Parameters**, **Properties** und **Errors**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="a05d7-137">In Visual C++ gibt die **GetItem (***Index***)** -Methode ein Element der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="a05d7-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="a05d7-138">*Index* ist ein **Variant**-Wert, der eigentliche Wert ist ein numerischer Index des Members in der Auflistung oder eine Zeichenfolge mit dem Namen des Members.</span><span class="sxs-lookup"><span data-stu-id="a05d7-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="a05d7-139">\*\* \_Die \_declspec (Property...)\*\* -Compiler-Direktive deklariert die **Item** -Eigenschaft als alternative Syntax für die grundlegende **GetItem ()** -Methode der einzelnen Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="a05d7-140">Für die alternative Syntax werden eckige Klammern verwendet, und sie ähnelt einem Arrayverweis.</span><span class="sxs-lookup"><span data-stu-id="a05d7-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="a05d7-141">Im Allgemeinen sehen die beiden Formen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="a05d7-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="a05d7-142">Weisen Sie z. B. einem Feld des **Recordset**-Objekts mit dem Namen ***rs*** einen Wert zu, der aus der **authors**-Tabelle der **pubs**-Datenbank abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="a05d7-143">Verwenden Sie die **Item ()** -Eigenschaft für den Zugriff auf das dritte **Feld** der **Fields** -Auflistung des **Recordset** -Objekts (Auflistungen werden von Null indiziert; davon ausgehend, dass das dritte Feld den Namen ***au\_fname***).</span><span class="sxs-lookup"><span data-stu-id="a05d7-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="a05d7-144">Rufen Sie dann die **Value()**-Methode für das **Field**-Objekt auf, um einen Zeichenfolgenwert zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="a05d7-145">Dies kann in Visual Basic auf die folgenden vier Arten ausgedrückt werden (die beiden letzten Formen gelten nur für Visual Basic, in anderen Sprachen gibt es keine Entsprechungen):</span><span class="sxs-lookup"><span data-stu-id="a05d7-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="a05d7-146">Die Entsprechung in Visual C++ zu den ersten beiden Formen lautet:</span><span class="sxs-lookup"><span data-stu-id="a05d7-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="a05d7-147">\-oder-(die alternative Syntax für die **value** -Eigenschaft wird ebenfalls angezeigt)</span><span class="sxs-lookup"><span data-stu-id="a05d7-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="a05d7-148">COM-spezifische Datentypen</span><span class="sxs-lookup"><span data-stu-id="a05d7-148">COM-specific data types</span></span>

<span data-ttu-id="a05d7-p114">Im Allgemeinen weisen alle Visual Basic-Datentypen, die Sie in der ADO-API-Referenz finden, eine Visual C++-Entsprechung auf. Dazu gehören Standarddatentypen wie **unsigned char** für **Byte** in Visual Basic, **short** für **Integer** und **long** für **Long**. Mithilfe der Syntaxindizes können Sie genau feststellen, was für die Operanden einer bestimmten Methode oder Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="a05d7-152">Ausnahmen zu dieser Regel bilden die Datentypen, die nur für COM gelten: **Variant**, **BSTR** und **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="a05d7-153">Variant</span><span class="sxs-lookup"><span data-stu-id="a05d7-153">Variant</span></span>

<span data-ttu-id="a05d7-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p115">A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="a05d7-157">Die \*\* \_Variant\_\*\* -Klasse t kapselt und verwaltet den **Variant** -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a05d7-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="a05d7-158">Wenn die ADO-API-Referenz besagt, dass eine Methode oder ein Eigenschafts Operand einen Wert akzeptiert, bedeutet dies normalerweise, dass der Wert in einem \*\* \_Variant-Datentyp\_\*\* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="a05d7-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="a05d7-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="a05d7-162">BSTR</span></span>

<span data-ttu-id="a05d7-p117">**BSTR** (**B**asic **STR**ing) ist ein strukturierter Datentyp, der eine Zeichenfolge und die Länge der Zeichenfolge enthält. COM bietet Methoden zum Zuordnen, Ändern und Freigeben eines **BSTR**-Werts.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="a05d7-165">Die \*\* \_BSTR\_t\*\* -Klasse kapselt und verwaltet den **BSTR** -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a05d7-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="a05d7-166">Wenn die ADO-API-Referenz besagt, dass eine Methode oder Eigenschaft einen **String** -Wert akzeptiert, bedeutet dies, dass der Wert in der Form von \*\* \_BSTR\_t\*\*ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="a05d7-167">Umwandeln \_von\_Variant- \_Datentyp\_t und BSTR t-Klassen</span><span class="sxs-lookup"><span data-stu-id="a05d7-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="a05d7-168">Häufig ist es nicht erforderlich, einen \*\* \_\_Variant\*\* -Wert oder \*\* \_BSTR\_t\*\* in einem Argument für einen Vorgang explizit zu codieren.</span><span class="sxs-lookup"><span data-stu-id="a05d7-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="a05d7-169">Wenn die \*\* \_Variant\_\*\* -Klasse t oder \*\* \_BSTR\_t\*\* einen Konstruktor besitzt, der mit dem Datentyp des Arguments übereinstimmt, generiert der Compiler die \*\* \_entsprechende\_Variante t\*\* oder \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="a05d7-170">Wenn das Argument jedoch nicht eindeutig ist, wenn also der Datentyp des Arguments mit mehr als einem Konstruktor übereinstimmt, müssen Sie das Argument mit dem entsprechenden Datentyp umwandeln, um den richtigen Konstruktor aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="a05d7-171">Beispielsweise lautet die Deklaration für die **Recordset::Open** -Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a05d7-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="a05d7-172">Das ActiveConnection-Argument übernimmt einen Verweis auf \*\* \_einen\_Variant\*\*-Wert, den Sie als Verbindungszeichenfolge oder als Zeiger auf ein geöffnetes **Connection** -Objekt codieren können.</span><span class="sxs-lookup"><span data-stu-id="a05d7-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="a05d7-173">Die richtige \*\* \_Variante\_t\*\* wird implizit erstellt, wenn Sie eine Zeichenfolge wie "DSN = Pubs; UID = SA; pwd =;" oder einen Zeiger wie "(IDispatch \*) pConn" weitergeben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="a05d7-174">Oder Sie können einen \*\* \_Variant\_\*\* -Wert mit einem Zeiger wie "\_Variant\_t ((IDispatch \*) pConn, true)" explizit codieren.</span><span class="sxs-lookup"><span data-stu-id="a05d7-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="a05d7-175">Die Umwandlung (IDispatch \*) löst die Mehrdeutigkeit mit einem anderen Konstruktor auf, der einen Zeiger auf eine IUnknown-Schnittstelle annimmt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="a05d7-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="a05d7-178">Im letzten Fall wird das zweite boolesche Argument des Konstruktors explizit mit dem optionalen Standardwert true codiert.</span><span class="sxs-lookup"><span data-stu-id="a05d7-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="a05d7-179">Dieses Argument bewirkt, dass der **Variant** -Konstruktor seine **AddRef**()-Methode aufruft, durch die ADO beim Abschluss des ADO-Methoden-oder-Eigenschaften Aufrufs automatisch den \*\* \_Variant-Datentyp\_t:: Release\*\*() aufruft.</span><span class="sxs-lookup"><span data-stu-id="a05d7-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="a05d7-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="a05d7-180">SafeArray</span></span>

<span data-ttu-id="a05d7-p122">**SafeArray** ist ein strukturierter Datentyp, der ein Array anderer Datentypen enthält. **SafeArray** wird als *safe* (sicher) bezeichnet, da dieser Datentyp Informationen zu den Grenzen der einzelnen Arraydimensionen enthält und den Zugriff auf die Arrayelemente innerhalb dieser Grenzen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p122">A **SafeArray** is a structured data type that contains an array of other data types. A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="a05d7-183">Wenn in der ADO-API-Referenz angegeben ist, dass eine Methode oder Eigenschaft ein Array übernimmt oder zurückgibt, bedeutet dies, dass die Methode oder Eigenschaft einen **SafeArray** -Wert übernimmt oder zurückgibt, kein systemeigenes C/C++-Array.</span><span class="sxs-lookup"><span data-stu-id="a05d7-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="a05d7-p123">Für den zweiten Parameter der **OpenSchema** -Methode des **Connection** -Objekts ist z. B. ein Array von **Variant** -Werten erforderlich. Diese **Variant** -Werte müssen als Elemente eines **SafeArray** -Werts übergeben werden, und dieser **SafeArray** -Wert muss als Wert eines anderen **Variant** -Werts festgelegt werden. Dieser andere **Variant** -Wert wird als zweites Argument von **OpenSchema** übergeben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p123">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values. Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**. It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="a05d7-187">Als weiteres Beispiel ist das erste Argument der **Find** -Methode ein **Variant** -Wert, dessen Wert ein eindimensionaler **SafeArray** -Wert ist. Jedes optionale erste und zweite Argument von **AddNew** ist ein eindimensionaler **SafeArray** -Wert, und der Rückgabewert der **GetRows** -Methode ist ein **Variant** -Wert, dessen Wert ein zweidimensionaler **SafeArray** -Wert ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="a05d7-188">Fehlende und Standardparameter</span><span class="sxs-lookup"><span data-stu-id="a05d7-188">Missing and default parameters</span></span>

<span data-ttu-id="a05d7-p124">Bei Visual Basic sind fehlende Parameter in Methoden zulässig. Die **Open** -Methode des **Recordset** -Objekts weist z. B. fünf Parameter auf, aber Sie können Zwischenparameter überspringen und nachstehende Parameter auslassen. Ein standardmäßiger **BSTR** - oder **Variant** -Wert wird je nach Datentyp des fehlenden Operanden ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="a05d7-192">In C/C++, all operands must be specified.</span><span class="sxs-lookup"><span data-stu-id="a05d7-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="a05d7-193">Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp eine Zeichenfolge ist, geben Sie \*\* \_ein\_BSTR t\*\* an, das eine NULL-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="a05d7-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="a05d7-194">Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp ein **Variant**-Datentyp ist, geben Sie einen \*\* \_\_t\*\* -Datentyp mit dem\_Wert\_"Dispo E PARAMNOTFOUND" und\_einen VT-Fehlertyp an.</span><span class="sxs-lookup"><span data-stu-id="a05d7-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="a05d7-195">Alternativ können Sie die äquivalente \*\* \_Variante\_t\*\* , **vtMissing**, angeben, die von der \*\* \#Import\*\* -Direktive bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="a05d7-p126">Drei Methoden bilden Ausnahmen zur üblichen Verwendung von **vtMissing**. Dies sind die **Execute** -Methoden der Objekte **Connection** - und **Command** -Objekte sowie die **NextRecordset** -Methode des **Recordset** -Objekts. Im Folgenden sind deren Signaturen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="a05d7-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="a05d7-p127">Die Parameter *RecordsAffected* und *Parameters* sind Zeiger auf einen **Variant**-Wert. *Parameters* ist ein Eingabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, der einen Parameter oder ein Array von Parametern enthält, der bzw. das den ausgeführten Befehl ändert. *RecordsAffected* ist ein Ausgabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, an den die Anzahl der von der Methode betroffenen Zeilen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="a05d7-202">Geben Sie in der **Execute** -Methode des **Command** -Objekts an, dass keine Parameter durch Festlegen \&von *Parametern* für vtMissing (was empfohlen wird) oder für den NULL-Zeiger (also **null** oder NULL (0)) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a05d7-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="a05d7-203">Wird *Parameters* auf einen NULL-Zeiger festgelegt, ersetzt die Methode intern die Entsprechung von **vtMissing** und schließt dann den Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="a05d7-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="a05d7-p129">Geben Sie für alle Methoden an, dass die Anzahl betroffener Datensätze nicht zurückgegeben werden soll, indem Sie *RecordsAffected* auf den NULL-Zeiger festlegen. In diesem Fall ist der NULL-Zeiger kein fehlender Parameter, sondern ein Kennzeichen dafür, dass die Methode die Anzahl betroffener Datensätze verwerfen soll.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p129">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer. In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="a05d7-206">Deshalb können Sie für diese drei Methoden z. B. folgenden Code schreiben:</span><span class="sxs-lookup"><span data-stu-id="a05d7-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="a05d7-207">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="a05d7-207">Error handling</span></span>

<span data-ttu-id="a05d7-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span><span class="sxs-lookup"><span data-stu-id="a05d7-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="a05d7-209">Die \*\* \#Import\*\* -Direktive generiert Wrappercode um jede "rohe" Methode oder Eigenschaft und überprüft das zurückgegebene HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a05d7-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="a05d7-210">Wenn der HRESULT-Fehler angibt, löst der Wrappercode einen COM-Fehler \_aus\_,\_indem com-Problem errorex () mit dem HRESULT-Rückgabecode als Argument aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="a05d7-211">COM error objects can be caught in a **try**-**catch** block.</span><span class="sxs-lookup"><span data-stu-id="a05d7-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="a05d7-212">(Aus Effizienzgründen sollten Sie einen Verweis auf ein \*\* \_com\_Error\*\* -Objekt abfangen.)</span><span class="sxs-lookup"><span data-stu-id="a05d7-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="a05d7-p131">Bedenken Sie, dass es sich dabei um ADO-Fehler handelt: Sie resultieren daraus, dass der ADO-Vorgang fehlschlägt. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="a05d7-215">Die \*\* \#Import\*\* -Direktive erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die in der ADO. dll deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="a05d7-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="a05d7-216">Sie können jedoch den gleichen Mechanismus für die Fehlerbehandlung nutzen, indem Sie ein eigenes Makro oder eine Inlinefunktion für die Fehlerüberprüfung schreiben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="a05d7-217">Beispiele finden Sie im Thema [Visual C++-Erweiterungen](visual-c-extensions-for-ado.md) oder im Code in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="a05d7-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="a05d7-218">Visual C++-Entsprechungen von Visual Basic-Konventionen</span><span class="sxs-lookup"><span data-stu-id="a05d7-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="a05d7-219">Im Folgenden finden Sie eine Zusammenfassung verschiedener Konventionen in der ADO-Dokumentation, codiert in Visual Basic, sowie deren Entsprechungen in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a05d7-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="a05d7-220">Deklarieren eines ADO-Objekts</span><span class="sxs-lookup"><span data-stu-id="a05d7-220">Declaring an ADO object</span></span>

<span data-ttu-id="a05d7-221">In Visual Basic wird eine ADO-Objektvariable (in diesem Fall für ein **Recordset** -Objekt) wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="a05d7-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="a05d7-222">Die Klausel "ADODB. Recordset "ist die ProgID des **Recordset** -Objekts, wie in der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="a05d7-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="a05d7-223">Eine neue Instanz eines **Record** -Objekts wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="a05d7-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="a05d7-224">\-oder</span><span class="sxs-lookup"><span data-stu-id="a05d7-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="a05d7-225">In Visual C++ generiert die \*\* \#Import\*\* -Direktive Smart Pointer-Type-Deklarationen für alle ADO-Objekte.</span><span class="sxs-lookup"><span data-stu-id="a05d7-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="a05d7-226">Eine Variable, die auf ein \*\* \_Recordset\*\* -Objekt zeigt, hat beispielsweise den Typ \*\* \_RecordsetPtr\*\*und wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="a05d7-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="a05d7-227">Eine Variable, die auf eine neue Instanz eines \*\* \_Recordset\*\* -Objekts verweist, wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="a05d7-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="a05d7-228">\-oder</span><span class="sxs-lookup"><span data-stu-id="a05d7-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="a05d7-229">\-oder</span><span class="sxs-lookup"><span data-stu-id="a05d7-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="a05d7-230">Nachdem die **CreateInstance** -Methode aufgerufen wurde, kann die Variable wie folgt verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="a05d7-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="a05d7-231">Beachten Sie, dass in einem Fall der "."-Operator verwendet wird, als ob die Variable eine Instanz einer Klasse (Rs. CreateInstance), und in einem anderen Fall wird der Operator "\>-" verwendet, als ob die Variable ein Zeiger auf eine Schnittstelle (RS-\>Open) wäre.</span><span class="sxs-lookup"><span data-stu-id="a05d7-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="a05d7-232">Eine Variable kann auf zweierlei Weise verwendet werden, da der\>Operator "-" überlastet ist, damit eine Instanz einer Klasse sich wie ein Zeiger auf eine Schnittstelle verhält.</span><span class="sxs-lookup"><span data-stu-id="a05d7-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="a05d7-233">Ein privates Klassenmember der Instanzenvariablen enthält einen Zeiger auf die \*\* \_Recordset\*\* -Schnittstelle; der Operator "\>-" gibt diesen Zeiger zurück; und der zurückgegebene Zeiger greift auf die Member des \*\* \_Recordset\*\* -Objekts zu.</span><span class="sxs-lookup"><span data-stu-id="a05d7-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="a05d7-234">Codieren eines fehlenden Parameters</span><span class="sxs-lookup"><span data-stu-id="a05d7-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="a05d7-235">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a05d7-235">String</span></span>

<span data-ttu-id="a05d7-236">Wenn Sie einen fehlenden **String** -Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden aus.</span><span class="sxs-lookup"><span data-stu-id="a05d7-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="a05d7-237">Sie müssen den Operanden in Visual C++ angeben.</span><span class="sxs-lookup"><span data-stu-id="a05d7-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="a05d7-238">Codieren Sie \*\* \_eine\_BSTR-t\*\* , die eine leere Zeichenfolge als Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="a05d7-239">Variant</span><span class="sxs-lookup"><span data-stu-id="a05d7-239">Variant</span></span>

<span data-ttu-id="a05d7-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span><span class="sxs-lookup"><span data-stu-id="a05d7-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="a05d7-241">You must specify all operands in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a05d7-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="a05d7-242">Codieren eines fehlenden **Variant** -Parameters mit einem \*\* \_\_\*\* Wert vom Typ "Special"\_,\_"Dispo E PARAMNOTFOUND" und\_"Type", VT Error.</span><span class="sxs-lookup"><span data-stu-id="a05d7-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="a05d7-243">Alternativ können Sie **vtMissing**angeben, die eine äquivalente vordefinierte Konstante ist, die von der \*\* \#Import\*\* -Direktive bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="a05d7-244">\-oder use-</span><span class="sxs-lookup"><span data-stu-id="a05d7-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="a05d7-245">Deklarieren eines Variant-Werts</span><span class="sxs-lookup"><span data-stu-id="a05d7-245">Declaring a variant</span></span>

<span data-ttu-id="a05d7-246">In Visual Basic wird ein **Variant** -Wert wie folgt mit der **Dim** -Anweisung deklariert:</span><span class="sxs-lookup"><span data-stu-id="a05d7-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="a05d7-247">Deklarieren Sie in Visual C++ eine Variable als Typ \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="a05d7-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="a05d7-248">Nachfolgend finden Sie einige schematische \*\* \_Variante\_t\*\* -Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="a05d7-p139">[!HINWEIS] Diese Deklarationen geben Ihnen lediglich eine ungefähre Vorstellung davon, was Sie in Ihrem eigenen Programm codieren können. Weitere Informationen finden Sie in den Beispielen unten und in der Visual C++-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a05d7-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="a05d7-251">Verwenden von Arrays von Varianten</span><span class="sxs-lookup"><span data-stu-id="a05d7-251">Using arrays of variants</span></span>

<span data-ttu-id="a05d7-252">In Visual Basic können Arrays von **Variant** -Werten mit der **Dim** -Anweisung codiert werden. Sie können dazu auch die **Array** -Funktion verwenden, wie im folgenden Beispielcode dargestellt:</span><span class="sxs-lookup"><span data-stu-id="a05d7-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="a05d7-253">Im folgenden Visual C++-Beispiel wird die \*\*\*\* Verwendung eines SAFEARRAYs veranschaulicht, das mit einem \*\* \_Variant\_\*\*-Wert von t verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="a05d7-254">Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="a05d7-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a05d7-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span><span class="sxs-lookup"><span data-stu-id="a05d7-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="a05d7-p140">Sie benötigen nur ein eindimensionales Array, sodass Sie **SafeArrayCreateVector** verwenden können, statt der allgemeinen **SAFEARRAYBOUND** -Deklaration und der **SafeArrayCreate** -Funktion. Der Code würde wie folgt aussehen, wenn **SafeArrayCreate** verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="a05d7-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="a05d7-258">Das durch die aufgezählte Konstante, **adSchemaColumns**, angegebene Schema ist mit vier Einschränkungsspalten verknüpft\_: Tabellenkatalog\_, Tabellenschema\_, Tabellenname und\_Spaltenname.</span><span class="sxs-lookup"><span data-stu-id="a05d7-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="a05d7-259">Therefore, an array of **Variant** values with four elements is created.</span><span class="sxs-lookup"><span data-stu-id="a05d7-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="a05d7-260">Dann wird ein Einschränkungswert angegeben, der der dritten Spalte\_, dem Tabellennamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="a05d7-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="a05d7-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span><span class="sxs-lookup"><span data-stu-id="a05d7-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="a05d7-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span><span class="sxs-lookup"><span data-stu-id="a05d7-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="a05d7-263">Wenn Sie mit **SafeArrays** vertraut sind, überrascht es Sie möglicherweise, dass **SafeArrayDestroy()** nicht vor dem Ende aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="a05d7-264">Tatsächlich wird durch den Aufruf von **SafeArrayDestroy()** in diesem Fall eine Laufzeitausnahme verursacht.</span><span class="sxs-lookup"><span data-stu-id="a05d7-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="a05d7-265">Der Grund ist, dass der Destruktor für vtCriteria **VariantClear**() aufrufen wird, wenn der \*\* \_Variant\_\*\* -Wert aus dem Gültigkeitsbereich wechselt, wodurch das **SAFEARRAY**freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="a05d7-266">Der Aufruf von **SafeArrayDestroy**, ohne die \*\* \_Variante\_t\*\*manuell zu löschen, würde dazu führen, dass der Destruktor versucht, einen ungültigen **SAFEARRAY** -Zeiger zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a05d7-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="a05d7-267">Wenn **SafeArrayDestroy** aufgerufen wird, würde der Code wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="a05d7-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="a05d7-268">Es ist jedoch viel einfacher, die \*\* \_\_Variante t\*\* mit **SAFEARRAY**zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a05d7-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


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

### <a name="using-property-getputputref"></a><span data-ttu-id="a05d7-269">Verwenden der Eigenschaft Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="a05d7-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="a05d7-270">In Visual Basic wird der Name einer Eigenschaft nicht dadurch qualifiziert, ob sie abgerufen oder zugewiesen wird bzw. ob ihr ein Verweis zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a05d7-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="a05d7-271">In diesem Visual C++-Beispiel wird die **Get**/**Put**/\*\*-PutRef \* \* *-Eigenschaft*veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a05d7-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="a05d7-272">[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="a05d7-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a05d7-273">In diesem Beispiel werden zwei Formen eines fehlenden Zeichenfolgenarguments verwendet: eine explizite Konstante, **strMissing**und eine Zeichenfolge, mit der der Compiler einen temporären \*\* \_\_BSTR t\*\* erstellt, der für den Bereich der **Open** -Methode vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="a05d7-274">Es ist nicht erforderlich, den Operanden von RS\>-PutRefActiveConnection (CN) in ( \*IDispatch) umzuwandeln, da der Typ des Operanden bereits \*(IDispatch) ist.</span><span class="sxs-lookup"><span data-stu-id="a05d7-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="a05d7-275">Verwenden von GetItem (x)\[und Item x\]</span><span class="sxs-lookup"><span data-stu-id="a05d7-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="a05d7-276">Mit diesem Visual Basic-Beispiel wird die standardmäßige und die alternative Syntax für **Item()** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="a05d7-277">Mit diesem Visual C++-Beispiel wird **Item** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a05d7-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="a05d7-278">[!HINWEIS] Der folgende Hinweis entspricht kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="a05d7-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="a05d7-279">Wenn mit **Item** auf die Auflistung zugegriffen wird, muss der Index **2** in **long** umgewandelt werden, damit ein geeigneter Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="a05d7-280">Umwandeln von ADO-Objektzeigern mit "(IDispatch \*)"</span><span class="sxs-lookup"><span data-stu-id="a05d7-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="a05d7-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span><span class="sxs-lookup"><span data-stu-id="a05d7-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="a05d7-282">[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="a05d7-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a05d7-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span><span class="sxs-lookup"><span data-stu-id="a05d7-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="a05d7-284">Cast it with (IDispatch \*), sodass der richtige Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="a05d7-285">Legen Sie außerdem explizit den zweiten \*\* \_Variant\_\*\* -Parameter auf den Standardwert **true**fest, sodass die Objektverweis Anzahl korrekt ist, wenn das **Recordset:: Open** -Vorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a05d7-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="a05d7-286">\_Der Ausdruck (BSTR\_t) ist keine Umwandlung, sondern ein \*\* \_Variant\_\*\* -Operator, der eine \*\* \_BSTR\_t\*\* -Zeichenfolge aus dem von value zurückgegebenen **Variant** - **Wert**extrahiert.</span><span class="sxs-lookup"><span data-stu-id="a05d7-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="a05d7-287">Der Ausdruck (Char\*) ist keine Umwandlung, sondern ein \*\* \_BSTR\_t\*\* -Operator, der einen Zeiger auf die gekapselte Zeichenfolge in einem \*\* \_BSTR\_t\*\* -Objekt extrahiert.</span><span class="sxs-lookup"><span data-stu-id="a05d7-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="a05d7-288">In diesem Codeabschnitt werden einige der nützlichen Verhaltensweisen von \*\* \_Variant\_t\*\* - \*\* \_und\_BSTR t\*\* -Operatoren veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a05d7-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

