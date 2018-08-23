---
title: Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007-Objektmodellen, modelliert Objekt [InfoPath 2007] – InfoPath 2007-entwicklungsumgebungen
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen zum Entwickeln von Geschäftslogik in Formularvorlagen und externe Automatisierung aus verwaltetem Code unterstützt.
ms.openlocfilehash: 638306eabf9f761ff126953e66228cad8cc5c3ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579529"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Grundlegendes zu InfoPath-Objektmodellen und zur Entwicklungsumgebung

Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen zum Entwickeln von Geschäftslogik in Formularvorlagen und externe Automatisierung aus verwaltetem Code unterstützt.
  
InfoPath Forms Services in SharePoint Server 2013 verfügbar ist, bietet eine Web Browser für Ausfüllen von InfoPath-Formularen. Wenn auf einem Server bereitgestellt, die ausgeführt wird werden InfoPath Forms Services, Formulare, die auf browserkompatiblen Formularvorlagen (XSN) in einem Webbrowser von Computern öffnen können, die keine InfoPath installiert haben, aber sie in InfoPath geöffnet, wenn es installiert ist. InfoPath Forms Services außerdem ein Objektmodell zum Automatisieren von Serveraufgaben im Zusammenhang mit der InfoPath-Formular Vorlage Veröffentlichung und Verwaltung.
  
InfoPath 2013 unterstützt die Visual Studio 2012 Programmieraufgaben Umgebung und die zugehörigen Programmiersprachen, die weiter unten in diesem Thema beschrieben sind.
  
## <a name="infopath-programming-models"></a>InfoPath-Programmiermodelle

InfoPath 2013 werden zwei Objektmodelle zum Entwickeln von Geschäftslogik in Formularvorlagen unterstützt:
  
- Das InfoPath-Objektmodell mit verwaltetem Code
    
- Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code
    
Darüber hinaus kann in InfoPath 2013 Schreiben von verwaltetem Code für die Automatisierung von InfoPath aus einer externen Anwendung.
  
InfoPath Forms Services stellt ein Objektmodell zum Automatisieren von Serveraufgaben, wie überprüfen und Hochladen von Formularvorlagen zwischen Code, ausgeführt wird, auf dem Server, der Server-Administratorzugriff und Berechtigungen erforderlich sind.
  
> [!NOTE]
> Das InfoPath Filler 2013 können öffnen, und führen InfoPath-Formular Vorlage Lösungen in früheren Versionen von InfoPath, die mit Skriptsprachen (JScript und VBScript) geschriebene Geschäftslogik verwenden erstellt. InfoPath Designer 2010 unterstützt jedoch nicht erstellen oder Ändern von Formularvorlagen, die mit dem Skript geschriebene Geschäftslogik verwenden. 
  
### <a name="the-infopath-managed-code-object-model"></a>Das InfoPath-Objektmodell mit verwaltetem Code

Das Objektmodell für verwalteten Code InfoPath 2013 ist in zwei Assemblys implementiert beide Microsoft.Office.Infopath.dll lauten.
  
Eine Version der Assembly implementiert eine Teilmenge des InfoPath-Objektmodells, die enthält nur die Typen und Elemente, die in der Geschäftslogik von als browserfähige Formularvorlagen, die auf SharePoint Server 2013 mit ausgeführt bereitgestellte Formularvorlagen unterstützt werden InfoPath Forms Services. Formularvorlagen mit Geschäftslogik für die Assembly geschrieben geöffnet und in InfoPath Filler und in einem Webbrowser ausgeführt.
  
Die andere Version der Assembly implementiert zusätzliche Typen und Elemente, die Funktionen bereitzustellen, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird. Formularvorlagen mit Geschäftslogik, die zusätzliche Klassen und Member in dieser Assembly verfasste geöffnet und nur im Editor InfoPath Filler ausgeführt.
  
