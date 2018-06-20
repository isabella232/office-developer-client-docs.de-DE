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
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Verwenden Sie nicht kompatibel mit InfoPath Microsoft.Office.Interop.InfoPath.SemiTrust-Elemente

Beim Hinzufügen von Code zu einer Formularvorlage, die mit dem Microsoft Office InfoPath 2003 Toolkit erstellt wurde, oder erstellen eine neue Formularvorlage, die mit dem InfoPath 2003-kompatible Objektmodell (gemäß [erstellen, die ein Formular mithilfe des InfoPath 2003-Objekts verwendet Modell](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), in der Standardeinstellung Microsoft InfoPath verwendet eine Teilmenge der Objekte und Member vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellt, identisch mit denen von InfoPath 2003 verwendet werden. Dies erfolgt, um Kompatibilität mit InfoPath 2003 bereitzustellen. Das vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellten Objektmodell enthält jedoch zusätzliche Objekte und Elemente, die neuen Funktionen bereitstellen, der die Office InfoPath 2007 und InfoPath hinzugefügt wurde. 
  
Beispielsweise bieten die [Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) und [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) -Schnittstellen neue Informationen Rights Management Funktionalität, die in InfoPath 2003 nicht verfügbar ist. Beim Öffnen oder erstellen Sie die Formularvorlage mit verwaltetem Code mit InfoPath 2003-kompatible Objektmodell sind diese und andere neue Objekte, Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace hinzugefügt wurde nicht standardmäßig verfügbar. 
  
Ähnlich wie, während die [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) -Schnittstelle bietet die gleiche Funktionalität wie InfoPath 2003; die Schnittstelle [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) wurde mit Versionsangabe Einbeziehung zusätzliche Eigenschaften und Methoden, die in Office InfoPath 2007 hinzugefügt wurden, und die [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) wurde mit Versionsangabe Einbeziehung zusätzliche Eigenschaften und Methoden, die in InfoPath hinzugefügt wurden . 
  
Wenn Sie Objekte und Elemente, die in Office InfoPath 2007 hinzugefügt wurden verwenden möchten oder InfoPath in ein Formularvorlagenprojekt erstellt mithilfe des Objektmodells, das vom **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace bereitgestellt, können Sie jedoch Code dazu, die verwendet Dieser Member werden nicht mit InfoPath 2003 kompatibel sein. 
  
> [!NOTE]
> Alle Formularvorlagen mit Geschäftslogik, die mit dem Objektmodell, das vom **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace bereitgestellt, ob sie oder nicht, Objekte und Member kompatibel mit InfoPath verwenden erstellt werden für nicht unterstützt. browserfähige Formularvorlagen für Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt. Geschäftslogik für browserfähige Formularvorlagen muss das neue InfoPath verwaltetem Code Objektmodell des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace verwenden. 
  
## <a name="example"></a>Beispiel

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Erstellen einer XDocument- oder Anwendungsobjektvariablen zum Zugreifen auf neue Objektmodellmember

Zugriff auf die neuen Objekte und Elemente, die in der **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace zur Verfügung stehen, müssen Sie deklarieren und Objektvariablen auf die richtige Version der Schnittstelle, die diese Member implementiert umgewandelt. Standardmäßig die `thisXDocument` und `thisApplication` Variablen zugreifen, die InfoPath 2003-kompatible Versionen der entsprechenden **_XDocument2** und [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) Schnittstellen. Zugriff auf die **_XDocument3** und [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) Schnittstellen, die Zugriff auf die neue Funktionalität bereitstellen müssen Sie deklarieren Sie eine Objektvariable des Typs **_XDocument3** oder **_Application3** , und klicken Sie dann das von der `thisXDocument`oder `thisApplication` Variable auf den gleichen Typ wie in den folgenden Beispielen gezeigt. 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Zugreifen auf ein neues Objekt von der XDocument- oder Anwendungsobjektvariable aus mithilfe einer Accessoreigenschaft

Nachdem Sie eine Variable, die spätere Version _ **XDocument3** oder **_Application3** Typ erstellt haben, können Sie es verwenden, greifen Sie auf ein Objekt oder Element, das neuen InfoPath-Funktionen bereitstellt. 
  
Das folgende Beispiel zeigt, wie Sie eine Objektvariable vom Typ _ **XDocument3** mit der [Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) Accessor-Eigenschaft zum Zugriff auf die neue **Berechtigung** -Schnittstelle und dessen [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) -Eigenschaft, um festzustellen, ob berechtigungseinstellungen sind für das Formular aktiviert. 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Zugreifen auf ein Versionsobjekt und Umwandeln in den Versionstyp

Wenn einem Objekt, das im InfoPath 2003-Objektmodell vorhanden war, neue Eigenschaften oder Methoden hinzugefügt werden, hat das Objekt, das diese neuen Member implementiert, einen Versionsnamen.
  
Das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) -Objekt stellt beispielsweise keinen Zugriff auf zwei neue Eigenschaften, die nur verfügbar sind, wenn Sie die [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) -Versionsobjekt verwenden: die Eigenschaften [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) und [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Um diese Eigenschaften zuzugreifen, müssen Sie deklarieren Sie eine Objektvariable vom Typ **ViewInfo2** und wandeln Sie das Objekt, das durch die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) -Eigenschaft der Objektvariablen _ **XDocument3** den **ViewInfo2** -Typ zurückgegeben, wie im folgenden Beispiel Beispiel. 
  
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


