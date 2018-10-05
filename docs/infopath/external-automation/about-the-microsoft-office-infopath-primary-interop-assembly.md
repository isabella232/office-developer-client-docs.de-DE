---
title: Informationen zur Microsoft Office InfoPath Primary Interop-Assembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, primäre Interop-Assembly InfoPath primären interop-Assembly, PIAs [InfoPath 2007], primären Interop-Assemblys [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Um das Erstellen von InfoPath-Lösungen unterstützen, die Sprachen mit verwaltetem Code wie Visual c# und Visual Basic verwenden, wird die Option .NET Programmierbarkeit Support im InfoPath-Setupprogramm drei Interop-Assemblys installiert.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393355"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Informationen zur Microsoft Office InfoPath Primary Interop-Assembly

Die InfoPath-Anwendung wird als Component Object Model (COM) Anwendung erstellt, die ihre Programmierbarkeit Schnittstellen für die externe Automatisierung als COM-Schnittstellen verfügbar macht. Um das Erstellen von InfoPath-Lösungen unterstützen, die Sprachen mit verwaltetem Code wie Visual c# und Visual Basic verwenden, wird die Option **.NET Programmierbarkeit Support** im InfoPath-Setupprogramm drei Interop-Assemblys installiert. Interop-Assemblys sind Assemblys, die fungieren als Brücke zwischen verwaltetem oder nicht verwaltetem Code, indem COM-Objektmember den gleichwertigen Mitglieder verwaltet. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
In diesem Thema wird das Objektmodell verfügbar gemacht werden, bis die Microsoft.Office.Interop.InfoPath Interop-Assembly, die ausschließlich für die externe Automatisierungscode verwendet wird. Informationen zu der Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly, die verwendet wird, ausschließlich für Schreiben und Ausführen von verwaltetem Code, die von in InfoPath-Formularvorlagen (XSN) ausgeführt wird, finden Sie unter [InfoPath 2003 kompatible Objektmodelle](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Wichtige Informationen zur Installation

Die Standardoption für die Installation des InfoPath-Setup-Programms installiert die Microsoft.Office.Interop.InfoPath Assembly in den globalen Assemblycache (GAC), deren Inhalt sich von den Ordner C:\Windows\Assembly (oder in C:\Windows\assembly\GAC_ angezeigt werden können MSIL beim direkt im Dateisystem anzeigen). Diese Assembly ist als die "Microsoft Office InfoPath Primary Interop Assembly" bezeichnet und wird häufig in Verbindung mit der Microsoft.Office.Interop.InfoPath.Xml-Assembly, die auch im GAC installiert ist, zum Automatisieren von InfoPath-Anwendung verwendet externe Anwendungen, die verwalteten Code verwenden. Informationen über die Assembly Microsoft.Office.Interop.InfoPath.Xml finden Sie unter [Über die InfoPath XML-Interop-Assembly](about-the-infopath-xml-interop-assembly.md).
  
Wenn die Microsoft.Office.Interop.InfoPath Assembly nicht im GAC angezeigt wird, sollten Sie sicherstellen, dass InfoPath ordnungsgemäß installiert wurde. Standardmäßig ist die Option **.NET-Programmierunterstützung für** im Setup-Programm so lange als .NET Framework 1.1 Redistributable, .NET Framework 1.1 Software Development Kit (SDK) oder eine höhere Version von .NET Framework **vom Arbeitsplatz starten** festgelegt. wird vor dem Ausführen von Setup installiert. Wenn diese Interop-Assemblys nicht auf Ihrem Computer verfügbar sind, müssen Sie bestätigen, dass .NET Framework 1.1 oder höher installiert ist, und klicken Sie dann mit **Programme und Funktionen** aus der **Systemsteuerung** um Setup zu ändern, indem Sie die **.NET-Programmierung Unterstützung** Option unter **Microsoft Office InfoPath** auf **vom Arbeitsplatz starten**.
  
Informationen zum Herunterladen von .NET Framework 1.1 Redistributable finden Sie unter [.NET Framework 1.1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Die Microsoft.Office.Interop.InfoPath-Namespace

Obwohl der Prozess der Schreiben von verwalteten ist Code für eine bestimmte Aufgabe führen Sie die Verwendung einer Sprache wie Visual Basic für Applikationen oder das Objektmodell verfügbar gemacht werden beim Anzeigen der **Microsoft.Office.Interop.InfoPath** JScript Aufgabe sehr ähnlich Namespace aus dem **Objektbrowser** in Microsoft Visual Studio sucht komplexer. Dies ist, da die Interoperabilität mit .NET Framework benötigt ein COM-Server, alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte von .NET Framework selbst verfügbar zu machen. Weitere Informationen wie und warum das Objektmodell von einer Interop-Assembly verfügbar gemacht werden komplexere angezeigt wird finden Sie im Abschnitt "Wie COM-Objekte sind verfügbar gemacht zu verwaltetem Code" neben dem Thema [InfoPath 2003 kompatible Objektmodelle](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

Die Beispiele in diesem Abschnitt wird davon ausgegangen, dass Sie Verweise auf die Assemblys Microsoft.Office.Interop.InfoPath und Microsoft.Office.Interop.InfoPath.Xml eingerichtet haben. Informationen zum Festlegen, Referenzen und Beispiele für zusätzliche externe Automatisierung finden Sie unter [externe Automatisierungsszenarien und Beispiele](external-automation-scenarios-and-examples.md).
  
Bevor Sie den Abschluss der Microsoft IntelliSense-Anweisung in externem Automatisierungscode verwenden können, müssen Sie eine Objektvariable für eine Instanz der Klasse [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) erstellen, wie in der folgenden Codezeile gezeigt. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Nach dem Erstellen der Objektvariablen, wird bei der Eingabe der Name der Variablen gefolgt von einem Punkt ein Dropdown-Listenfeld mit den Mitgliedern der **Anwendungsklasse** auswählen angezeigt. 
  
Die Verwendung mit einem InfoPath-Formular deklarieren Sie eine Objektvariable vom Typ [XDocument-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , und initialisieren Sie es dann durch Öffnen des Formulars aus der [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) -Auflistung des **Application** -Objektvariable wie in der folgenden Codezeile gezeigt. 
  
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

IntelliSense-Anweisung Abschluss Dropdown-Liste für Mitglieder der **XDocument** -Klasse wird ausgegeben, wenn Sie den Namen der Variablen, gefolgt von einem Punkt eingeben. 
  
Für die Verwendung mit dem Inhalt des zugrunde liegenden XML-Dokuments für das Formular mithilfe von Microsoft XML Core Services (MSXML) müssen Sie eine Variable vom Typ [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) erstellen, und klicken Sie dann die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) -Eigenschaft des **XDocument** -Klasse verwenden, um den XML-Code zuweisen Modell DOM (Document Object) des Formulars, das diese Variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

IntelliSense-Anweisung Abschluss Dropdown-Liste für Mitglieder der **IXMLDOMDocument2** -Klasse wird ausgegeben, wenn Sie den Namen der Variablen geben, gefolgt von einem Punkt, dem Sie MSXML zum Arbeiten mit dem XML-Dokument verwenden kann. 
  
### <a name="using-the-class-library-reference-documentation"></a>Verwenden der Referenzdokumentation der Klassenbibliothek

Die Organisation des [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) -Namespace Referenzdokumentation der Klassenbibliothek gilt für die Beziehungen zwischen Co-Klasse und der geerbten Schnittstellen, die sie implementieren. 
  
Wenn Sie ein Thema für die Klassenschnittstelle Co-, wie die [Anwendung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , öffnen zeigt den Link an die Mitglieder der folgenden der Beschreibung der Schnittstelle am Anfang des Themas Coklassen-Schnittstelle ein leeres Thema. Um die Liste der Elemente anzuzeigen, die von der Co-Schnittstelle implementiert sind, müssen Sie öffnen Sie das Thema für die aktuelle Schnittstelle, die von der Co-Klasse geerbt wird, und öffnen Sie die Tabelle Member. Eine Verknüpfung mit der geerbten Schnittstelle wird am Anfang des Abschnitts "Hinweise" im Thema Co-Schnittstelle bereitgestellt. 
  
Wenn Sie im Code-Editor von Visual Studio F1 drücken, ähnelt das Verhalten, mit der Ausnahme, dass das Element, auf dem Sie F1-Hilfe aufzurufen, da Sie in der Regel am häufigsten mit den Mitgliedern einer Schnittstelle arbeiten direkt angezeigt werden. Allerdings kann die Tatsache, dass ein Element aus einer mit Versionsangabe-Schnittstelle implementiert werden kann beim ersten verwirrend werden es auftreten. Beispiel: bei Eingabe `myXDocument.UI.Alert` , und platzieren Sie den Cursor auf `Alert` , und drücken Sie F1, ein Thema mit dem Titel "Anwenderschnittstelle: 2. Alert-Methode"wird angezeigt. Dies ist, da die **Alert** -Methode eine Implementierung eines Mitglieds der **Anwenderschnittstelle: 2** -Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an InfoPath-Objektmodellmember

Wenn ein InfoPath-Objektmodellmember einen optionalen Parameter enthält, und Sie einen Wert für diesen Parameter nicht angeben, müssen Sie das Feld **Type.Missing** für diesen Parameter übergeben. Installationsfehler, Feld **Type.Missing** übergeben, wenn Sie ein Istwert ausgelassen wird, in einen Buildfehler bewirken. Dies gilt für Code in c# und Visual Basic geschrieben. Die [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) -Methode der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) -Schnittstelle umfasst beispielsweise zwei optionale Parameter: _VarEndNode_ und _VarViewContext_. Eine Codezeile, die keine tatsächlichen Werte für diese optionale Parameter angegeben wird, sollte wie in den folgenden Beispielen aussehen.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Siehe auch

- [Szenarios für die externe Automatisierung und Beispiele](external-automation-scenarios-and-examples.md)

