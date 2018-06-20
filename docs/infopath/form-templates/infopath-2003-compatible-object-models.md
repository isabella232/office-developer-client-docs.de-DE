---
title: InfoPath 2003-kompatible Objektmodelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen object Model, InfoPath 2003-kompatible Objektmodell, Objektmodelle [InfoPath 2003], kompatibel mit InfoPath 2007, Objektmodelle [InfoPath 2007], InfoPath 2003 kompatible
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath wird als Anwendung Component Object Model (COM) geschrieben und stellt die Programmierbarkeit Schnittstellen für externe Automatisierung und Formular Vorlage Skript als COM-Schnittstellen.
ms.openlocfilehash: 09ba36b39e520629764bd57a623e8fb490a63a89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790782"
---
# <a name="infopath-2003-compatible-object-models"></a>InfoPath 2003-kompatible Objektmodelle

Microsoft InfoPath wird als Anwendung Component Object Model (COM) geschrieben und stellt die Programmierbarkeit Schnittstellen für externe Automatisierung und Formular Vorlage Skript als COM-Schnittstellen. Um das Erstellen von InfoPath-Lösungen zu unterstützen, die Visual c# und Visual Basic Sprachen mit verwaltetem Code verwenden, wird das InfoPath-Setup-Programm drei Interop-Assemblys installiert. Interop-Assemblys sind Assemblys, die fungieren als Brücke zwischen verwaltetem oder nicht verwaltetem Code, indem COM-Objektmember den gleichwertigen Mitglieder verwaltet. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
In diesem Thema wird das Objektmodell erläutert, das über die Microsoft.Office.Interop.InfoPath.SemiTrust-Interop-Assembly offen gelegt wird, die ausschließlich zum Schreiben und Ausführen von Geschäftslogik mit verwaltetem Code innerhalb von InfoPath-Formularvorlagen (XSN) verwendet wird.  
  
Informationen zu den Assemblys Microsoft.Office.Interop.InfoPath und Microsoft.Office.Interop.InfoPath.Xml finden Sie in der Dokumentation für die [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.aspx) und [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) Namespaces. 
  
## <a name="important-installation-information"></a>Wichtige Informationen zur installation

Standardmäßig installiert die Installationsoption **Standard** des InfoPath-Setup-Programms in der C:\Program Files\Microsoft Office\ Kopien der Assemblys Microsoft.Office.Interop.InfoPath.SemiTrust und Microsoft.Office.Interop.InfoPath.Xml Office14-Ordner. Die Assemblys Microsoft.Office.Interop.InfoPath und Microsoft.Office.Interop.InfoPath.Xml werden auch in den globalen Assemblycache (GAC), installiert, deren, die Inhalt sich von den Ordner C:\Windows\Assembly angezeigt werden können. 
  
Wenn diese Assemblys nicht installiert sind, sollten Sie sicherstellen, dass Microsoft InfoPath ordnungsgemäß installiert wurde. Wie lange als .NET Framework 2.0 oder höher installiert ist, bevor Sie Setup ausführen, wird die Option **.NET-Programmierunterstützung für** im InfoPath-Setupprogramm auf **vom Arbeitsplatz starten** für eine **Typische** Installation von InfoPath festgelegt. Wenn diese Interop-Assemblys nicht auf Ihrem Computer verfügbar sind, müssen Sie bestätigen, dass .NET Framework 2.0 oder höher installiert haben, und klicken Sie dann **Software hinzufügen oder entfernen** aus der **Systemsteuerung** ausgeführt und die **.NET-Programmierunterstützung für** festgelegt ist die Option auf **vom Arbeitsplatz starten**.
  
