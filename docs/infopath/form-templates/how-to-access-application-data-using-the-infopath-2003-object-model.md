---
title: Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], Zugreifen auf Daten mithilfe des 2003-Objektmodells,InfoPath 2003-kompatible Formularvorlagen, Zugreifen auf Anwendungsdaten
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der Application-Schnittstelle instanziiert wird.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437441"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Schnittstelle instanziiert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) wird. 
  
Ein infoPath 2003-kompatibles Formularvorlagenprojekt für verwalteten Code, das mit Visual Studio 2012 erstellt wurde, initialisiert die Variable in der Methode der `thisApplication` `_Startup` Formularcodeklasse, [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) die für den Zugriff auf die Elemente der Anwendungsschnittstelle verwendet werden kann. Im folgenden Beispiel werden die [Eigenschaften Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Application-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurück zu geben. Diese Informationen werden mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UI2-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) in einem Meldungsfeld angezeigt. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

Im Visual C#-Beispiel wird der Verweis auf das Zeichen in der Zeichenfolge für die Warnungsnachricht von InfoPath ohne verwalteten Code als standardneuer Zeilenfeed gerendert, der bewirkt, dass der Text umbricht und in einer neuen Zeile im Meldungsfeld platziert  `\n` wird. Um explizit den neuen Zeilenwert zu verwenden, der für die aktuelle Umgebung und Plattform definiert wurde, sollten Sie die **Environment.NewLine**-Eigenschaft verwenden, wie dies im folgenden Beispiel dargestellt ist. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars

Entwickler können die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwenden, um Zugriff auf Informationen zum einem Formular zugrunde liegenden XML-Dokument zu erhalten, einschließlich eines Verweises auf ein XML Document Object Model (DOM), das die Quell-XML-Daten des Formulars enthält. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verfügbar sind, z. B. ob das zugrunde liegende XML-Dokument geändert wurde (mithilfe der [IsDirty-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) und ob es digital signiert wurde (mithilfe der [IsSigned-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) Im nächsten Meldungsfeld wird die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) verwendet, um die Quell-XML des dem Formular zugrunde liegenden XML-Dokuments zu zeigen. 
  
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

Auf Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf die in diesem Formular gespeicherten Quell-XML-Daten, kann auch über die [XDocument-Schnittstelle zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) werden. Auf diese Informationen wird mithilfe der [Solution-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) zugegriffen, die einen Verweis auf die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) zurückgibt. 
  
Im folgenden Beispiel zeigt die erste Warnung einige der Daten an, die über die [SolutionObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) verfügbar sind, z. B. den Speicherort des URI (Uniform Resource Identifier) (mithilfe der [URI-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) und dessen Versionsnummer (mithilfe der [Version-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) Die nächste Warnung verwendet die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) der [SolutionObject-Schnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) um die Quell-XML der XSF-Datei zu zeigen. 
  
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


