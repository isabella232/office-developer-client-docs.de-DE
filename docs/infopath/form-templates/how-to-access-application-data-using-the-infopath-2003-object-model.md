---
title: Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], Zugreifen auf Daten mithilfe des 2003-Objektmodells, InfoPath 2003-kompatible Formularvorlagen, Zugreifen auf Anwendungsdaten
ms.localizationpriority: medium
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der Application-Schnittstelle instanziiert wird.
ms.openlocfilehash: 006ae3d7d00f7137fd0acd521ed66731a8d73417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631352"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) instanziiert wird. 
  
Ein InfoPath 2003-kompatibles Formularvorlagenprojekt mit verwaltetem Code, das mit Visual Studio 2012 erstellt wurde, initialisiert die `thisApplication` Variable in der Methode der `_Startup` Formularcodeklasse, die für den Zugriff auf die Member der [Application-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) verwendet werden kann. Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Application-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurückzugeben. Diese Informationen werden mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UI2-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) in einem Meldungsfeld angezeigt. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

Im Visual C#-Beispiel wird der Verweis auf das  `\n` Zeichen in der Zeichenfolge für die Warnmeldung von nicht verwaltetem InfoPath-Code als standardmäßiger neuer Zeilenvorschub gerendert, der bewirkt, dass der Text umbricht und in einer neuen Zeile im Meldungsfeld platziert wird. Um explizit den neuen Zeilenwert zu verwenden, der für die aktuelle Umgebung und Plattform definiert wurde, sollten Sie die **Environment.NewLine**-Eigenschaft verwenden, wie dies im folgenden Beispiel dargestellt ist. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars

Entwickler können die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwenden, um Zugriff auf Informationen zu dem einem Formular zugrunde liegenden XML-Dokument zu erhalten, einschließlich eines Verweises auf ein XML-DOM (Document Object Model), das die XML-Quelldaten des Formulars enthält. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verfügbar sind, z. B. ob das zugrunde liegende XML-Dokument geändert wurde (mithilfe der [IsDirty-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) und ob es digital signiert wurde (mithilfe der [IsSigned-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) Im nächsten Meldungsfeld wird die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwendet, um die Quell-XML des dem Formular zugrunde liegenden XML-Dokuments anzuzeigen. 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

Die **xml**-Eigenschaft, die im vorangegangenen Beispiel verwendet wurde, ist eine Eigenschaft des XML-DOM (Document Object Model). Weitere Informationen zum XML-DOM finden Sie in der Dokumentation zum MSXML 5.0-SDK. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Zugreifen auf Daten aus der Formulardefinitionsdatei eines Formulars

Auf Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf die enthaltenen XML-Quelldaten, kann auch über die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) zugegriffen werden. Auf diese Informationen wird mithilfe der [Solution-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) zugegriffen, die einen Verweis auf die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) zurückgibt. 
  
Im folgenden Beispiel zeigt die erste Warnung einige der Daten an, die über die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) verfügbar sind, z. B. den Speicherort des Uniform Resource Identifier (URI) (unter Verwendung der [URI-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) und die Versionsnummer (mithilfe der [Version-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) Die nächste Warnung verwendet die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) der [SolutionObject-Schnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) um die XML-Quelldatei der XSF-Datei anzuzeigen. 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


