---
title: Verwenden Sie nicht kompatibel mit InfoPath Microsoft.Office.Interop.InfoPath.SemiTrust-Elemente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen mithilfe von Infopath 2007-features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Das vom Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace bereitgestellten Objektmodell enthält Objekte und Elemente, die neuen Funktionen bereitstellen, der die Office InfoPath 2007 und InfoPath hinzugefügt wurde.
ms.openlocfilehash: 3d0e9b450dab6a821af1f698d9859b21e85abf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790746"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="92313-104">Verwenden Sie nicht kompatibel mit InfoPath Microsoft.Office.Interop.InfoPath.SemiTrust-Elemente</span><span class="sxs-lookup"><span data-stu-id="92313-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="92313-105">Beim Hinzufügen von Code zu einer Formularvorlage, die mit dem Microsoft Office InfoPath 2003 Toolkit erstellt wurde, oder erstellen eine neue Formularvorlage, die mit dem InfoPath 2003-kompatible Objektmodell (gemäß [erstellen, die ein Formular mithilfe des InfoPath 2003-Objekts verwendet Modell](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), in der Standardeinstellung Microsoft InfoPath verwendet eine Teilmenge der Objekte und Member vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellt, identisch mit denen von InfoPath 2003 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92313-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="92313-106">Dies erfolgt, um Kompatibilität mit InfoPath 2003 bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="92313-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="92313-107">Das vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellten Objektmodell enthält jedoch zusätzliche Objekte und Elemente, die neuen Funktionen bereitstellen, der die Office InfoPath 2007 und InfoPath hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="92313-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="92313-108">Beispielsweise bieten die [Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) und [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) -Schnittstellen neue Informationen Rights Management Funktionalität, die in InfoPath 2003 nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="92313-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="92313-109">Beim Öffnen oder erstellen Sie die Formularvorlage mit verwaltetem Code mit InfoPath 2003-kompatible Objektmodell sind diese und andere neue Objekte, Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace hinzugefügt wurde nicht standardmäßig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92313-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="92313-110">Ähnlich wie, während die [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) -Schnittstelle bietet die gleiche Funktionalität wie InfoPath 2003; die Schnittstelle [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) wurde mit Versionsangabe Einbeziehung zusätzliche Eigenschaften und Methoden, die in Office InfoPath 2007 hinzugefügt wurden, und die [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) wurde mit Versionsangabe Einbeziehung zusätzliche Eigenschaften und Methoden, die in InfoPath hinzugefügt wurden .</span><span class="sxs-lookup"><span data-stu-id="92313-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="92313-111">Wenn Sie Objekte und Elemente, die in Office InfoPath 2007 hinzugefügt wurden verwenden möchten oder InfoPath in ein Formularvorlagenprojekt erstellt mithilfe des Objektmodells, das vom **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace bereitgestellt, können Sie jedoch Code dazu, die verwendet Dieser Member werden nicht mit InfoPath 2003 kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="92313-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="92313-112">Alle Formularvorlagen mit Geschäftslogik, die mit dem Objektmodell, das vom **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace bereitgestellt, ob sie oder nicht, Objekte und Member kompatibel mit InfoPath verwenden erstellt werden für nicht unterstützt. browserfähige Formularvorlagen für Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92313-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="92313-113">Geschäftslogik für browserfähige Formularvorlagen muss das neue InfoPath verwaltetem Code Objektmodell des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="92313-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="92313-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="92313-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="92313-115">Erstellen einer XDocument- oder Anwendungsobjektvariablen zum Zugreifen auf neue Objektmodellmember</span><span class="sxs-lookup"><span data-stu-id="92313-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="92313-116">Zugriff auf die neuen Objekte und Elemente, die in der **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace zur Verfügung stehen, müssen Sie deklarieren und Objektvariablen auf die richtige Version der Schnittstelle, die diese Member implementiert umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="92313-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="92313-117">Standardmäßig die `thisXDocument` und `thisApplication` Variablen zugreifen, die InfoPath 2003-kompatible Versionen der entsprechenden **_XDocument2** und [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="92313-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="92313-118">Zugriff auf die **_XDocument3** und [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) Schnittstellen, die Zugriff auf die neue Funktionalität bereitstellen müssen Sie deklarieren Sie eine Objektvariable des Typs **_XDocument3** oder **_Application3** , und klicken Sie dann das von der `thisXDocument`oder `thisApplication` Variable auf den gleichen Typ wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="92313-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="92313-119">Zugreifen auf ein neues Objekt von der XDocument- oder Anwendungsobjektvariable aus mithilfe einer Accessoreigenschaft</span><span class="sxs-lookup"><span data-stu-id="92313-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="92313-120">Nachdem Sie eine Variable, die spätere Version _ **XDocument3** oder **_Application3** Typ erstellt haben, können Sie es verwenden, greifen Sie auf ein Objekt oder Element, das neuen InfoPath-Funktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="92313-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="92313-121">Das folgende Beispiel zeigt, wie Sie eine Objektvariable vom Typ _ **XDocument3** mit der [Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) Accessor-Eigenschaft zum Zugriff auf die neue **Berechtigung** -Schnittstelle und dessen [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) -Eigenschaft, um festzustellen, ob berechtigungseinstellungen sind für das Formular aktiviert.</span><span class="sxs-lookup"><span data-stu-id="92313-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="92313-122">Zugreifen auf ein Versionsobjekt und Umwandeln in den Versionstyp</span><span class="sxs-lookup"><span data-stu-id="92313-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="92313-123">Wenn einem Objekt, das im InfoPath 2003-Objektmodell vorhanden war, neue Eigenschaften oder Methoden hinzugefügt werden, hat das Objekt, das diese neuen Member implementiert, einen Versionsnamen.</span><span class="sxs-lookup"><span data-stu-id="92313-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="92313-124">Das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) -Objekt stellt beispielsweise keinen Zugriff auf zwei neue Eigenschaften, die nur verfügbar sind, wenn Sie die [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) -Versionsobjekt verwenden: die Eigenschaften [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) und [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="92313-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="92313-125">Um diese Eigenschaften zuzugreifen, müssen Sie deklarieren Sie eine Objektvariable vom Typ **ViewInfo2** und wandeln Sie das Objekt, das durch die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) -Eigenschaft der Objektvariablen _ **XDocument3** den **ViewInfo2** -Typ zurückgegeben, wie im folgenden Beispiel Beispiel.</span><span class="sxs-lookup"><span data-stu-id="92313-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


