---
title: Mit InfoPath 2003 kompatible Objektmodelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Objektmodell, InfoPath 2003-kompatibles Objektmodell,Objektmodelle [InfoPath 2003], kompatibel mit InfoPath 2007,Objektmodelle [InfoPath 2007], InfoPath 2003-kompatibel
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath wird als COM(Component Object Model)-Anwendung geschrieben und macht seine Programmierschnittstellen für externe Automatisierung und Formularvorlagenskripts als COM-Schnittstellen verfügbar.
ms.openlocfilehash: f3351a0fee6e23de0785aa28b0970c6a90361f16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303521"
---
# <a name="infopath-2003-compatible-object-models"></a>Mit InfoPath 2003 kompatible Objektmodelle

Microsoft InfoPath wird als COM(Component Object Model)-Anwendung geschrieben und macht seine Programmierschnittstellen für externe Automatisierung und Formularvorlagenskripts als COM-Schnittstellen verfügbar. Als Unterstützung für die Erstellung von InfoPath-Projektmappen, in denen die Programmiersprachen Visual C# und Visual Basic mit verwaltetem Code verwendet werden, werden vom InfoPath-Setupprogramm drei Interop-Assemblys installiert. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. 
  
Die Dateien für die von InfoPath installierten drei Interop-Assemblys lauten:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
In diesem Thema wird das Objektmodell erläutert, das über die Microsoft.Office.Interop.InfoPath.SemiTrust-Interop-Assembly offen gelegt wird, die ausschließlich zum Schreiben und Ausführen von Geschäftslogik mit verwaltetem Code innerhalb von InfoPath-Formularvorlagen (XSN) verwendet wird.  
  
Weitere Informationen zu Microsoft. Office.Interop.InfoPath- und Microsoft.Office.Interop.InfoPath.Xml-Assemblys finden Sie in der Dokumentation für die [Microsoft.Office.Interop.InfoPath-](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) undMicrosoft.Office.Interop.InfoPath.Xml-Namespaces. [](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) 
  
## <a name="important-installation-information"></a>Wichtige Installationsinformationen

Standardmäßig werden  mit der Standardinstallationsoption des InfoPath-Setupprogramms Kopien von Microsoft installiert. Office.Interop.InfoPath.SemiTrust und Microsoft.Office.Interop.InfoPath.Xml Assemblys im Ordner C:\Programme\Microsoft Office\Office14. The Microsoft. Office.Interop.InfoPath- und Microsoft.Office.Interop.InfoPath.Xml-Assemblys werden auch im globalen Assemblycache (Global Assembly Cache, GAC) installiert, dessen Inhalt aus dem Ordner "C:\Windows\Assembly" angezeigt werden kann. 
  
Wenn diese Assemblys nicht installiert sind, sollten Sie bestätigen, dass Microsoft InfoPath ordnungsgemäß installiert wurde. Solange das .NET Framework 2.0 oder höher installiert ist, bevor setup ausgeführt wird, ist die **Option .NET Programmierbarkeitsunterstützung** im InfoPath-Setupprogramm auf **Von** Meinem Computer ausführen für eine typische Installation von InfoPath festgelegt.  Wenn diese Interopassemblys auf Ihrem Computer nicht verfügbar sind, müssen Sie bestätigen, dass .NET Framework 2.0 oder  höher installiert ist, und dann Programme aus der Systemsteuerung hinzufügen oder entfernen ausführen und die **Option .NET-Programmierbarkeitsunterstützung** auf  **Von** Meinem Computer ausführen festlegen.
  
