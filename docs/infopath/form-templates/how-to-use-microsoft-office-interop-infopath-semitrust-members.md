---
title: Verwenden Sie Microsoft. Office.Interop.InfoPath.SemiTrust-Member sind nicht mit InfoPath kompatibel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen mit infopath 2007-Features
ms.localizationpriority: medium
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Das von Microsoft bereitgestellte Objektmodell. Office.Interop.InfoPath.SemiTrust-Namespace enthält Objekte und Member, die neue Funktionen bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurden.
ms.openlocfilehash: f4986a89a07295014aae9e29797ddb0fe1bc94af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584878"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Verwenden Sie Microsoft. Office.Interop.InfoPath.SemiTrust-Member sind nicht mit InfoPath kompatibel

Wenn Sie einer Formularvorlage, die mit dem Microsoft Office InfoPath 2003-Toolkit erstellt wurde, Code hinzufügen oder eine neue Formularvorlage erstellen, die mit dem InfoPath 2003-kompatiblen Objektmodell funktioniert (wie unter [Erstellen einer Formularvorlage mithilfe des InfoPath 2003-Objektmodells](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)beschrieben), gilt Folgendes: Microsoft InfoPath verwendet eine Teilmenge der Vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellten Objekte und Elemente, die mit denen von InfoPath 2003 identisch sind. Dies dient der Kompatibilität mit InfoPath 2003. Das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellte Objektmodell enthält jedoch zusätzliche Objekte und Member, die neue Funktionen bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurden. 
  
Beispielsweise stellen die [PermissionObject-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) und [Permission-Schnittstellen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) neue Funktionen zur Verwaltung von Informationsrechten bereit, die in InfoPath 2003 nicht verfügbar sind. Dies und andere neue Objekte, die microsoft hinzugefügt wurden. Office.Interop.InfoPath.SemiTrust-Namespace ist nicht standardmäßig verfügbar, wenn Sie eine Formularvorlage mit verwaltetem Code mit infoPath 2003-kompatiblem Objektmodell öffnen oder erstellen. 
  
Auf ähnliche Weise bietet die [_XDocument2-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) die gleiche Funktionalität wie InfoPath 2003. Die [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) Schnittstelle wurde mit einer Version versehen, um zusätzliche Eigenschaften und Methoden einzuschließen, die in Office InfoPath 2007 hinzugefügt wurden, und die [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) wurde so aktualisiert, dass sie zusätzliche Eigenschaften und Methoden enthält, die in InfoPath hinzugefügt wurden. 
  
Wenn Sie Objekte und Member verwenden möchten, die in Office InfoPath 2007 oder InfoPath in einem Formularvorlagenprojekt hinzugefügt wurden, das mithilfe des vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellten Objektmodells erstellt wurde, können Sie dies tun, aber Code, der diese Member verwendet, ist nicht mit InfoPath 2003 kompatibel. 
  
> [!NOTE]
> Alle Formularvorlagen mit Geschäftslogik, die mithilfe des vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellten Objektmodells erstellt wurden, unabhängig davon, ob sie Objekte und Elemente verwenden, die mit InfoPath kompatibel sind oder nicht, werden für browserfähige Formularvorlagen, die in Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt werden, nicht unterstützt. Geschäftslogik für browserfähige Formularvorlagen muss das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, das von [Microsoft.Office bereitgestellt wird. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
## <a name="example"></a>Beispiel

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Erstellen einer XDocument- oder Anwendungsobjektvariablen zum Zugreifen auf neue Objektmodellmember

Damit Sie auf die neuen im **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace verfügbaren Objekte und Member zugreifen können, müssen Sie Objektvariablen deklarieren und in die richtige Version der Schnittstelle umwandeln, die diese Member implementiert. Standardmäßig greifen die Variablen und variablen  `thisXDocument`  `thisApplication` auf die InfoPath 2003-kompatiblen Versionen der entsprechenden **_XDocument2-** und [_Application2 schnittstellen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) zu. Um auf die **_XDocument3** und [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) Schnittstellen zuzugreifen, die Zugriff auf neue Funktionen bieten, müssen Sie eine Objektvariable des **Typs _XDocument3** oder **_Application3** deklarieren und dann das von der oder der Variablen zurückgegebene Objekt in den gleichen  `thisXDocument` Typ  `thisApplication` umwandeln, wie in den folgenden Beispielen gezeigt. 
  
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

Nachdem Sie eine Variable der neueren Version _ **XDocument3** oder **_Application3** Erstellt haben, können Sie damit auf ein Objekt oder Element zugreifen, das neue InfoPath-Funktionen bereitstellt. 
  
Das folgende Beispiel zeigt, wie Sie eine Objektvariable vom Typ _ **XDocument3** mit der [Permission-Accessoreigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) verwenden, um auf die neue **Permission-Schnittstelle** und deren [Enabled-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) zuzugreifen, um zu bestimmen, ob Berechtigungseinstellungen für das Formular aktiviert sind. 
  
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
  
Beispielsweise bietet das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) -Objekt keinen Zugriff auf zwei neue Eigenschaften, die nur verfügbar sind, wenn das [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) -Objekt mit Versionsangabe verwendet wird: die [Caption-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) und [HideName-Eigenschaft.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) 
  
Um auf diese Eigenschaften zuzugreifen, müssen Sie eine Objektvariable vom Typ **ViewInfo2** deklarieren und das von der [ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) der _ **XDocument3-Objektvariable zurückgegebene** Objekt in den **ViewInfo2-Typ** umwandeln, wie im folgenden Beispiel gezeigt. 
  
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