Informationen zum Herunterladen von .NET Framework 2.0 Redistributable finden Sie unter [.NET Framework 2.0 Redistributable.](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>Microsoft.Office.Interop.InfoPath.SemiTrust-namespace

Vor der Veröffentlichung von Microsoft Office InfoPath 2003 Service Pack 1 und Microsoft Office InfoPath 2003 Toolkit für Visual Studio® .NET wurde die gesamte Programmierlogik für InfoPath-Formularvorlagen mithilfe von Microsoft JScript oder Microsoft VBScript erstellt, das in der Microsoft Script Editor-Entwicklungsumgebung (MSE) geschrieben wurde. Ein in MSE geschriebenes Skript wird zur Laufzeit interpretiert und greift auf das COM-Objektmodell zu, das von der Dynamic Link Library IPEDITOR.dll verfügbar gemacht wird.
  
Um die Unterstützung für die Erstellung von Formularvorlagen, die für die Programmierlogik Sprachen mit verwaltetem Code wie Visual c# und Visual Basic verwenden,-Funktionalität wurde hinzugefügt, um InfoPath So aktivieren Sie die common Language Runtime (CLR) hosting und die Interop-Assembly Microsoft.Office.Interop.InfoPath.SemiTrust erstellt wurde, zum Aktivieren von verwalteten Codes für die Zusammenarbeit mit dem COM-Objektmodell von InfoPath auf sichere Weise verfügbar gemacht werden. Informationen über das Sicherheitsmodell, das auf InfoPath Formularvorlagen mit verwaltetem Code angewendet wird, finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md). 
  
Obwohl der Prozess der schreiben verwalteten ähnelt Code für eine bestimmte Aufgabe in einer InfoPath-Formularvorlage ausführen dieselbe Programmieraufgabe durch Schreiben von Skripts, das InfoPath 2003-kompatible Objektmodell verfügbar gemacht, wenn die **anzeigen Microsoft.Office.Interop.InfoPath.SemiTrust** Namespace aus dem **Objektbrowser** in Visual Studio 2012 sieht wesentlich komplexer. Dies ist, da die .NET Framework-Interoperabilität-Technologie verwendet, um das InfoPath 2003-kompatible Objektmodell unterstützen ist, ein COM-Servers erforderlich, um alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte von .NET Framework selbst verfügbar zu machen. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>COM-Objekte werden wie für das InfoPath 2003 kompatible Objektmodell verfügbar gemacht.

Beim systemintern mit einem COM-Server als allgemeine Sprachen wie JScript, VBScript oder Visual Basic (aber nicht die .NET Version von Visual Basic und Visual c#) arbeiten, ist das Objektmodell, das verfügbar gemacht, ist einfacher als die zugrunde liegenden COM-Klassen und Schnittstellen. Beispielsweise, wenn aus diesen Sprachen, die InfoPath- **Benutzeroberfläche** arbeiten Objekt macht eine Reihe von sieben Methoden, wie die **Alert** -Methode zum Anzeigen einer Nachricht für Benutzer im Feld. 
  
Die zugrunde liegende COM-Konstrukte, die das **UI** -Objekt unterstützt werden jedoch besteht aus drei Entitäten: zwei Schnittstellen mit der **Benutzeroberfläche** und **Anwenderschnittstelle: 2**und eine COM-Co-Klasse, die Mitglieder der folgenden zwei Schnittstellen implementiert. Es gibt zwei Versionen der **UI** -Schnittstelle, da das COM-Framework erfordert die Definition einer Schnittstelle festen zum Aufrechterhalten der Abwärtskompatibilität für Programme und Komponenten, die eine Implementierung dieser Schnittstelle aufrufen beibehalten. 
  
In diesem Fall enthält **die Benutzeroberfläche, die für die erste Version von InfoPath definiert wurde,** vier Methoden, einschließlich der **Alert** -Methode. Die Schnittstelle **Anwenderschnittstelle: 2** eine zweite Version der **Benutzeroberfläche** Schnittstelle betrachtet werden kann, und es definiert wurde für die InfoPath Service Pack 1-Version. Die **Anwenderschnittstelle: 2** -Schnittstelle erbt die vier Methoden der ursprünglichen **UI** -Schnittstelle und drei neue Methoden, wie die **Confirm** -Methode hinzugefügt. Obwohl Sie können einer Codezeile entweder im Skript oder verwalteten Code zum Aufrufen der **Confirm** -Methode mit `XDocument.UI.Confirm`, wird die zugrunde liegende Code ist tatsächlich die **Confirm** -Methode der **Anwenderschnittstelle: 2** -Schnittstelle von der Implementierung dieser Methode aufrufen in der COM-Co-Klasse. 
  
Das Objektmodell für Skripts verfügbar gemacht wird diese Details verbirgt, aber die Interop-Assembly erforderlich, mit einem COM-Server aus verwaltetem Code macht die Co-Klasse und beide Schnittstellen öffentlich funktionsfähig ist. Für die einzelnen **UI** -Objekt in der Skripting MSE-Umgebung verwendet stellt der **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace die folgenden drei Elemente zur Verfügung: 
  
- [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) -Schnittstelle 
    
- [Anwenderschnittstelle: 2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) -Schnittstelle 
    
- [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Coklassen-Schnittstelle 
    
Obwohl alle drei dieser Schnittstellen im **Objektbrowser** verfügbar gemacht werden und sind in der Dokumentation zur Klassenbibliothek für den Namespace enthalten, nur arbeiten Sie mit der **UIObject** -Schnittstelle Co-Klasse, die das **UI** -Objekt implementiert, und mit den Mitgliedern der **Anwenderschnittstelle: 2** -Schnittstelle, die die neueste Version der Schnittstelle ist, die durch das **UIObject** -Coklassen-Schnittstelle implementiert wird. Zugriff auf die **UIObject** -Coklassen-Schnittstelle von seinem übergeordneten [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Objekt, wie in Skript, verwenden Sie die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Accessor-Eigenschaft. Bis auf wenige Ausnahmen ist dies das Muster für alle Objekte aus der ursprünglichen Version von InfoPath, die bei der Veröffentlichung von InfoPath Service Pack 1 aktualisiert wurden. 
  
Während das Muster im Wesentlichen identisch ist, ist die Situation etwas einfacher für die vollkommen neuer Objekte, die in InfoPath Service Pack 1, wie etwa das **Certificate** -Objekt hinzugefügt wurden. In diesem Fall sind nur zwei Elemente mit befassen: [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) -Coklassen-Schnittstelle und die Mitglieder der [Zertifikat](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) -Schnittstelle, die das aktuellste Ergebnis ist und nur von der **CertificateObject** implementierte Schnittstelle Coklassen-Schnittstelle. Wie bei der Verwendung von InfoPath-COM-Objekte aus Skript [Zertifikat](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) -Accessor-Eigenschaft verwendet wird auf das Objekt von der übergeordneten Website zugreifen. 
  
In demselben Muster betrifft die Schnittstellen für Auflistungen, mit Ausnahme die Co-Schnittstelle für eine Auflistung "Collection" an den Namen anstelle von "Objekt" angefügt wurde. Beispielsweise Coklassen-Schnittstelle für die COM- **DataAdapters** -Auflistung heißt [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) und die Schnittstelle implementiert wird die [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) -Schnittstelle. Auf ähnliche Weise wird die [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) -Accessor-Eigenschaft des übergeordneten Objekts **XDocument** die Auflistung zuzugreifen. 
  
Es gibt drei Ausnahmen dieser Benennungsmuster. Die Co-Schnittstellen für die COM- **Anwendung** und **XDocument** -Objekte haben keine "Objekt" in ihre Namen angefügt. Ihre Namen sind identisch mit ihren entsprechenden COM-Objekte: [Anwendung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) und **XDocument-Objekt**. Darüber hinaus den Namen der von der **Anwendung** implementiert Schnittstellen und **XDocument** Co-Schnittstellen mit einem Unterstrich (_) vorangestellt werden: [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) und [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . Die dritte Ausnahme ist das COM- **DataObject** -Objekt. Die Coklassen-Schnittstelle für dieses Objekt heißt [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , aber genau wie andere InfoPath-COM-Objekten, die Schnittstelle implementierten der [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) -Schnittstelle ist. 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Wie Microsoft XML Core Services (MSXML) 5.0 für Microsoft Office-Objekte auf das InfoPath 2003 kompatible Objektmodell offengelegt werden

Eine Teilmenge der Objekte und Elemente des Objektmodells zur Verfügung gestellt von Microsoft XML Core Services (MSXML), der auch eine COM-Server ist, werden von Schnittstellen, die von der Microsoft.Office.Interop.InfoPath.SemiTrust-interop-Assembly verfügbar gemacht werden umbrochen. Der Grund dafür, dass dies erforderlich ist ist, die einige der Member des InfoPath-COM-Objektmodells MSXML abhängig und müssen in der Lage, diese Member auf sichere Weise zugreifen. Die Namen der Schnittstellen im **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace, die umbrochen werden die Objekte und Member des MSXML-Objektmodells sind identisch mit den Namen von MSXML com-Server verfügbar gemacht werden. In den meisten Fällen werden diese Namen "IXMLDOM" als Präfix vorangestellt, da sie zum Arbeiten mit dem XML-Dokument (DOKUMENTOBJEKTMODELL) verwendet werden. Beispielsweise gibt die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) -Eigenschaft des **XDocument** -Schnittstelle, die verwendet wird, um einen Verweis auf das einem Formular zugrunde liegenden XML-Dokument zurückzugeben, die [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) -Schnittstelle, die durch umgebrochen wird die Interop-Assembly Microsoft.Office.Interop.InfoPath.SemiTrust. Sie aufrufen und verwenden Sie die Elemente der **IXMLDOMDocument** -Schnittstelle im Wesentlichen die gleiche Weise als, verwaltetem Code mithilfe von Skripts in Formularvorlagen, die nicht verwenden. 
  
Weitere Informationen zum Verwenden von Membern von Microsoft XML Core Services (MSXML) für Microsoft Office-Objektmodell in Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit MSXML und System.Xml mithilfe des InfoPath 2003-Objektmodells](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

Für den Großteil des Codes, die Sie für das InfoPath 2003-kompatible Objektmodell in einer Formularvorlage mit verwaltetem Code schreiben, verwenden Sie die `thisXDocument` und `thisApplication` Variablen, die in initialisiert werden die `_Startup` -Methode des die Standardklassendatei "FormCode.cs" oder "FormCode.vb". Sie können die `thisXDocument` und `thisApplication` Variablen den Zugriff auf Member der [XDocument-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) und der [Anwendung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Co-Schnittstellen. Nachdem Sie den Namen der entweder Variable gefolgt von einem Punkt eingeben, werden IntelliSense-Anweisung Vervollständigung der Liste Elemente von den entsprechenden Coklassen-Schnittstelle angezeigt. Sie können weiterhin auf diese Weise auf die Objektmodellelement zugreifen, den Sie arbeiten möchten. 
  
Im folgenden ist ein einfaches Beispiel, das verwendet die `thisXDocument` Variable die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode, um die Version der InfoPath-Anwendung anzeigen, indem Sie mithilfe der [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) -Eigenschaft zugegriffen aus Zugriff auf die `thisApplication` Variable. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Verwenden von der Referenzdokumentation der Klassenbibliothek

Die Organisation der **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace Referenzdokumentation der Klassenbibliothek gilt für die Beziehungen zwischen Co-Klasse und der geerbten Schnittstellen, die sie implementieren. Dies wird im Abschnitt "Wie COM-Objekte sind verfügbar gemacht zu verwaltetem Code" weiter oben in diesem Thema beschrieben. 
  
Obwohl der Organisation sowie der **Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace naming Referenzdokumentation verwirrend wird zunächst in den Themen im Wesentlichen auf die gleiche Weise wie der InfoPath-Objektmodellreferenz, die organisiert werden Teil der InfoPath Referenz für Entwickler, die in InfoPath enthalten ist. Mit Ausnahme der Themen für die **Anwendung** und die **XDocument** -Schnittstellen ordnen Sie alle Themen COM-Co-Schnittstelle auf die entsprechende "Object" und "Collection" Themen aus der InfoPath scripting Verweis. Beispielsweise entsprechen ähnliche Inhalte in der "UI-Objekt" und "Windows-Auflistung" "UIObject-Schnittstelle" und in den Themen "WindowsCollection-Schnittstelle" von der Referenzdokumentation **Microsoft.Office.Interop.InfoPath.SemiTrust** -namespace Die Themen der InfoPath-Objektmodellreferenz scripting Verweis. 
  
Der Link zu den Membern der Coklassen-Schnittstelle nach der Beschreibung der Schnittstelle am Anfang des Themas verweist allerdings auf ein leeres Thema. Sie müssen zum Anzeigen der Liste mit Membern, die von der Coklassen-Schnittstelle implementiert werden, das Thema für die aktuellste Schnittstelle öffnen, die von der Coklasse geerbt wird, und dann die Tabelle ihrer Member öffnen. Sie finden einen Link zu der geerbten Schnittstelle am Anfang des Themas zur Coklassen-Schnittstelle im Abschnitt "Hinweise".
  
Wenn Sie im Code-Editor F1 drücken, ähnelt das Verhalten, mit der Ausnahme, dass das Element, auf dem Sie F1-Hilfe aufzurufen, da Sie in der Regel am häufigsten mit den Mitgliedern einer Schnittstelle arbeiten direkt angezeigt werden. Allerdings kann die Tatsache, dass ein Element aus einer mit Versionsangabe-Schnittstelle implementiert werden kann beim ersten verwirrend werden es auftreten. Beispiel: bei Eingabe `thisXDocument.UI.Alert` , und platzieren Sie den Cursor auf `Alert` , und drücken Sie F1, ein Thema mit dem Titel "Anwenderschnittstelle: 2. Alert-Methode"wird angezeigt. Dies ist, da die **Alert** -Methode eine Implementierung eines Mitglieds der **Anwenderschnittstelle: 2** -Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben Optionaler Parameter an InfoPath-Objektmodellmember

Wenn eine InfoPath 2003-kompatible Objektmodellelement einen optionalen Parameter enthält, und Sie einen Wert für diesen Parameter nicht angeben, müssen Sie stattdessen das Feld **Type.Missing** für diesen Parameter übergeben. Installationsfehler, Feld **Type.Missing** übergeben, wenn Sie ein Istwert ausgelassen wird, in einen Buildfehler bewirken. Dies gilt für Code in Visual c# und Visual Basic geschrieben. Die [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) -Methode der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle umfasst beispielsweise zwei optionale Parameter: _VarEndNode_ und _VarViewContext_. Eine Codezeile, die keine tatsächlichen Werte für diese optionale Parameter angegeben wird, sollte wie in den folgenden Beispielen aussehen.
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>Informationen zu common Language Specification-Kompatibilität

Jede Schnittstelle und Member in der Assembly Microsoft.Office.Interop.InfoPath.SemiTrust wurde intern, dessen **CLSCompliant** -Attribut auf **false**festgelegt. Referenzdokumentation für die teilweise mithilfe von **System.Reflection**generiert wird, weshalb die Beschreibung der Schnittstellen und Member der Begriff "diese Schnittstelle /-Methode/Eigenschaft ist nicht CLS-kompatibel" angehängt wird. Die meisten Schnittstellen und Member des [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespaces werden jedoch tatsächlich CLS-kompatibel. 
  
## <a name="see-also"></a>Siehe auch

- [Allgemeine Aufgaben zum Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Grundlegendes zum InfoPath 2003-Objektmodells](understanding-the-infopath-2003-object-model.md)

