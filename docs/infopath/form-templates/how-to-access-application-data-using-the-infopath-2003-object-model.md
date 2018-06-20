---
title: Access-Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [Infopath 2007], den Zugriff auf Daten mithilfe von InfoPath 2003-kompatible Formularvorlagen, zugreifen auf Anwendungsdaten 2003-Objektmodells
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Das InfoPath 2003-kompatible Objektmodell bietet Objekte und Sammlungen, die den Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen zu einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF) verwendet werden können. Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der Benutzeroberfläche der Anwendung instanziiert wird.
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790720"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Access-Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell bietet Objekte und Sammlungen, die den Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen zu einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF) verwendet werden können. Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der Benutzeroberfläche der [Anwendung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) instanziiert wird. 
  
Initialisiert eine InfoPath 2003-kompatible verwaltetem Code Formularvorlagenprojekt mit Visual Studio 2012 erstellt die `thisApplication` Variablen in der `_Startup` -Methode des die Formularklasse Code, die den Zugriff auf Member der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle verwendet werden kann. Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle zum Zurückgeben der Anzahl Name und Version der ausgeführten Instanz von InfoPath verwendet. Diese Informationen werden mithilfe der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [Anwenderschnittstelle: 2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) -Schnittstelle in einem Meldungsfeld angezeigt. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

In Visual C#-Beispiel, den Verweis auf die `\n` Zeichen in der Zeichenfolge für die Benachrichtigung an gerendert wird, indem InfoPath nicht verwalteter Code als Standard neu line Feed, der bewirkt, dass den Text zu unterbrechen und in einer neuen Zeile im Meldungsfeld platziert werden. Wenn den neue Wert für den aktuellen Umgebung und Plattform definierten explizit verwenden möchten, verwenden Sie die **Environment.NewLine** -Eigenschaft stattdessen wie im folgenden Beispiel gezeigt. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Zugreifen auf Daten aus dem zugrunde liegenden XML-Dokument eines Formulars

Entwickler können die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle verwenden, Zugriff auf Informationen zu einem Formular zugrunde liegenden XML-Dokument, einschließlich eines Verweises auf eine XML-DOM Document Object Model (), die den XML-Quelldaten des Formulars enthält. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten, die von der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle wie gibt an, ob das zugrunde liegende XML-Dokument (mithilfe der [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) -Eigenschaft) geändert wurde und ob er wurde verfügbar ist digital signiert (mithilfe der [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) -Eigenschaft). Das nächste Meldungsfeld verwendet die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle [DOM-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) Eigenschaft, um die Quell-XML-Daten des dem Formular zugrunde liegenden XML-Dokument anzuzeigen. 
  
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

Die **Xml** -Eigenschaft verwendet, die im vorherigen Beispiel ist eine Eigenschaft der das XML-Objektmodell (DOM). Weitere Informationen zum XML-DOM finden Sie unter der MSXML 5.0 SDK-Dokumentation. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Zugreifen auf Daten aus der Formulardefinitionsdatei eines Formulars

Informationen zur XSF-Datei eines Formulars, einschließlich eines XML-DOM-Verweises auf den XML-Quelldaten, die er enthält, kann auch über die [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle zugegriffen werden. Diese Informationen erfolgt mithilfe der [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) -Eigenschaft, die einen Verweis auf das [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle zurückgibt. 
  
Im folgenden Beispiel zeigt der erste Hinweis einige der Daten, die über die [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle, wie etwa den Uniform Resource Identifier (URI)-Speicherort (mithilfe der [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) -Eigenschaft) und die Versionsnummer (mithilfe der [verfügbar ist Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) Eigenschaft). Der nächste Hinweis verwendet die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) -Eigenschaft der [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) -Schnittstelle, um die Quell-XML-Code der XSF-Datei anzuzeigen. 
  
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


