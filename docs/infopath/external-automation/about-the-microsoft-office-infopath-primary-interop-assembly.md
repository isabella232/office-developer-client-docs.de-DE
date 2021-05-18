---
title: Informationen zur Microsoft Office InfoPath Primary Interop-Assembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, primäre Interopassembly,primäre Interopassembly infoPath,PIAs [InfoPath 2007],primäre Interopassemblys [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Zur Unterstützung der Erstellung von InfoPath-Lösungen, die Sprachen mit verwalteten Code wie Visual C# und Visual Basic verwenden, installiert die Option .NET Programmability Support im InfoPath-Setupprogramm drei Interopassemblys.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310136"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Informationen zur Microsoft Office InfoPath Primary Interop-Assembly

Die InfoPath-Anwendung ist als COM -Anwendung (Component Object Model) erstellt, die ihre Programmierschnittstellen für die externe Automatisierung als COM-Schnittstellen verfügbar macht. Zur Unterstützung der Erstellung von InfoPath-Lösungen, die Sprachen mit verwalteten Code wie Visual C# und Visual Basic verwenden, installiert **die Option .NET Programmability Support** im InfoPath-Setupprogramm drei Interopassemblys. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
In diesem Thema wird das Objektmodell erläutert, das über die Microsoft.Office.Interop.InfoPath-Interop-Assembly verfügbar gemacht wird, die ausschließlich für externen Automatisierungscode verwendet wird. Informationen zur Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly, die ausschließlich zum Schreiben und Ausführen von verwalteten Code verwendet wird, der in InfoPath-Formularvorlagen (XSN) ausgeführt wird, finden Sie unter [InfoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Wichtige Informationen zur Installation

Mit der Standardinstallationsoption des #A0 wird die Microsoft.Office.Interop.InfoPath-Assembly im globalen Assemblycache (GAC) installiert, deren Inhalt im Ordner C:\Windows\Assembly (oder in C:\Windows\assembly\GAC_MSIL angezeigt werden kann, wenn das Dateisystem direkt angezeigt wird). Diese Assembly wird als "Microsoft Office InfoPath Primary Interop Assembly" bezeichnet und wird häufig in Verbindung mit der Microsoft.Office.Interop.InfoPath.Xml-Assembly verwendet, die auch in der GAC installiert ist, um die InfoPath-Anwendung aus externen Anwendungen zu automatisieren, die verwalteten Code verwenden. Weitere Informationen zur Microsoft.Office.Interop.InfoPath.Xml finden Sie unter [Informationen zur InfoPath XML Interop Assembly](about-the-infopath-xml-interop-assembly.md).
  
Wenn die Microsoft.Office.Interop.InfoPath-Assembly im GAC nicht sichtbar ist, sollten Sie bestätigen, dass InfoPath ordnungsgemäß installiert wurde. Standardmäßig ist die Option **.NET Programmierbarkeitsunterstützung** im  Setupprogramm auf Von Meinem Computer ausführen festgelegt, solange das .NET Framework 1.1 Redistributable, .NET Framework 1.1 Software Development Kit (SDK) oder eine spätere Version von .NET Framework installiert ist, bevor setup ausgeführt wird. Wenn diese Interopassemblys auf Ihrem Computer nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1.1  oder höher installiert ist, und dann Programme und **Features** aus der Systemsteuerung verwenden, um das Setup zu ändern, indem Sie die Option **.NET Programmierbarkeitsunterstützung** unter **Microsoft Office InfoPath** auf **Von** Meinem Computer ausführen festlegen.
  
Informationen zum Herunterladen der .NET Framework 1.1 Redistributable finden Sie [unter .NET Framework 1.1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Der Microsoft.Office.Interop.InfoPath-Namespace

Obwohl der Prozess des Schreibens von verwalteten Code für eine bestimmte Aufgabe dem Ausführen derselben Aufgabe mit einer Sprache wie Visual Basic for Applications oder JScript sehr ähnlich ist, sieht das objektmodell, das beim Anzeigen des **Microsoft.Office.Interop.InfoPath-Namespace** aus dem Objektbrowser **in** Microsoft Visual Studio verfügbar gemacht wird, komplexer aus. Dies liegt daran, dass die Interoperabilität mit dem .NET Framework erfordert, dass ein COM-Server alle öffentlichen Schnittstellen verfügbar macht, sowie einige zusätzliche Konstrukte, die von der .NET Framework werden. Weitere Informationen dazu, wie und warum das von einer Interop-Assembly verfügbar gemachte Objektmodell komplexer erscheint, finden Sie im Abschnitt "Wie COM-Objekte für verwalteten Code verfügbar gemacht werden" im Thema [InfoPath 2003 Compatible Object Models.](../form-templates/infopath-2003-compatible-object-models.md) 
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

In den Beispielen in diesem Abschnitt wird davon ausgegangen, dass Sie Verweise auf microsoft.Office.Interop.InfoPath und Microsoft.Office.Interop.InfoPath.Xml haben. Informationen zum Festlegen von Verweisen und zusätzliche Beispiele für die externe Automatisierung finden Sie unter [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).
  
Bevor Sie microsoft IntelliSense-Anweisung im externen Automatisierungscode verwenden können, müssen Sie eine Objektvariable für eine Instanz der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) erstellen, wie in der folgenden Codezeile dargestellt. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Wenn Sie nach dem Erstellen der Objektvariablen den Variablennamen gefolgt von einem Zeitraum eingeben, wird eine Dropdownliste mit Mitgliedern der zu wählenden **Application-Klasse** angezeigt. 
  
Um mit einem InfoPath-Formular zu arbeiten, deklarieren Sie eine Objektvariable vom Typ [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) und initialisieren Sie es dann, indem Sie das Formular aus der [XDocuments-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) der Application-Objektvariablen öffnen, wie in der folgenden Codezeile dargestellt.  
  
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

Die IntelliSense abschluss der Anweisung für Elemente der **XDocument-Klasse** wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Zeitraum eingeben. 
  
Um mit dem Inhalt des zugrunde liegenden XML-Dokuments für das Formular mithilfe von Microsoft XML Core Services (MSXML) zu arbeiten, müssen Sie eine Variable vom Typ [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) erstellen und dann die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) der **XDocument-Klasse** verwenden, um der Variablen das XML Document Object Model (DOM) des Formulars zuzuordnen. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Die IntelliSense-Anweisungsabschluss-Dropdownliste für Mitglieder der **IXMLDOMDocument2-Klasse** wird angezeigt, wenn Sie den Namen der Variablen gefolgt von einem Zeitraum eingeben, mit dem Sie MSXML verwenden können, um mit dem XML-Dokument zu arbeiten. 
  
### <a name="using-the-class-library-reference-documentation"></a>Verwenden der Referenzdokumentation der Klassenbibliothek

Die Organisation der Referenzdokumentation zur [Microsoft.Office.Interop.InfoPath-Namespace-Klassenbibliothek](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) spiegelt die Beziehungen zwischen Coklassenschnittstellen und den geerbten Schnittstellen wider, die sie implementieren. 
  
Wenn Sie ein Thema für eine Coclass-Schnittstelle öffnen, z. B. [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) zeigt der Link zu den Mitgliedern der Coclass-Schnittstelle nach der Beschreibung der Schnittstelle am Anfang des Themas ein leeres Thema an. Sie müssen zum Anzeigen der Liste mit Membern, die von der Coklassen-Schnittstelle implementiert werden, das Thema für die aktuellste Schnittstelle öffnen, die von der Coklasse geerbt wird, und dann die Tabelle ihrer Member öffnen. Sie finden einen Link zu der geerbten Schnittstelle am Anfang des Themas zur Coklassen-Schnittstelle im Abschnitt "Hinweise". 
  
Wenn Sie F1 im Visual Studio-Code-Editor drücken, ist das Verhalten ähnlich, mit der Ausnahme, dass das Element, für das Sie die F1-Hilfe aufrufen, direkt angezeigt wird, da Sie in der Regel mit Mitgliedern einer Schnittstelle arbeiten. Dennoch kann die Tatsache, dass ein Member von einer versionsspezifischen Schnittstelle implementiert werden kann, zunächst verwirrend erscheinen. Wenn Sie z. B. den Cursor eingeben und platzieren und F1 drücken, wird ein Thema mit dem Titel  `myXDocument.UI.Alert`  `Alert` "UI2. Alert Method" wird angezeigt. Dies ist der Fall, da die **Alert**-Methode eine Implementierung eines Members der **UI2**-Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an InfoPath-Objektmodellmember

Wenn ein Element des InfoPath-Objektmodells einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie das **Feld Type.Missing** für diesen Parameter übergeben. Wenn das **Type.Missing**-Feld nicht angegeben wird und ein tatsächlicher Wert ausgelassen wird, führt dies zu einem Buildfehler. Dies gilt für Code, der sowohl in C# als auch in Visual Basic. Die [SelectNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) der [ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) enthält beispielsweise zwei optionale Parameter:  _varEndNode_ und  _varViewContext_. Eine Codezeile, in der keine tatsächlichen Werte für diese optionalen Parameter angegeben sind, sollte wie in den folgenden Beispielen dargestellt aussehen.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Siehe auch

- [Szenarien für die externe Automatisierung und Beispiele](external-automation-scenarios-and-examples.md)