> [!NOTE]
> Es ist möglich, schreiben, dass bedingter Logik, der den Eigenschaften der [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse verwendet, die bestimmen, welche Umgebung (InfoPath Filler oder einem Webbrowser) die Formularvorlage ausgeführt wird. Mithilfe dieser bedingten Logik kann Ihre Geschäftslogik zwischen, die in einem Webbrowser funktioniert und Klassen und Member, die nur in InfoPath Filler-Editor arbeiten verfasste Code verzweigen. Weitere Informationen finden Sie unter [Schreiben von bedingter Logik, bestimmt die Laufzeit - Umgebung](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
Die Assembly, die InfoPath beim Hinzufügen und von Geschäftslogik für die Formularvorlage Kompilieren verwendet wird, hängt davon ab, ob Sie die Formularvorlage **Leeres Formular** oder **Leeres Formular (InfoPath Filler)** auf der Registerkarte **neu** von der Microsoft Office Backstage auswählen Wenn Sie beginnen, ein neues Formular im InfoPath-Designer entwerfen. Mithilfe der Formularvorlage **Leeres Formular** erstellten Formulare verwenden Sie die Assembly, die enthält nur die Typen und Elemente, die in der Geschäftslogik von als browserfähige Formularvorlagen bereitgestellte Formularvorlagen unterstützt werden. Mithilfe der Formularvorlage **Leeres Formular** erstellten Formulare können in einem Webbrowser und InfoPath Filler geöffnet werden. Mithilfe der Formularvorlage **Leeres Formular (InfoPath Filler)** erstellten Formulare verwenden Sie die Assembly, die implementiert zusätzliche Typen und Member, die Funktionalität, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird bereitstellen, und kann nur in InfoPath Filler geöffnet. 
  
> [!TIP]
> Nach dem start eine Formularvorlage entwerfen, können Sie ändern, welche Assembly durch Ändern der kompatibilitätseinstellungen Formular verwendet wird. Klicken Sie dazu klicken Sie auf der Registerkarte **Entwickler** auf **Sprache** , und klicken Sie dann in der Liste **Kategorie** auf **Kompatibilität** . Wählen Sie in der Liste **Formulartyp** **Webbrowserformular** zum Erstellen eines Formulars, das als einer browserkompatiblen auf SharePoint Server 2013 bereitgestellt werden können. Wählen Sie **InfoPath Filler Formular** zum Erstellen eines Formulars, das nur im Editor InfoPath Filler ausgeführt werden kann. Die anderen Auswahlmöglichkeiten in der Liste **Formulartyp** bieten Unterstützung für Kompatibilität mit InfoPath 2007 und InfoPath 2003. 
  
Die Klassen und Member beider Versionen dieses Objektmodell werden über den [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace verfügbar gemacht. Die folgende Tabelle enthält, in dem die Assemblys in den Verzeichnissen der InfoPath 2013 Installation befinden. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (befindet sich in C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |Die Teilmenge des Objektmodells, die enthält nur Typen und Elemente, die in der Geschäftslogik einer Formularvorlage auf einem Server bereitgestellt ausgeführt wird, InfoPath Forms Services ausgeführt werden.  <br/> |
|Microsoft.Office.InfoPath.dll (befindet sich in C:\Program Files\Microsoft Office\Office15\InfoPathOM)  <br/> |Das "vollständige" Objektmodell mit Typen und Membern, die nicht in der Geschäftslogik einer Formularvorlage in InfoPath Forms Services bereitgestellt ausgeführt wird.  <br/> |
   
> [!NOTE]
> Die weiter oben in diesem Abschnitt genannten Assemblys werden zur Entwurfszeit verwendet, wenn Sie schreiben und kompilieren Sie Code. Zur Laufzeit die Assembly verwendet, wenn eine Formularvorlage in InfoPath geöffnet wird in den globalen Assemblycache (GAC) des Computers befindet sich auf dem InfoPath installiert ist. Wenn eine Formularvorlage in einem Webbrowser auf einem Server, der InfoPath Forms Services ausgeführt wird geöffnet wird, befindet sich die Assembly verwendet, auf dem Server. 
  
Bereitstellen von zwei Assemblys wird sichergestellt, dass Ihre Geschäftslogik nur Aufrufe an das entsprechende Objektmodellelemente für den unterstützten Formular-Editoren (Web-Browser oder InfoPath Filler) enthalten soll. Beispielsweise wenn Sie Ihr Code, IntelliSense-Features wie etwa Abschluss der Anweisung bearbeiten und Inline-Dokumentation nur anzeigen und Arbeiten mit den entsprechenden Objektmodellelemente für Ihr Formular-Editoren Ziel.
  
In beiden Versionen von das Objektmodell für verwalteten Code verfügbar gemacht werden, durch die Assembly Microsoft.Office.InfoPath, navigieren und Aktualisieren von XML-Datenspeicher in Geschäftslogik Aufrufe der Member der t: **System.Xml.XPath.XPathNavigator** Klasse erfordert. In InfoPath 2003 navigieren und Aktualisieren von XML-Datenspeicher erfordert das Aufrufen der Member des MSXML-Klassen (für Geschäftslogik, die mit JScript oder VBScript erstellt) oder durch Aufrufen über die Wrapper für MSXML, die Klassen durch die **bereitgestellt werden Microsoft.Office.Interop.InfoPath.SemiTrust** -Namespace (für Geschäftslogik mit c# oder Visual Basic und dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET erstellt). 
  
Verwenden von Membern der **XPathNavigator** -Klasse den gleichen Code für die Geschäftslogik DOM-Bearbeitung für Formularvorlagen unterstützt, die im InfoPath-Client und webfähigen Formularen, die von SharePoint Server 2013 mit InfoPath-Formulare geöffnet geöffnet werden können Dienste in einem Webbrowser. 
  
Informationen zum Arbeiten mit Membern der **XPathNavigator** -Klasse in der Geschäftslogik von InfoPath Formularvorlagen mit verwaltetem Code, finden Sie unter [Arbeiten mit der "XPathNavigator" und "XPathNodeIterator" Klassen](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code

Das InfoPath 2003-kompatible Objektmodell für verwalteten Code wurde in InfoPath 2003 Service Pack 1 zusammen mit dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET zum Schreiben von Geschäftslogik in Formularvorlagen mit verwaltetem Code eingeführt. Dieses Objektmodell ist weiterhin von InfoPath 2013 die Kompatibilität mit InfoPath 2003 unterstützt.
  
Die Klassen und Member dieses Objektmodell werden über [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace verfügbar gemacht. Dieses Objektmodell ist in der folgenden Assemblydatei implementiert, die im Ordner "c:\Programme\Microsoft Office\Office14" befindet. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Stellt COM-Interop für das InfoPath-COM-Objektmodell für Formularvorlagen-Geschäftslogik mit c# oder Visual Basic geschrieben.  <br/> |
   
> [!NOTE]
> Obwohl das Erstellen der Geschäftslogik mit wird das COM-Interop-verwaltetem Code bereitgestellte Objektmodell der Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly von noch unterstützt InfoPath 2013 mit in-Objektmodell nicht unterstützt für geschriebene Geschäftslogik browserfähige Formularvorlagen in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt. Browserfähige Formularvorlagen müssen das InfoPath-Objektmodell für verwalteten Code für benutzerdefinierte Geschäftslogik verwenden. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatisieren von InfoPath aus verwaltetem Code

Zusätzlich zum Schreiben von Geschäftslogik mit verwaltetem Code können Entwickler Automatisierung von InfoPath mithilfe von verwaltetem Code in einer externen Anwendung ausgeführt wird. Diese Funktionalität und die Assemblys zum Schreiben von Code wurden in InfoPath 2003 Service Pack 1 eingeführt. Die Objekte und Member für die Automatisierung von InfoPath wurden aktualisiert, um zusätzliche Funktionalität bereitzustellen, beim Schreiben von Code für InfoPath 2013 externe Automatisierung.
  
Die Klassen und Member für die externe Automatisierung verwendet werden über die Namespaces [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) und [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) verfügbar gemacht. Die Assemblydateien, die für das Schreiben von Automatisierungscode erforderlich sind, befinden sich im Ordner "c:\Programme\Microsoft Office\Office14". 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Stellt COM-Interop für das InfoPath-COM-Objektmodell für externe Automatisierungscode mit c# oder Visual Basic geschrieben.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Stellt COM-Interop für MSXML für XML-DOM-Vorgänge in externem Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben ist.  <br/> |
   
Weitere Informationen über die Objektmodelle von die Namespaces **Microsoft.Office.Interop.InfoPath** und **Microsoft.Office.Interop.InfoPath.Xml** bereitgestellt, die dienen ausschließlich zum Automatisieren von InfoPath-Anwendung mithilfe von verwaltetem Code aus externen Anwendungen, finden Sie im [InfoPath Developer Center](http://msdn.microsoft.com/en-us/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>Das InfoPath Forms Services-Objektmodell

Das Objektmodell für verwalteten Code für die Automatisierung von Verwaltungsaufgaben für InfoPath Forms Services ist in der Microsoft.Office.InfoPath.Server.dll am implementiert \<Laufwerk\>: \Programme\Microsoft Office Server\15.0\Bin auf ein Microsoft SharePoint Server 2013-Installation.
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |Das Objektmodell zum Automatisieren von InfoPath Forms Services-Aufgaben wie beispielsweise hochladen, aktivieren oder Deaktivieren von browserfähigen Formularvorlagen.  <br/> |
   
Weitere Informationen zum Objektmodell für InfoPath Forms Services finden Sie in der SharePoint Server 2013 Software Entwickler Kit (SDK) auf MSDN verfügbar ist.
  
## <a name="infopath-development-environment"></a>InfoPath-Entwicklungsumgebung

Die Entwicklung von Geschäftslogik in Formularvorlagen für InfoPath 2013 kann mithilfe von Visual Studio 2012, mit dem [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) Add-on installiert ausgeführt werden. 
  
> [!NOTE]
> InfoPath 2013 unterstützt keine erstellen oder Bearbeiten von Formularvorlagen, die mit JScript oder VBScript geschriebene Geschäftslogik verwenden, obwohl InfoPath Filler öffnenden Skript-basierte Formularvorlagen unterstützt, die in früheren Versionen von InfoPath erstellt wurden. 
  
## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)
- [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

