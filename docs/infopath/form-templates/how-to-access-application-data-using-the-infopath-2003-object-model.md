---
title: Zugreifen auf Anwendungsdaten mithilfe des InfoPath-2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [InfoPath 2007], Zugriff auf Daten mithilfe des 2003-Objektmodells, InfoPath 2003-kompatible Formularvorlagen, zugreifen auf Anwendungsdaten
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten kann über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen werden, die mithilfe der Anwendungsschnittstelle instanziiert wird.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437441"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Zugreifen auf Anwendungsdaten mithilfe des InfoPath-2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten kann über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen werden, die mithilfe der [Anwendungs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Schnittstelle instanziiert wird. 
  
Ein InfoPath 2003-kompatibles Formularvorlagenprojekt mit verwaltetem Code, das mithilfe von `thisApplication` Visual Studio 2012 `_Startup` erstellt wurde, initialisiert die Variable in der Methode der Formularcodeklasse, die für den Zugriff auf die Member der [Anwendungs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Schnittstelle verwendet werden kann. Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Anwendungs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Schnittstelle verwendet, um den Namen und die Versionsnummer der laufenden Instanz von InfoPath zurückzugeben. Diese Informationen werden in einem Meldungsfeld mithilfe der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) -Schnittstelle angezeigt. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

Im Visual C#-Beispiel wird der Verweis auf das `\n` Zeichen in der Zeichenfolge für die Warnmeldung von InfoPath nicht verwaltetem Code als standardmäßiger neuer Linien-Feed gerendert, der dazu führt, dass der Text unterbrochen wird und in einer neuen Zeile im Meldungsfeld angezeigt wird. Um explizit den neuen Zeilenwert zu verwenden, der für die aktuelle Umgebung und Plattform definiert wurde, sollten Sie die **Environment.NewLine**-Eigenschaft verwenden, wie dies im folgenden Beispiel dargestellt ist. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars

Entwickler können die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle verwenden, um Zugriff auf Informationen zum zugrunde LIEGENden XML-Dokument eines Formulars zu erhalten, einschließlich eines Verweises auf ein XML-DOM (Document Object Model), das die XML-Quelldaten des Formulars enthält. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die von der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle verfügbar sind, beispielsweise ob das zugrunde liegende XML-Dokument geändert wurde (mithilfe der IsDirty-Eigenschaft) und ob es [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) digital signiert (mit der [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) IsSigned-Eigenschaft). Das nächste Meldungsfeld verwendet die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) -Eigenschaft der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle, um die Quell-XML des dem Formular zuGRUNDe liegenden XML-Dokuments anzuzeigen. 
  
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

Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf die darin enthaltenen Quell-XML-Daten, können auch über die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle aufgerufen werden. Auf diese Informationen wird mithilfe der [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) -Eigenschaft zugegriffen, die einen Verweis auf [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) die SolutionObject-Schnittstelle zurückgibt. 
  
Im folgenden Beispiel zeigt die erste Warnung einige der Daten an, die über die SolutionObject- [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) Schnittstelle verfügbar sind, beispielsWEISE den URI-Speicherort (Uniform Resource Identifier) (mithilfe der [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) -Eigenschaft) und die Versionsnummer (mithilfe der [ Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) -Eigenschaft). Die nächste Warnung verwendet die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) -Eigenschaft der [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle, um die Quell-XML der XSF-Datei anzuzeigen. 
  
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


