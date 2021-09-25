---
title: Informationen zur Microsoft Office InfoPath Primary Interop-Assembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, primary interop assembly,InfoPath primary interop assembly,PIAs [InfoPath 2007],primary interop assemblies [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Um die Erstellung von InfoPath-Lösungen zu unterstützen, die Sprachen mit verwaltetem Code wie Visual C# und Visual Basic verwenden, installiert die Option .NET Programmability Support im InfoPath-Setupprogramm drei Interopassemblys.
ms.openlocfilehash: 659297635627cbf4d7a80c5d0dae7a9bd25ce980
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552136"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Informationen zur Microsoft Office InfoPath Primary Interop-Assembly

Die InfoPath-Anwendung wird als COM-Anwendung (Component Object Model) erstellt, die ihre Programmierschnittstellen für die externe Automatisierung als COM-Schnittstellen verfügbar macht. Zur Unterstützung der Erstellung von InfoPath-Lösungen, die Sprachen mit verwaltetem Code wie Visual C# und Visual Basic verwenden, installiert die **Option .NET Programmability Support** im InfoPath-Setupprogramm drei Interopassemblys. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
In diesem Thema wird das über Microsoft verfügbar gemachte Objektmodell erläutert. Office.Interop.InfoPath-Interopassembly, die ausschließlich für externen Automatisierungscode verwendet wird. Informationen zu Microsoft. Office.Interop.InfoPath.SemiTrust-Assembly, die ausschließlich zum Schreiben und Ausführen von verwaltetem Code verwendet wird, der in InfoPath-Formularvorlagen (XSN) ausgeführt wird, siehe [InfoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Wichtige Informationen zur Installation

Die Standardinstallationsoption des InfoPath-Setupprogramms installiert Microsoft. Office.Interop.InfoPath-Assembly im globalen Assemblycache (Global Assembly Cache, GAC), dessen Inhalt im Ordner "C:\Windows\Assembly" angezeigt werden kann (oder in "C:\Windows\assembly\GAC_MSIL" beim direkten Anzeigen des Dateisystems). Diese Assembly wird als "Microsoft Office primäre Interopassembly von InfoPath" bezeichnet und wird häufig in Verbindung mit der Microsoft.Office.Interop.InfoPath.Xml assembly verwendet, die auch im GAC installiert ist, um die InfoPath-Anwendung aus externen Anwendungen zu automatisieren, die verwalteten Code verwenden. Informationen zur Microsoft.Office.Interop.InfoPath.Xml Assembly finden Sie unter [InfoPath XML Interop Assembly](about-the-infopath-xml-interop-assembly.md).
  
Wenn microsoft. Office.Interop.InfoPath-Assembly im GAC nicht sichtbar ist, sollten Sie bestätigen, dass InfoPath ordnungsgemäß installiert wurde. Standardmäßig ist die **Option .NET Programmierbarkeitsunterstützung** im Setupprogramm auf **"Von meinem Computer ausführen"** festgelegt, solange die .NET Framework 1.1 Redistributable, .NET Framework 1.1 Software Development Kit (SDK) oder eine höhere Version des .NET Framework installiert ist, bevor das Setup ausgeführt wird. Wenn diese Interopassemblys auf Dem Computer nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1.1 oder höher installiert ist, und dann **Programme und Features** aus der **Systemsteuerung** verwenden, um das Setup zu ändern, indem Sie die **Option .NET Programmability Support** unter Microsoft Office **InfoPath** auf **"Von meinem Computer ausführen"** festlegen.
  
Informationen zum Herunterladen der .NET Framework 1.1 Redistributable finden Sie unter [.NET Framework 1.1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>The Microsoft. Office.Interop.InfoPath-Namespace

Obwohl das Schreiben von verwaltetem Code für eine bestimmte Aufgabe der Ausführung derselben Aufgabe mit einer Sprache wie Visual Basic for Applications oder JScript sehr ähnlich ist, sieht das Objektmodell, das beim Anzeigen des **Microsoft.Office.Interop.InfoPath-Namespace** im **Objektkatalog** in Microsoft Visual Studio verfügbar gemacht wird, komplexer aus. Dies liegt daran, dass die Interoperabilität mit dem .NET Framework einen COM-Server erfordert, um alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte verfügbar zu machen, die vom .NET Framework selbst benötigt werden. Weitere Informationen dazu, wie und warum das von einer Interopassembly verfügbar gemachte Objektmodell komplexer erscheint, finden Sie im Abschnitt "So werden COM-Objekte für verwalteten Code verfügbar gemacht" im Thema ["InfoPath 2003 Compatible Object Models".](../form-templates/infopath-2003-compatible-object-models.md) 
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

In den Beispielen in diesem Abschnitt wird davon ausgegangen, dass Sie Verweise auf Microsoft eingerichtet haben. Office.Interop.InfoPath und Microsoft.Office.Interop.InfoPath.Xml Assemblys. Informationen zum Festlegen von Verweisen und zusätzlichen Beispielen für die externe Automatisierung finden Sie unter ["Szenarien und Beispiele für externe Automatisierung".](external-automation-scenarios-and-examples.md)
  
Bevor Sie den Abschluss der Microsoft IntelliSense-Anweisung in externem Automatisierungscode verwenden können, müssen Sie eine Objektvariable für eine Instanz der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) erstellen, wie in der folgenden Codezeile dargestellt. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Wenn Sie nach dem Erstellen der Objektvariablen den Variablennamen gefolgt von einem Punkt eingeben, wird eine Dropdownliste mit mitgliedern der auszuwählenden **Application-Klasse** angezeigt. 
  
Um mit einem InfoPath-Formular zu arbeiten, deklarieren Sie eine Objektvariable vom Typ [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) und initialisieren Sie sie, indem Sie das Formular aus der [XDocuments-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) der Application-Objektvariablen öffnen, wie in der folgenden Codezeile dargestellt.  
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

Die Dropdownliste zum Abschluss der IntelliSense-Anweisung für Member der **XDocument-Klasse** wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Punkt eingeben. 
  
Zum Arbeiten mit dem Inhalt des zugrunde liegenden XML-Dokuments für das Formular mit Microsoft XML Core Services (MSXML) müssen Sie eine Variable vom Typ [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) erstellen und dann die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) der **XDocument-Klasse** verwenden, um der Variablen das XML-Dom (Document Object Model) des Formulars zuzuweisen. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Die Dropdownliste zum Abschluss der IntelliSense-Anweisung für Member der **IXMLDOMDocument2-Klasse** wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Punkt eingeben, mit dem Sie MSXML verwenden können, um mit dem XML-Dokument zu arbeiten. 
  
### <a name="using-the-class-library-reference-documentation"></a>Verwenden der Referenzdokumentation der Klassenbibliothek

Die Organisation der Referenzdokumentation der [Microsoft.Office.Interop.InfoPath-Namespace-Klassenbibliothek](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) spiegelt die Beziehungen zwischen coclass-Schnittstellen und den geerbten Schnittstellen wider, die sie implementieren. 
  
Wenn Sie ein Thema für eine Coclass-Schnittstelle öffnen, z. B. [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) zeigt der Link zu den Mitgliedern der Coclass-Schnittstelle nach der Beschreibung der Schnittstelle am Anfang des Themas ein leeres Thema an. Sie müssen zum Anzeigen der Liste mit Membern, die von der Coklassen-Schnittstelle implementiert werden, das Thema für die aktuellste Schnittstelle öffnen, die von der Coklasse geerbt wird, und dann die Tabelle ihrer Member öffnen. Sie finden einen Link zu der geerbten Schnittstelle am Anfang des Themas zur Coklassen-Schnittstelle im Abschnitt "Hinweise". 
  
Wenn Sie F1 im Visual Studio Code Editor drücken, ist das Verhalten ähnlich, mit der Ausnahme, dass das Element, für das Sie die F1-Hilfe aufrufen, direkt angezeigt wird, da Sie in der Regel mit Membern einer Schnittstelle arbeiten. Dennoch kann die Tatsache, dass ein Member von einer versionsspezifischen Schnittstelle implementiert werden kann, zunächst verwirrend erscheinen. Wenn Sie z. B. den Cursor eingeben  `myXDocument.UI.Alert` und platzieren  `Alert` und F1 drücken, lautet das Thema "UI2". Alert-Methode" wird angezeigt. Dies ist der Fall, da die **Alert**-Methode eine Implementierung eines Members der **UI2**-Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an InfoPath-Objektmodellmember

Wenn ein InfoPath-Objektmodellmember einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie das Feld **Type.Missing** für diesen Parameter übergeben. Wenn das **Type.Missing**-Feld nicht angegeben wird und ein tatsächlicher Wert ausgelassen wird, führt dies zu einem Buildfehler. Dies gilt für Code, der sowohl in C# als auch in Visual Basic geschrieben wurde. Die [SelectNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) der [ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) enthält beispielsweise zwei optionale Parameter: _varEndNode_ und _varViewContext._ Eine Codezeile, in der keine tatsächlichen Werte für diese optionalen Parameter angegeben sind, sollte wie in den folgenden Beispielen dargestellt aussehen.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Siehe auch

- [Szenarien für die externe Automatisierung und Beispiele](external-automation-scenarios-and-examples.md)

