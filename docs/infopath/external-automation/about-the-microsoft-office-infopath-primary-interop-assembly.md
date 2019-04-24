---
title: Informationen zur Microsoft Office InfoPath Primary Interop-Assembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, primäre Interop-Assembly, InfoPath Primary Interop Assembly, PIAs [InfoPath 2007], Primary Interop Assemblies [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Zur Unterstützung der Erstellung von InfoPath-Lösungen, die Sprachen mit verwaltetem Code verwenden, wie beispielsweise Visual C# und Visual Basic, werden in der .NET-Programmier Unterstützungs Option im InfoPath-Setupprogramm drei Interop-Assemblys installiert.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310136"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Informationen zur Microsoft Office InfoPath Primary Interop-Assembly

Die InfoPath-Anwendung wird als COM-Anwendung (Component Object Model) erstellt, die die Programmierschnittstellen für die externe Automatisierung als COM-Schnittstellen verfügbar macht. Zur Unterstützung der Erstellung von InfoPath-Lösungen, die Sprachen mit verwaltetem Code verwenden, wie beispielsweise Visual C# und Visual Basic, werden in der **.net-Programmier Unterstützungs** Option im InfoPath-Setupprogramm drei Interop-Assemblys installiert. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft. Office. Interop. InfoPath. dll
    
- Microsoft. Office. Interop. InfoPath. SemiTrust. dll
    
- Microsoft. Office. Interop. InfoPath. Xml. dll
    
In diesem Thema wird das Objektmodell erläutert, das über die Microsoft. Office. Interop. InfoPath-Interop-Assembly verfügbar gemacht wird, die exklusiv für externen Automatisierungscode verwendet wird. Informationen zur Microsoft. Office. Interop. InfoPath. SemiTrust-Assembly, die ausschließlich zum Schreiben und Ausführen von verwaltetem Code verwendet wird, der in InfoPath-Formularvorlagen (XSN) ausgeführt wird, finden Sie unter [infopath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Wichtige Informationen zur Installation

Die Standardinstallationsoption des InfoPath-Setupprogramms installiert die Microsoft. Office. Interop. InfoPath-Assembly im globalen Assemblycache (GAC), deren Inhalt im Ordner C:\Windows\Assembly angezeigt werden kann (oder in C:\Windows\assembly\GAC_ MSIL beim direkten Anzeigen des Dateisystems). Diese Assembly wird als "Microsoft Office InfoPath Primary Interop Assembly" bezeichnet und wird häufig in Verbindung mit der Microsoft. Office. Interop. InfoPath. XML-Assembly verwendet, die auch im GAC installiert ist, um die InfoPath-Anwendung aus zu automatisieren. externe Anwendungen, die verwalteten Code verwenden. Informationen zur Microsoft. Office. Interop. InfoPath. XML-Assembly finden Sie unter Informationen zur [InfoPath-XML-Interop-Assembly](about-the-infopath-xml-interop-assembly.md).
  
Wenn die Microsoft. Office. Interop. InfoPath-Assembly im GAC nicht sichtbar ist, sollten Sie sicherstellen, dass InfoPath ordnungsgemäß installiert wurde. Standardmäßig ist die Option **.NET-Programmierunterstützung** im Setupprogramm so festgelegt, dass Sie **von meinem Computer ausgeführt** wird, solange .NET Framework 1,1 Redistributable, .NET Framework 1,1 Software Development Kit (SDK) oder eine neuere Version von .NET Framework wird vor dem Ausführen von Setup installiert. Wenn diese Interop-Assemblys nicht auf Ihrem Computer verfügbar sind, müssen Sie sicherstellen, dass .NET Framework 1,1 oder höher installiert ist, und dann in der **System** Steuerung **Programme und Funktionen** verwenden, um das Setup zu ändern, indem Sie die **.net-Programmierbarkeit festlegen. Support** Option unter **Microsoft Office InfoPath** für die **Ausführung vom Arbeitsplatz aus**.
  
Informationen zum Herunterladen von .NET Framework 1,1 Redistributable finden Sie unter [.NET framework 1,1](https://www.microsoft.com/en-us/download/details.aspx?id=26)Redistributable.
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Der Microsoft. Office. Interop. InfoPath-Namespace

Obwohl der Prozess des Schreibens von verwaltetem Code für eine bestimmte Aufgabe dem Ausführen derselben Aufgabe mit einer Sprache wie Visual Basic für Applikationen oder JScript sehr ähnlich ist, wird das Objektmodell beim Anzeigen des **Microsoft. Office. Interop. InfoPath angezeigt.** der Namespace aus dem **Objektkatalog** in Microsoft Visual Studio sieht komplexer aus. Dies liegt daran, dass die Interoperabilität mit .NET Framework einen COM-Server erfordert, um alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte bereitzustellen, die für .NET Framework selbst erforderlich sind. Weitere Informationen dazu, wie und warum das von einer Interop-Assembly verfügbar gemachte Objektmodell komplexer erscheint, finden Sie im Abschnitt "wie COM-Objekte für verwalteten Code verfügbar gemacht werden" im Thema [InfoPath 2003 Compatible Object Models](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

In den Beispielen in diesem Abschnitt wird davon ausgegangen, dass Sie Verweise auf die Assemblys Microsoft. Office. Interop. InfoPath und Microsoft. Office. Interop. InfoPath. XML hergestellt haben. Informationen zum Festlegen von verweisen und zusätzlichen Beispielen für die externe Automatisierung finden Sie unter [Szenarios und Beispiele für externe Automatisierung](external-automation-scenarios-and-examples.md).
  
Bevor Sie den Microsoft IntelliSense-Anweisungsabschluss in externem Automatisierungscode verwenden können, müssen Sie eine Objektvariable für eine Instanz der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) -Klasse erstellen, wie in der folgenden Codezeile dargestellt. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Nachdem Sie die Objektvariable erstellt haben und den Variablennamen gefolgt von einem Punkt eingegeben haben, wird eine Dropdownliste mit den Mitgliedern der **Anwendungs** Klasse angezeigt, die Sie auswählen können. 
  
Wenn Sie mit einem InfoPath-Formular arbeiten möchten, deklarieren Sie eine Objektvariable vom Typ [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , und initialisieren Sie Sie dann, indem Sie das Formular aus der [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) -Auflistung der **Application** -Objektvariablen öffnen, wie in der folgenden Codezeile gezeigt. 
  
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

Die Dropdownliste IntelliSense-Anweisungsvervollständigung für Member der **XDocument** -Klasse wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Punkt eingeben. 
  
Wenn Sie mit den Inhalten des zugrunde liegenden XML-Dokuments für das Formular mithilfe von Microsoft XML Core Services (MSXML) arbeiten möchten, müssen Sie eine Variable vom Typ [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) erstellen und dann die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) -Eigenschaft der **XDocument** -Klasse verwenden, um den XML-Code zuzuweisen. Dokumentobjektmodell (DOM) des Formulars für diese Variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Die Dropdownliste IntelliSense-Anweisungsvervollständigung für Member der **IXMLDOMDocument2** -Klasse wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Punkt eingeben, mit dem Sie MSXML zum Arbeiten mit dem XML-Dokument verwenden können. 
  
### <a name="using-the-class-library-reference-documentation"></a>Verwenden der Referenzdokumentation der Klassenbibliothek

Die Organisation der Referenzdokumentation zur [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) -Namespace-Klassenbibliothek spiegelt die Beziehungen zwischen den Co-Klassen Schnittstellen und den geerbten Schnittstellen wider, die Sie implementieren. 
  
Wenn Sie ein Thema für eine coclass-Schnittstelle wie [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) öffnen, zeigt die Verknüpfung mit den Mitgliedern der coclass-Schnittstelle, die auf die Beschreibung der Schnittstelle am Anfang des Themas folgt, ein leeres Thema an. Sie müssen zum Anzeigen der Liste mit Membern, die von der Coklassen-Schnittstelle implementiert werden, das Thema für die aktuellste Schnittstelle öffnen, die von der Coklasse geerbt wird, und dann die Tabelle ihrer Member öffnen. Sie finden einen Link zu der geerbten Schnittstelle am Anfang des Themas zur Coklassen-Schnittstelle im Abschnitt "Hinweise". 
  
Wenn Sie F1 im Code-Editor von Visual Studio drücken, ist das Verhalten ähnlich, mit der Ausnahme, dass das Mitglied, auf das Sie F1-Hilfe aufrufen, direkt angezeigt wird, da Sie in der Regel mit den Mitgliedern einer Schnittstelle arbeiten. Dennoch kann die Tatsache, dass ein Member von einer versionsspezifischen Schnittstelle implementiert werden kann, zunächst verwirrend erscheinen. Wenn Sie beispielsweise den Cursor `myXDocument.UI.Alert` eingeben und auf `Alert` F1 drücken, wird ein Thema mit dem Titel "UI2. Alert-Methode "wird angezeigt. Dies ist der Fall, da die **Alert**-Methode eine Implementierung eines Members der **UI2**-Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an InfoPath-Objektmodellmember

Wenn ein InfoPath-Objektmodellelement einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie das **Type. Missing** -Feld für diesen Parameter übergeben. Wenn das **Type.Missing**-Feld nicht angegeben wird und ein tatsächlicher Wert ausgelassen wird, führt dies zu einem Buildfehler. Dies gilt für Code, der sowohl in C# als auch in Visual Basic geschrieben ist. Die [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) -Methode der ViewObject-Schnitt [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) Stelle enthält beispielsweise zwei optionale Parameter: _varEndNode_ und _varViewContext_. Eine Codezeile, in der keine tatsächlichen Werte für diese optionalen Parameter angegeben sind, sollte wie in den folgenden Beispielen dargestellt aussehen.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Siehe auch

- [Szenarien für die externe Automatisierung und Beispiele](external-automation-scenarios-and-examples.md)

