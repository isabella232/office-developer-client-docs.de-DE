---
title: Mit InfoPath 2003 kompatible Objektmodelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Objektmodell, InfoPath 2003-kompatibles Objektmodell, Objektmodelle [InfoPath 2003], kompatibel mit InfoPath 2007, Objektmodelle [InfoPath 2007], InfoPath 2003 kompatibel
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath wird als COM-Anwendung (Component Object Model) geschrieben und stellt die Programmierschnittstellen für die externe Automatisierung und das Formularvorlagen Skript als COM-Schnittstellen bereit.
ms.openlocfilehash: f3351a0fee6e23de0785aa28b0970c6a90361f16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303521"
---
# <a name="infopath-2003-compatible-object-models"></a>Mit InfoPath 2003 kompatible Objektmodelle

Microsoft InfoPath wird als COM-Anwendung (Component Object Model) geschrieben und stellt die Programmierschnittstellen für die externe Automatisierung und das Formularvorlagen Skript als COM-Schnittstellen bereit. Als Unterstützung für die Erstellung von InfoPath-Projektmappen, in denen die Programmiersprachen Visual C# und Visual Basic mit verwaltetem Code verwendet werden, werden vom InfoPath-Setupprogramm drei Interop-Assemblys installiert. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft. Office. Interop. InfoPath. dll
    
- Microsoft. Office. Interop. InfoPath. SemiTrust. dll
    
- Microsoft. Office. Interop. InfoPath. Xml. dll
    
In diesem Thema wird das Objektmodell erläutert, das über die Microsoft.Office.Interop.InfoPath.SemiTrust-Interop-Assembly offen gelegt wird, die ausschließlich zum Schreiben und Ausführen von Geschäftslogik mit verwaltetem Code innerhalb von InfoPath-Formularvorlagen (XSN) verwendet wird.  
  
