---
title: Verwenden von Microsoft. Office. Interop. InfoPath. SemiTrust-Membern, die nicht mit InfoPath kompatibel sind
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen mit InfoPath 2007-Features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Das vom Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace bereitgestellte Objektmodell enthält Objekte und Elemente, die neue Funktionalität bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurde.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415341"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Verwenden von Microsoft. Office. Interop. InfoPath. SemiTrust-Membern, die nicht mit InfoPath kompatibel sind

Beim Hinzufügen von Code zu einer Formularvorlage, die mit dem Microsoft Office InfoPath 2003 Toolkit erstellt wurde, oder erstellen Sie eine neue Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet werden kann (siehe [Erstellen einer Formularvorlage mit dem infopath 2003-Objekt Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)) standardmäßig verwendet Microsoft InfoPath eine Teilmenge der vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellten Objekte und Member, die mit denen von InfoPath 2003 identisch sind. Dies dient der Kompatibilität mit InfoPath 2003. Das vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellte Objektmodell enthält jedoch zusätzliche Objekte und Elemente, die neue Funktionalität bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurde. 
  
Die PermissionObject- [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) und [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) -Schnittstellen bieten beispielsweise neue Funktionen zur Verwaltung von Informationsrechten, die in InfoPath 2003 nicht verfügbar sind. Dies und andere neue Objekte, die dem Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace hinzugefügt werden, sind nicht standardmäßig verfügbar, wenn Sie eine Formularvorlage mit InfoPath 2003-kompatiblen Objektmodell öffnen oder erstellen. 
  
Entsprechend stellt die [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) -Schnittstelle dieselbe Funktionalität wie InfoPath 2003 bereit. die [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) -Schnittstelle wurde so erweitert, dass Sie zusätzliche Eigenschaften und Methoden enthält, die in Office InfoPath 2007 hinzugefügt wurden, und die [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) wurde mit zusätzlichen Eigenschaften und Methoden erweitert, die in InfoPath hinzugefügt wurden. . 
  
Wenn Sie in einem Formularvorlagenprojekt, das mit dem vom **Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace bereitgestellten Objektmodell erstellt wurde, Objekte und Elemente verwenden möchten, die in Office InfoPath 2007 oder InfoPath hinzugefügt wurden, können Sie dies tun, aber Code, der Diese Member sind nicht mit InfoPath 2003 kompatibel. 
  
> [!NOTE]
> Alle Formularvorlagen mit Geschäftslogik, die mit dem vom **Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace bereitgestellten Objektmodell erstellt wurden, unabhängig davon, ob Sie Objekte und Member verwenden, die mit InfoPath kompatibel sind oder nicht, werden für browserfähige Formularvorlagen, die für Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt werden. Die Geschäftslogik für browserfähige Formularvorlagen muss das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt wird. 
  
## <a name="example"></a>Beispiel

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Erstellen einer XDocument- oder Anwendungsobjektvariablen zum Zugreifen auf neue Objektmodellmember

Damit Sie auf die neuen im **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace verfügbaren Objekte und Member zugreifen können, müssen Sie Objektvariablen deklarieren und in die richtige Version der Schnittstelle umwandeln, die diese Member implementiert. Standardmäßig greifen die `thisXDocument` und `thisApplication` -variablen auf die InfoPath 2003-kompatiblen Versionen der entsprechenden **_XDocument2** -und [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) -Schnittstellen zu. Für den Zugriff auf die **_XDocument3** -und [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) -Schnittstellen, die den Zugriff auf neue Funktionen ermöglichen, müssen Sie eine Objektvariable des **_XDocument3** -oder **_Application3** -Typs deklarieren und dann das von der `thisXDocument`oder `thisApplication` Variable auf den gleichen Typ, wie in den folgenden Beispielen gezeigt. 
  
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

Nachdem Sie eine Variable mit der höheren **XDocument3** -oder **_Application3** -Typ-Version erstellt haben, können Sie Sie für den Zugriff auf ein Objekt oder einen Member verwenden, das neue InfoPath-Funktionen bereitstellt. 
  
Das folgende Beispiel zeigt, wie Sie eine Objektvariable vom Typ _ **XDocument3** mit der [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) -Accessor-Eigenschaft für den Zugriff auf die neue **Permission** -Schnittstelle und Ihre [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) -Eigenschaft verwenden, um zu bestimmen, ob Berechtigungseinstellungen für das Formular aktiviert. 
  
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
  
Das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) -Objekt bietet beispielsweise keinen Zugriff auf zwei neue Eigenschaften, die nur verfügbar sind, wenn das [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) -Objekt mit Versionsverwaltung verwendet wird: die Eigenschaften [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) und [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Für den Zugriff auf diese Eigenschaften müssen Sie eine Objektvariable vom Typ **ViewInfo2** deklarieren und das von der ViewInfos [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) -Eigenschaft der _ **XDocument3** -Objektvariable zurückgegebene Objekt in den **ViewInfo2** -Typ umwandeln, wie im folgenden dargestellt. Beispiel. 
  
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