Informationen zum Herunterladen der .NET Framework 2.0 Redistributable finden Sie [unter .NET Framework 2.0 Redistributable.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>The Microsoft. Office.Interop.InfoPath.SemiTrust Namespace

Vor der Veröffentlichung von Microsoft Office InfoPath 2003 Service Pack 1 und Microsoft Office InfoPath 2003 Toolkit für Visual Studio® .NET wurde die gesamte Programmierlogik für InfoPath-Formularvorlagen mithilfe von Microsoft JScript oder Microsoft VBScript erstellt, das in der Microsoft Script Editor-Entwicklungsumgebung (MSE) geschrieben wurde. Ein in MSE geschriebenes Skript wird zur Laufzeit interpretiert und greift auf das COM-Objektmodell zu, das von der Dynamic Link Library IPEDITOR.dll verfügbar gemacht wird.
  
Zur Unterstützung der Erstellung von Formularvorlagen, die Sprachen mit verwalteten Code wie Visual C# und Visual Basic für die Programmierlogik verwenden, wurde InfoPath Funktionalität hinzugefügt, um das Hosten der Common Language Runtime (CLR) und von Microsoft zu ermöglichen. Office.Interop.InfoPath.SemiTrust-Interop-Assembly wurde erstellt, um verwalteten Code für die sichere Zusammenarbeit mit dem COM-Objektmodell zu aktivieren, das von InfoPath verfügbar gemacht wird. Informationen zum Sicherheitsmodell, das für Formularvorlagen mit verwalteten Code in InfoPath gilt, finden Sie unter Informationen zum Sicherheitsmodell für [Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md). 
  
Obwohl das Schreiben von verwalteten Code für eine bestimmte Aufgabe in einer InfoPath-Formularvorlage dem Ausführen der gleichen Programmieraufgabe durch Schreiben eines Skripts sehr ähnlich ist, sieht das InfoPath 2003-kompatible Objektmodell, das beim Anzeigen des **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** aus dem Objektbrowser **in** Visual Studio 2012 verfügbar gemacht wird, wesentlich komplexer aus. Dies liegt daran, dass die .NET Framework-Interoperabilitätstechnologie, die zur Unterstützung des InfoPath 2003-kompatiblen Objektmodells verwendet wird, einen COM-Server benötigt, um alle öffentlichen Schnittstellen sowie einige zusätzliche Konstrukte verfügbar zu machen, die von der .NET Framework selbst erforderlich sind. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>So werden COM-Objekte für das infoPath 2003-kompatible Objektmodell verfügbar gemacht

Bei der systemeigenen Arbeit mit einem COM-Server mit Programmiersprachen hoher Ebene, beispielsweise JScript, VBScript oder Visual Basic (jedoch nicht die .NET-Versionen von Visual Basic und Visual C#), ist das offen gelegte Objektmodell einfacher als die zugrunde liegenden COM-Klassen und Schnittstellen. So legt das **UI**-Objekt von InfoPath bei der Arbeit mit diesen Sprachen eine Gruppe mit sieben Methoden offen, beispielsweise die **Alert**-Methode, um ein Meldungsfeld für Benutzer anzuzeigen. 
  
Die zugrunde liegenden COM-Konstrukte, die das **UI**-Objekt unterstützen, bestehen jedoch aus drei Entitäten: Zwei Schnittstellen mit Namen **UI** und **UI2** sowie einer COM-Coklasse, die die Member dieser beiden Schnittstellen implementiert. Es gibt zwei Versionen der **UI**-Schnittstelle, da das COM-Framework die Definition einer fest bestehenden Schnittstelle benötigt, um Rückwärtskompatibilität für Programme und Komponenten beizubehalten, die eine Implementierung dieser Schnittstelle aufrufen.  
  
In diesem Fall  stellt die Benutzeroberflächenschnittstelle, die für die erste Version von InfoPath definiert wurde, vier Methoden bereit, einschließlich der **Alert-Methode.** Die **UI2-Schnittstelle** kann als zweite  Version der Benutzeroberfläche betrachtet werden, und sie wurde für die InfoPath Service Pack 1-Version definiert. Die **UI2-Schnittstelle** erbt die  vier Methoden der ursprünglichen Benutzeroberflächenschnittstelle und fügt drei neue Methoden hinzu, z. B. **die Confirm-Methode.** Obwohl Sie eine Codezeile entweder in Skript oder verwalteten Code schreiben können, der die **Confirm-Methode** mithilfe aufruft, ruft der zugrunde liegende Code tatsächlich die Confirm-Methode der UI2-Schnittstelle aus der Implementierung dieser Methode in der `XDocument.UI.Confirm`  COM-Coclass auf.  
  
Wenn das Objektmodell für das Scripting offen gelegt wird, blendet es diese Details zwar aus, die Interop-Assembly, die für die Arbeit mit einem COM-Server für den verwalteten Code erforderlich ist, legt die Coklasse und beide Schnittstellen jedoch öffentlich offen. Für das einzelne, in der MSE-Scriptingumgebung verwendete **UI**-Objekt legt der **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace die folgenden drei Elemente offen: 
  
- [Benutzeroberflächenschnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) 
    
- [UI2-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
    
- [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) UIObject-Coclass-Schnittstelle 
    
Obwohl alle drei dieser Schnittstellen im  Objektbrowser verfügbar gemacht werden und in der Klassenbibliotheksdokumentation für den Namespace enthalten  sind, arbeiten Sie nur mit der UIObject-Coklassenschnittstelle, die das UI-Objekt implementiert, und mit den Mitgliedern der **UI2-Schnittstelle,** der aktuellsten Version der Schnittstelle, die von der **UIObject-Coklassenschnittstelle** implementiert wird.  Um wie im Skript über das übergeordnete [XDocument-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) auf die UiObject-Coclass-Schnittstelle zu zugreifen, verwenden Sie die  [UI-Accessor-Eigenschaft.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) Mit Ausnahme weniger beachtenswerter Ausnahmen ist dies das Muster für alle Objekte aus der ursprünglichen Version von InfoPath, die bei der Veröffentlichung von InfoPath Service Pack 1 aktualisiert wurden. 
  
Das Muster ist zwar grundsätzlich dasselbe, dennoch ist die Situation bei völlig neuen Objekten etwas einfacher, die in InfoPath Service Pack 1 hinzugefügt wurden, beispielsweise dem **Certificate**-Objekt. In diesem Fall müssen nur zwei Elemente verwendet werden: die Coclass-Schnittstelle [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) und die Member der [Zertifikatschnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) die die neueste und einzige Schnittstelle ist, die von der Coclass-Schnittstelle **CertificateObject** implementiert wurde. Genau wie bei der Verwendung von [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) InfoPath COM-Objekten aus dem Skript wird die Zertifikatzugriffseigenschaft verwendet, um vom übergeordneten Objekt aus auf das Objekt zu zugreifen. 
  
Dasselbe Muster wird auch auf die Schnittstellen für Auflistungen angewendet, wobei an die Coklassen-Schnittstelle für eine Auflistung "Collection" an den Namen angefügt ist anstelle von "Object". Die Coclass-Schnittstelle für die COM **DataAdapters-Auflistung** heißt beispielsweise [DataAdaptersCollection,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) und die implementierte Schnittstelle ist [die DataAdapters-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) Auf ähnliche Weise wird die [DataAdapters-Accessoreigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) des **übergeordneten XDocument-Objekts** für den Zugriff auf die Auflistung verwendet. 
  
Es gibt drei Ausnahmen für dieses Benennungsmuster. Die Coclass-Schnittstellen für die **COM-Anwendung** und **die XDocument-Objekte** verfügen nicht über "Object" an ihre Namen. Ihre Namen sind identisch mit den entsprechenden COM-Objekten: [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) und **XDocument**. Darüber hinaus erhalten die Namen der Schnittstellen, die von den Schnittstellen **Application** und **XDocument** implementiert werden, das Präfix unter dem Unterstrich (_): [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) und [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . Die dritte Ausnahme ist das COM **DataObject-Objekt.** Die Coclass-Schnittstelle für dieses Objekt heißt [DataSourceObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) aber genau wie andere InfoPath COM-Objekte ist die implementierte Schnittstelle die [DataObject-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Wie Microsoft XML Core Services (MSXML) 5.0 für Microsoft Office für das infoPath 2003-kompatible Objektmodell verfügbar gemacht werden

Eine Teilmenge der Objekte und Elemente des Von Microsoft XML Core Services (MSXML) bereitgestellten Objektmodells, das auch ein COM-Server ist, wird von Schnittstellen umschlossen, die von Microsoft verfügbar gemacht werden. Office.Interop.InfoPath.SemiTrust-Interop-Assembly. Der Grund dafür ist, dass einige Mitglieder des InfoPath COM-Objektmodells auf MSXML und in der Lage sein müssen, auf diese Elemente auf sichere Weise zu zugreifen. Die Namen der Schnittstellen im **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace,** die die Objekte und Elemente des MSXML-Objektmodells umschließen, sind identisch mit den Namen, die vom MSXML-COM-Server verfügbar gemacht werden. In den meisten Fällen wird diesen Namen das Präfix IXMLDOM vorangestellt, da sie für die Verwendung mit dem XML Document Object Model (DOM) verwendet werden. Die [DOM-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) der **XDocument-Schnittstelle,** die zum Zurückgeben eines Verweises auf das einem Formular zugrunde liegende XML-Dokument verwendet wird, gibt beispielsweise die [IXMLDOMDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) zurück, die von Microsoft umschlossen wird. Office.Interop.InfoPath.SemiTrust-Interop-Assembly. Sie rufen die Mitglieder der **IXMLDOMDocument-Schnittstelle** auf und verwenden sie im Wesentlichen auf die gleiche Weise wie bei der Verwendung von Skripts in Formularvorlagen, die keinen verwalteten Code verwenden. 
  
Weitere Informationen zur Verwendung von Mitgliedern des Microsoft XML Core Services (MSXML) für Microsoft Office-Objektmodell in Formularvorlagen mit verwalteten Code finden Sie unter Arbeiten mit MSXML und System.Xml Verwenden des [InfoPath 2003-Objektmodells.](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
### <a name="using-intellisense"></a>Verwenden von IntelliSense

Für den Großteil des Codes, den Sie für das InfoPath 2003-kompatible Objektmodell in einer Formularvorlage mit verwalteten Code schreiben, verwenden Sie die Und-Variablen, die in der Methode der Standardmäßigen  `thisXDocument`  `thisApplication`  `_Startup` Klassendatei FormCode.cs oder FormCode.vb initialisiert werden. Sie können die Und-Variablen verwenden, um auf die Member der `thisXDocument` `thisApplication` [XDocument-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) und Application-Coclass-Schnittstellen zu zugreifen. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Nachdem Sie den Namen einer variablen gefolgt von einem Zeitraum eingeben, zeigt IntelliSense Abschluss der Anweisung die Listenmitglieder der entsprechenden Coclass-Schnittstelle an. Sie können auf diese Weise fortfahren, um auf das Objektmodellmitglied zu zugreifen, mit dem Sie arbeiten möchten. 
  
Im folgenden Beispiel wird ein einfaches Beispiel gezeigt, in dem die Variable zum Zugreifen auf die Alert-Methode verwendet wird, um die Version der InfoPath-Anwendung mithilfe der Version-Eigenschaft, auf die über die Variable `thisXDocument` zugegriffen [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) `thisApplication` wird, angezeigt zu werden. 
  
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
  
Wenn Sie im Code-Editor auf F1 drücken, ist das Verhalten ähnlich, abgesehen davon, dass der Member, für den Sie die Hilfe mithilfe von F1 aufrufen, direkt angezeigt wird, da Sie mit großer Wahrscheinlichkeit mit Membern einer Schnittstelle arbeiten werden. Dennoch kann die Tatsache, dass ein Member von einer versionsspezifischen Schnittstelle implementiert werden kann, zunächst verwirrend erscheinen. Wenn Sie z. B. den Cursor eingeben und platzieren und F1 drücken, wird ein Thema mit dem Titel  `thisXDocument.UI.Alert`  `Alert` "UI2. Alert Method" wird angezeigt. Dies ist der Fall, da die **Alert**-Methode eine Implementierung eines Members der **UI2**-Schnittstelle ist. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Übergeben optionaler Parameter an Elemente des InfoPath-Objektmodells

Wenn ein InfoPath 2003-kompatibles Objektmodellmember einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie stattdessen das **Type.Missing**-Feld für diesen Parameter übergeben. Wenn das **Type.Missing**-Feld nicht angegeben wird und ein tatsächlicher Wert ausgelassen wird, führt dies zu einem Buildfehler. Dies trifft sowohl auf in Visual C# als auch auf in Visual Basic geschriebenen Code zu. Die [SelectNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) der [ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) enthält beispielsweise zwei optionale Parameter:  _varEndNode_ und  _varViewContext_. Eine Codezeile, in der keine tatsächlichen Werte für diese optionalen Parameter angegeben sind, sollte wie in den folgenden Beispielen dargestellt aussehen.
  
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

### <a name="about-common-language-specification-compliance"></a>Informationen zur Einhaltung gängiger Sprachspezifikationen

Bei jeder Schnittstelle und jedem Member in der Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly ist das entsprechende **CLSCompliant**-Attribut intern auf **false** festgelegt. Da die Referenzdokumentation teilweise mithilfe von **System.Reflection** generiert wird, ist an die Beschreibung jeder Schnittstelle und jedes Members der Satz "Diese Schnittstelle/Methode/Eigenschaft ist nicht CLS-kompatibel" angefügt. Die meisten Schnittstellen und Member des [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespaces](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) sind jedoch CLS-kompatibel. 
  
## <a name="see-also"></a>Siehe auch

- [Allgemeine Aufgaben für das Entwickeln der Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Grundlegendes zum InfoPath 2003-Objektmodell](understanding-the-infopath-2003-object-model.md)