Informationen zu den Assemblys Microsoft. Office. Interop. InfoPath und Microsoft. Office. Interop. InfoPath. XML finden Sie in der Dokumentation zu [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) und [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . Namespaces. 
  
## <a name="important-installation-information"></a>Wichtige Installationsinformationen

Standardmäßig werden mit **** der Installationsoption für das InfoPath-Setupprogramm Kopien der Assemblys "Microsoft. Office. Interop. InfoPath. SemiTrust" und "Microsoft. Office. Interop. InfoPath. xml" im Ordner "c:\Programme\Microsoft Office \" installiert. Office14-Ordner. Die Assemblys Microsoft. Office. Interop. InfoPath und Microsoft. Office. Interop. InfoPath. XML werden auch im globalen Assemblycache (GAC) installiert, dessen Inhalt im Ordner C:\Windows\Assembly angezeigt werden kann. 
  
Wenn diese Assemblys nicht installiert sind, sollten Sie sicherstellen, dass Microsoft InfoPath ordnungsgemäß installiert wurde. Solange .NET Framework 2,0 oder höher installiert ist, bevor das Setup ausgeführt wird, ist die Option **.NET-Programmierunterstützung** im InfoPath-Setupprogramm für eine **typische** Installation von InfoPath auf " **Arbeitsplatz** " festgelegt. Wenn diese Interop-Assemblys nicht auf Ihrem Computer verfügbar sind, müssen Sie sicherstellen, dass .NET Framework 2,0 oder höher installiert ist, und dann **Software** in der **System** Steuerung ausführen und die .net- **Programmierunterstützung** festlegen. Option zum **Ausführen von "Arbeitsplatz**".
  
Informationen zum Herunterladen von .NET Framework 2,0 Redistributable finden Sie unter [.NET framework 2,0 Redistributable.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>Der Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace

Vor der Veröffentlichung von Microsoft Office InfoPath 2003 Service Pack 1 und Microsoft Office InfoPath 2003 Toolkit für Visual Studio® .NET wurde die gesamte Programmierlogik für InfoPath-Formularvorlagen mithilfe von Microsoft JScript oder Microsoft VBScript erstellt, das in der Microsoft Script Editor-Entwicklungsumgebung (MSE) geschrieben wurde. Ein in MSE geschriebenes Skript wird zur Laufzeit interpretiert und greift auf das COM-Objektmodell zu, das von der Dynamic Link Library IPEDITOR.dll verfügbar gemacht wird.
  
Zur Unterstützung der Erstellung von Formularvorlagen, die Sprachen mit verwaltetem Code verwenden, wie Visual C# und Visual Basic für Programmierlogik, wurde InfoPath die Funktionalität hinzugefügt, die das Hosten der Common Language Runtime (CLR) und der Die Interop-Assembly Microsoft. Office. Interop. InfoPath. SemiTrust wurde erstellt, damit verwalteter Code mit dem COM-Objektmodell interagieren kann, das von InfoPath auf sichere Weise verfügbar gemacht wird. Informationen zum Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter Informationen zum [Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md). 
  
Obwohl das Schreiben von verwaltetem Code für eine bestimmte Aufgabe in einer InfoPath-Formularvorlage dem Ausführen derselben Programmieraufgabe durch das Schreiben von Skripts ähnelt, wird das InfoPath 2003-kompatible Objektmodell beim Anzeigen des ** Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace aus dem **Objektkatalog** in Visual Studio 2012 sieht viel komplexer aus. Der Grund dafür ist, dass die zur Unterstützung des InfoPath 2003-kompatiblen Objektmodells verwendete .NET Framework-Interoperabilitäts Technologie einen COM-Server benötigt, um alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte bereitzustellen, die für .NET Framework selbst erforderlich sind. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Wie COM-Objekte für das InfoPath 2003-kompatible Objektmodell verfügbar gemacht werden

Bei der systemeigenen Arbeit mit einem COM-Server mit Programmiersprachen hoher Ebene, beispielsweise JScript, VBScript oder Visual Basic (jedoch nicht die .NET-Versionen von Visual Basic und Visual C#), ist das offen gelegte Objektmodell einfacher als die zugrunde liegenden COM-Klassen und Schnittstellen. So legt das **UI**-Objekt von InfoPath bei der Arbeit mit diesen Sprachen eine Gruppe mit sieben Methoden offen, beispielsweise die **Alert**-Methode, um ein Meldungsfeld für Benutzer anzuzeigen. 
  
Die zugrunde liegenden COM-Konstrukte, die das **UI**-Objekt unterstützen, bestehen jedoch aus drei Entitäten: Zwei Schnittstellen mit Namen **UI** und **UI2** sowie einer COM-Coklasse, die die Member dieser beiden Schnittstellen implementiert. Es gibt zwei Versionen der **UI**-Schnittstelle, da das COM-Framework die Definition einer fest bestehenden Schnittstelle benötigt, um Rückwärtskompatibilität für Programme und Komponenten beizubehalten, die eine Implementierung dieser Schnittstelle aufrufen. 
  
In diesem Fall stellt die **Benutzeroberflächen** -Schnittstelle, die für die erste Release von InfoPath definiert wurde, vier Methoden bereit, einschließlich der **Alert** -Methode. Die **UI2** -Schnittstelle kann als zweite Version der **Benutzeroberflächen** Schnittstelle angesehen werden und wurde für die InfoPath Service Pack 1-Version definiert. Die **UI2** -Schnittstelle erbt die vier Methoden der ursprünglichen **Benutzeroberflächen** -Schnittstelle und fügt drei neue Methoden hinzu, beispielsweise die **Confirm** -Methode. Sie können zwar eine Codezeile in Skript oder verwaltetem Code schreiben, der die **Confirm** `XDocument.UI.Confirm`-Methode verwendet, aber der zugrunde liegende Code ruft tatsächlich die **Confirm** -Methode der **UI2** -Schnittstelle aus der Implementierung dieser Methode auf. in der COM-Co-Klasse. 
  
Wenn das Objektmodell für das Scripting offen gelegt wird, blendet es diese Details zwar aus, die Interop-Assembly, die für die Arbeit mit einem COM-Server für den verwalteten Code erforderlich ist, legt die Coklasse und beide Schnittstellen jedoch öffentlich offen. Für das einzelne, in der MSE-Scriptingumgebung verwendete **UI**-Objekt legt der **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace die folgenden drei Elemente offen: 
  
- [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) Oberfläche 
    
- [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) -Schnittstelle 
    
- [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle der Co-Klasse 
    
Obwohl alle drei Schnittstellen im **Objektkatalog** verfügbar gemacht werden und in der Klassenbibliotheksdokumentation für den Namespace enthalten sind, arbeiten Sie nur mit der **UIObject** -coclass-Schnittstelle, die das **UI** -Objekt implementiert, und mit den Membern der **UI2** -Schnittstelle, bei der es sich um die neueste Version der Schnittstelle handelt, die von der **UIObject** -coclass-Schnittstelle implementiert wird. Verwenden Sie die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Accessor-Eigenschaft, um auf die **UIObject** -coclass-Schnittstelle über das übergeordnete [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Objekt zuzugreifen. Mit Ausnahme einiger bemerkenswerter Ausnahmen ist dies das Muster für alle Objekte aus der ursprünglichen Version von InfoPath, die beim Veröffentlichen von InfoPath Service Pack 1 aktualisiert wurden. 
  
Das Muster ist zwar grundsätzlich dasselbe, dennoch ist die Situation bei völlig neuen Objekten etwas einfacher, die in InfoPath Service Pack 1 hinzugefügt wurden, beispielsweise dem**Certificate**-Objekt. In diesem Fall sind nur zwei Elemente zu beachten: die CertificateObject-coclass [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) -Schnittstelle und die Member der [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) -Schnittstelle, die die neueste und einzige vom CertificateObject implementierte Schnittstelle **** ist. coclass-Schnittstelle. Genau wie bei der Verwendung von InfoPath-COM-Objekten aus einem Skript wird die [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) Accessor-Eigenschaft verwendet, um auf das Objekt vom übergeordneten Element aus zuzugreifen. 
  
Dasselbe Muster wird auch auf die Schnittstellen für Auflistungen angewendet, wobei an die Coklassen-Schnittstelle für eine Auflistung "Collection" an den Namen angefügt ist anstelle von "Object". Die coclass-Schnittstelle für die COM-DataAdapters-Auflistung heißt beispielsweise dataAdaptercollection, und die von ihr implementierte Schnittstelle ist die DataAdapters-Schnittstelle. **** [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) Entsprechend wird die [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) DataAdapters-Accessor-Eigenschaft des übergeordneten **XDocument** -Objekts verwendet, um auf die Auflistung zuzugreifen. 
  
Es gibt drei Ausnahmen für dieses Benennungsmuster. Die coclass-Schnittstellen für die COM- **Anwendung** und die **XDocument** -Objekte haben keine "Object" an ihre Namen angefügt. Ihre Namen sind identisch mit den entsprechenden COM-Objekten: [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) und **XDocument**. Darüber hinaus wird den Namen der Schnittstellen, die von den Co-Klassen Schnittstellen **Application** und **XDocument** implementiert werden, das Unterstrichzeichen (_) vorangestellt: [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) und [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . Die dritte Ausnahme ist das COM- **DataObject** -Objekt. Die coclass-Schnittstelle für dieses Objekt heißt [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) DataSourceObject, aber genau wie andere InfoPath-COM-Objekte ist die Schnittstelle, die Sie implementiert, die [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) -Schnittstelle. 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Wie Microsoft XML Core Services (MSXML) 5,0 für Microsoft Office-Objekte für das InfoPath 2003-kompatible Objektmodell verfügbar gemacht werden

Eine Teilmenge der Objekte und Member des Objektmodells, die von Microsoft XML Core Services (MSXML) bereitgestellt werden, die auch ein COM-Server ist, werden von Schnittstellen umschlossen, die von der Interop-Assembly Microsoft. Office. Interop. InfoPath. SemiTrust verfügbar gemacht werden. Der Grund dafür ist, dass einige der Elemente des InfoPath-COM-Objektmodells auf MSXML basieren und auf sichere Weise auf diese Member zugreifen können müssen. Die Namen von Schnittstellen im **Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace, die die Objekte und Member des MSXML-Objektmodells umschließen, sind identisch mit den Namen, die vom MSXML-com-Server angezeigt werden. In den meisten Fällen werden diese Namen mit "IXMLDOM" vorangestellt, da Sie für die Arbeit mit dem XML-DOM (Document Object Model) verwendet werden. Beispielsweise gibt die [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) -Eigenschaft der **XDocument** -Schnittstelle, die verwendet wird, um einen Verweis auf das einem Formular zugrunde liegende XML-Dokument zurückzugeben, die [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) -Schnittstelle zurück, die von der Microsoft. Office. Interop. InfoPath. SemiTrust-Interop-Assembly. Sie rufen und verwenden die Member der **IXMLDOMDocument** -Schnittstelle im Grunde auf die gleiche Weise wie bei der Verwendung von Skripts in Formularvorlagen, die keinen verwalteten Code verwenden. 
  
Weitere Informationen zum Verwenden von Mitgliedern des Microsoft XML Core Services (MSXML) für Microsoft Office-Objektmodell in Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit MSXML und System. XML mithilfe des InfoPath-Objektmodells 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

Für den Großteil des Codes, den Sie mit dem InfoPath 2003-kompatiblen Objektmodell in einer Formularvorlage mit verwaltetem Code schreiben, verwenden `thisXDocument` Sie `thisApplication` die und-Variablen, die `_Startup` in der Methode der standardmäßigen FormCode.cs-oder FormCode. vb-Klassendatei initialisiert werden. `thisXDocument` Sie können die-und `thisApplication` -Variablen verwenden, um auf die Member der Benutzeroberflächen [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) und [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Co-Klasse zuzugreifen. Nachdem Sie den Namen einer Variablen gefolgt von einem Punkt eingegeben haben, werden die Listenelemente der entsprechenden coclass-Schnittstelle angezeigt. Sie können auf diese Weise fortfahren, um auf das Objektmodellelement zuzugreifen, mit dem Sie arbeiten möchten. 
  
Nachfolgend sehen Sie ein einfaches Beispiel, in `thisXDocument` dem die Variable für den Zugriff auf die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode verwendet wird, um die Version der InfoPath-Anwendung mithilfe `thisApplication` der [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) -Eigenschaft anzuzeigen, auf die von der Variablen zugegriffen wird. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Verwenden der Referenzdokumentation zur Klassenbibliothek

Die Organisation der Referenzdokumentation des **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace spiegelt die Beziehungen zwischen Coklassen-Schnittstellen und den geerbten Schnittstellen wider, die sie implementieren. Dies wird weiter oben in diesem Thema im Abschnitt "Verfügbarmachen von COM-Objekten für verwalteten Code" erläutert. 
  
Auch wenn die Organisation und Benennung der Referenzdokumentation des **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace zunächst etwas verwirrend erscheinen mag, sind die Themen grundsätzlich genau so organisiert wie die Referenz zum InfoPath-Objektmodell, die Bestandteil der InfoPath Developer-Referenz ist und in InfoPath enthalten ist. Mit Ausnahme der Themen für die Schnittstellen **Application** und **XDocument** sind alle Themen zur COM-Coklassen-Schnittstelle den entsprechenden Themen "Object" und "Collection" der InfoPath-Skriptreferenz zugeordnet. So entsprechen beispielsweise die Themen "UIObject-Schnittstelle" und "WindowsCollection-Schnittstelle" der Referenzdokumentation für den **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace demselben Inhalt der Themen "UI-Objekt" und "Windows-Auflistung" der Skriptreferenz zur Referenz für das InfoPath-Objektmodell. 
  
Der Link zu den Membern der Coklassen-Schnittstelle nach der Beschreibung der Schnittstelle am Anfang des Themas verweist allerdings auf ein leeres Thema. Sie müssen zum Anzeigen der Liste mit Membern, die von der Coklassen-Schnittstelle implementiert werden, das Thema für die aktuellste Schnittstelle öffnen, die von der Coklasse geerbt wird, und dann die Tabelle ihrer Member öffnen. Sie finden einen Link zu der geerbten Schnittstelle am Anfang des Themas zur Coklassen-Schnittstelle im Abschnitt "Hinweise".
  
Wenn Sie im Code-Editor auf F1 drücken, ist das Verhalten ähnlich, abgesehen davon, dass der Member, für den Sie die Hilfe mithilfe von F1 aufrufen, direkt angezeigt wird, da Sie mit großer Wahrscheinlichkeit mit Membern einer Schnittstelle arbeiten werden. Dennoch kann die Tatsache, dass ein Member von einer versionsspezifischen Schnittstelle implementiert werden kann, zunächst verwirrend erscheinen. Wenn Sie beispielsweise den Cursor `thisXDocument.UI.Alert` eingeben und auf `Alert` F1 drücken, wird ein Thema mit dem Titel "UI2. Alert-Methode "wird angezeigt. Dies ist der Fall, da die **Alert**-Methode eine Implementierung eines Members der **UI2**-Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an InfoPath-Objektmodellelemente

Wenn ein InfoPath 2003-kompatibles Objektmodellmember einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie stattdessen das **Type.Missing**-Feld für diesen Parameter übergeben. Wenn das **Type.Missing**-Feld nicht angegeben wird und ein tatsächlicher Wert ausgelassen wird, führt dies zu einem Buildfehler. Dies trifft sowohl auf in Visual C# als auch auf in Visual Basic geschriebenen Code zu. Die [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) -Methode der ViewObject-Schnitt [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) Stelle enthält beispielsweise zwei optionale Parameter: _varEndNode_ und _varViewContext_. Eine Codezeile, in der keine tatsächlichen Werte für diese optionalen Parameter angegeben sind, sollte wie in den folgenden Beispielen dargestellt aussehen.
  
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

### <a name="about-common-language-specification-compliance"></a>Informationen zur Kompatibilität von Common Language Specification

Bei jeder Schnittstelle und jedem Member in der Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly ist das entsprechende **CLSCompliant**-Attribut intern auf **false** festgelegt. Da die Referenzdokumentation teilweise mithilfe von **System.Reflection** generiert wird, ist an die Beschreibung jeder Schnittstelle und jedes Members der Satz "Diese Schnittstelle/Methode/Eigenschaft ist nicht CLS-kompatibel" angefügt. Die meisten Schnittstellen und Member des [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespaces sind jedoch tatsächlich CLS-kompatibel. 
  
## <a name="see-also"></a>Siehe auch

- [Allgemeine Aufgaben für das Entwickeln der Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Erstellen von Formularvorlagen mit dem InfoPath-Objektmodell 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Grundlegendes zum InfoPath 2003-Objektmodell](understanding-the-infopath-2003-object-model.md)

