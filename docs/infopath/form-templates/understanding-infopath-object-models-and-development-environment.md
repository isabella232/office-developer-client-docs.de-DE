---
title: Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, object models,object models [InfoPath 2007],InfoPath 2007, development environments
ms.localizationpriority: medium
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen für die Entwicklung von Geschäftslogik in Formularvorlagen und die externe Automatisierung aus verwaltetem Code.
ms.openlocfilehash: 99a72dda5e50f856fbf94c88e891f8a2a7e39d1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631286"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath

Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen für die Entwicklung von Geschäftslogik in Formularvorlagen und die externe Automatisierung aus verwaltetem Code.
  
InfoPath Forms Services, das in SharePoint Server 2013 verfügbar ist, bietet eine Webbrowseroberfläche zum Ausfüllen von InfoPath-Formularen. Wenn Formulare, die auf einem Server bereitgestellt werden, auf dem InfoPath Forms Services ausgeführt wird, können Formulare, die auf browserkompatiblen Formularvorlagen (XSN) basieren, in einem Webbrowser von Computern geöffnet werden, auf denen InfoPath nicht installiert ist, sie werden jedoch bei der Installation in InfoPath geöffnet. InfoPath Forms Services bietet auch ein Objektmodell zum Automatisieren von Serveraufgaben im Zusammenhang mit der Veröffentlichung und Verwaltung von InfoPath-Formularvorlagen.
  
InfoPath 2013 unterstützt die Visual Studio 2012-Programmierumgebung und die zugehörigen Programmiersprachen, die weiter unten in diesem Thema beschrieben werden.
  
## <a name="infopath-programming-models"></a>InfoPath-Programmiermodelle

InfoPath 2013 unterstützt zwei Objektmodelle für die Entwicklung von Geschäftslogik in Formularvorlagen:
  
- Das InfoPath-Objektmodell mit verwaltetem Code
    
- Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code
    
Darüber hinaus ermöglicht InfoPath 2013 das Schreiben von verwaltetem Code zum Automatisieren von InfoPath aus einer externen Anwendung.
  
InfoPath Forms Services stellt ein Objektmodell zum Automatisieren von Serveraufgaben bereit, z. B. das Überprüfen und Hochladen von Formularvorlagen aus auf dem Server ausgeführtem Code, der Zugriff und Berechtigungen des Serveradministrators erfordert.
  
> [!NOTE]
> InfoPath Filler 2013 kann InfoPath-Formularvorlagenlösungen öffnen und ausführen, die in früheren Versionen von InfoPath erstellt wurden und Geschäftslogik verwenden, die mit Skriptsprachen (JScript und VBScript) geschrieben wurde. Das Erstellen oder Ändern von Formularvorlagen, in denen mit Skripts geschriebene Geschäftslogik verwendet wird, wird von InfoPath Designer 2010 jedoch nicht unterstützt. 
  
### <a name="the-infopath-managed-code-object-model"></a>Das InfoPath-Objektmodell mit verwaltetem Code

Das InfoPath 2013-Objektmodell mit verwaltetem Code ist in zwei Assemblys implementiert, die beide Microsoft.Office.Infopath.dll benannt sind.
  
Eine Version der Assembly implementiert eine Teilmenge des InfoPath-Objektmodells, das nur die Typen und Member enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt werden, die auf SharePoint Server 2013 mit InfoPath Forms Services ausgeführt werden. Formularvorlagen mit Geschäftslogik, die für diese Assembly geschrieben wurde, werden im InfoPath Filler und in einem Webbrowser geöffnet und ausgeführt.
  
Die andere Version der Assembly implementiert zusätzliche Typen und Member mit Funktionalität, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird. Formularvorlagen mit Geschäftslogik, die für die zusätzlichen Klassen und Member in dieser Assembly geschrieben wurde, werden nur im InfoPath Filler-Editor geöffnet und ausgeführt.
  
> [!NOTE]
> Es ist möglich, bedingte Logik zu schreiben, die die Eigenschaften der [Environment-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) verwendet, um zu bestimmen, in welcher Umgebung (InfoPath Filler oder webbrowser) die Formularvorlage ausgeführt wird. Mithilfe dieser bedingten Logik kann Ihre Geschäftslogik zwischen Code verzweigen, der in einem Webbrowser funktioniert, und Code, der für Klassen und Member geschrieben wird, die nur im InfoPath Filler-Editor funktionieren. Weitere Informationen finden Sie unter [Schreiben von bedingter Logik, die die Laufzeitumgebung bestimmt.](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
Die Assembly, die InfoPath verwendet, wenn Sie Geschäftslogik für die Formularvorlage hinzufügen und kompilieren, hängt davon ab, ob Sie die Formularvorlage **"Leeres Formular"** oder **"Leeres Formular" (InfoPath Filler)** auf der Registerkarte **"Neu"** im Microsoft Office Backstage auswählen, wenn Sie mit dem Entwerfen eines neuen Formulars im InfoPath Designer beginnen. Formulare, die mit der Formularvorlage **Leeres Formular** erstellt wurden, verwenden die Assembly, die nur die Typen und Member enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt sind. Formulare, die mithilfe der Formularvorlage **"Leeres Formular"** erstellt wurden, können sowohl im Webbrowser als auch im InfoPath Filler geöffnet werden. Formulare, die mithilfe der **Formularvorlage "Leeres Formular" (InfoPath Filler)** erstellt wurden, verwenden die Assembly, die zusätzliche Typen und Member implementiert, die Funktionen bereitstellen, die in der Geschäftslogik browserfähiger Formularvorlagen nicht unterstützt werden und nur in InfoPath Filler geöffnet werden können. 
  
> [!TIP]
> Nachdem Sie mit dem Entwerfen einer Formularvorlage begonnen haben, können Sie ändern, welche Assembly verwendet wird, indem Sie die Formularkompatibilitätseinstellungen ändern. Hierzu klicken Sie auf **Sprache** auf der Registerkarte **Entwickler** und dann auf **Kompatibilität** in der Liste **Kategorie**. Wählen Sie in der **Formulartypliste** **das Webbrowserformular** aus, um ein Formular zu erstellen, das als browserkompatibles Formular auf SharePoint Server 2013 bereitgestellt werden kann. Wählen Sie **das InfoPath Filler-Formular** aus, um ein Formular zu erstellen, das nur im InfoPath Filler-Editor ausgeführt werden kann. Die anderen Auswahlen in der **Formulartypliste** unterstützen die Kompatibilität mit InfoPath 2007 und InfoPath 2003. 
  
Die Klassen und Member beider Versionen dieses Objektmodells werden über die [Microsoft.Office verfügbar gemacht. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) In der folgenden Tabelle sind die Assemblys in den Verzeichnissen einer InfoPath 2013-Installation aufgeführt. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (befindet sich in "C:\Programme\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices")  <br/> |Die Teilmenge des Objektmodells, das nur Typen und Member enthält, die in der Geschäftslogik einer Formularvorlage ausgeführt werden, die auf einem Server bereitgestellt wird, auf dem InfoPath Forms Services ausgeführt wird.  <br/> |
|Microsoft.Office.InfoPath.dll (befindet sich in "C:\Programme\Microsoft Office\Office15\InfoPathOM")  <br/> |Das "vollständige" Objektmodell, einschließlich Typen und Membern, die nicht in der Geschäftslogik einer Formularvorlage ausgeführt werden, die für InfoPath Forms Services bereitgestellt wird.  <br/> |
   
> [!NOTE]
> Die weiter oben in diesem Abschnitt genannten Assemblys werden zur Entwurfszeit beim Schreiben und Kompilieren von Code verwendet. Zur Laufzeit befindet sich die Assembly, die beim Öffnen einer Formularvorlage in InfoPath verwendet wird, im globalen Assemblycache (Global Assembly Cache, GAC) des Computers, auf dem InfoPath installiert ist. Wenn eine Formularvorlage in einem Webbrowser von einem Server geöffnet wird, auf dem InfoPath Forms Services ausgeführt wird, befindet sich die verwendete Assembly auf dem Server. 
  
Durch die Bereitstellung von zwei Assemblys wird sichergestellt, dass Ihre Geschäftslogik nur Aufrufe der entsprechenden Objektmodellmember für die unterstützten Formular-Editoren (Webbrowser oder InfoPath Filler) enthält. Wenn Sie beispielsweise Ihren Code bearbeiten, werden IntelliSense-Features wie die Vervollständigung von Anweisungen und die Inlinedokumentation nur für die entsprechenden Objektmodellmember für Die Zielformular-Editoren angezeigt und funktionieren mit diesen.
  
In beiden Versionen des objektmodells mit verwaltetem Code, das von Microsoft verfügbar gemacht wird. Office. InfoPath-Assembly, Navigieren und Aktualisieren von XML-Datenspeichern in Geschäftslogik erfordert Aufrufe an die Mitglieder der **System.Xml. XPath.XPathNavigator-Klasse.** In InfoPath 2003 Das Navigieren und Aktualisieren von XML-Datenspeichern erfordert das Aufrufen von Membern MSXML Klassen (für Geschäftslogik, die mit JScript oder VBScript erstellt wurde) oder das Aufrufen der Wrapper für MSXML Klassen, die vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellt werden (für Geschäftslogik, die mit C# oder Visual Basic und dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET erstellt wurde). 
  
Die Verwendung von Membern der **XPathNavigator-Klasse** ermöglicht den gleichen Geschäftslogikcode, um die DOM-Manipulation für Formularvorlagen zu unterstützen, die sowohl im InfoPath-Client als auch in webfähigen Formularen geöffnet werden, die von SharePoint Server 2013 mit InfoPath Forms Services in einem Webbrowser geöffnet werden. 
  
Informationen zum Arbeiten mit Membern der **XPathNavigator-Klasse** in der Geschäftslogik von InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code

Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code wurde in InfoPath 2003 Service Pack 1 zusammen mit dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET zum Schreiben von Geschäftslogik in Formularvorlagen mit verwaltetem Code eingeführt. Dieses Objektmodell wird weiterhin von InfoPath 2013 unterstützt, um Kompatibilität mit InfoPath 2003 bereitzustellen.
  
Die Klassen und Member dieses Objektmodells werden über den [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) verfügbar gemacht. Dieses Objektmodell ist in der folgenden Assemblydatei implementiert, die sich im Ordner "C:\Programme\Microsoft Office\Office14" befindet. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Stellt COM-Interoperabilität mit dem InfoPath-COM-Objektmodell für Geschäftslogik für Formularvorlagen bereit, die mit C# oder Visual Basic geschrieben wurde.  <br/> |
   
> [!NOTE]
> Das Erstellen von Geschäftslogik mithilfe des com-Interop-Objektmodells mit verwaltetem Code, das von Microsoft bereitgestellt wird. Office.Interop.InfoPath.SemiTrust-Assembly wird weiterhin von InfoPath 2013 unterstützt. Geschäftslogik, die mit diesem Objektmodell geschrieben wurde, wird für browserfähige Formularvorlagen, die auf SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, nicht unterstützt. Browserfähige Formularvorlagen müssen das InfoPath-Objektmodell mit verwaltetem Code für benutzerdefinierte Geschäftslogik verwenden. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatisieren von InfoPath aus verwaltetem Code

Zusätzlich zum Schreiben von Geschäftslogik mit verwaltetem Code können Entwickler InfoPath mithilfe von verwaltetem Code automatisieren, der in einer externen Anwendung ausgeführt wird. Diese Funktionalität und die zum Schreiben von Code erforderlichen Assemblys wurden in InfoPath 2003 Service Pack 1 eingeführt. Die Objekte und Member zum Automatisieren von InfoPath wurden aktualisiert, um zusätzliche Funktionen bereitzustellen, wenn Sie externen Automatisierungscode für InfoPath 2013 schreiben.
  
Die für die externe Automatisierung verwendeten Klassen und Member werden über [microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) und [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) Namespaces verfügbar gemacht. Die assembly files that are required for writing automation code are located in the C:\Program Files\Microsoft Office\Office14 folder. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Stellt COM-Interoperabilität mit dem InfoPath-COM-Objektmodell für externen Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben wurde.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Stellt COM-Interop für MSXML für XML-DOM-Vorgänge in externem Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben ist.  <br/> |
   
Weitere Informationen zu den Von **Microsoft.Office.Interop.InfoPath** bereitgestellten Objektmodellen und **Microsoft.Office.Interop.InfoPath.Xml** Namespaces, die ausschließlich zum Automatisieren der InfoPath-Anwendung mithilfe von verwaltetem Code aus externen Anwendungen verwendet werden, finden Sie im [InfoPath Developer Center.](https://msdn.microsoft.com/office/aa905434.aspx)
  
### <a name="the-infopath-forms-services-object-model"></a>Das InfoPath Forms Services-Objektmodell

Das Objektmodell mit verwaltetem Code zum Automatisieren InfoPath Forms Services Verwaltungsaufgaben ist in der Microsoft.Office.InfoPath.Server.dll implementiert, die sich unter \<drive\> :\Program Files\Microsoft Office Server\15.0\Bin auf einer Microsoft SharePoint Server 2013-Installation befindet.
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |Das Objektmodell zum Automatisieren InfoPath Forms Services Aufgaben wie das Hochladen, Aktivieren oder Deaktivieren browserfähiger Formularvorlagen.  <br/> |
   
Weitere Informationen zum InfoPath Forms Services-Objektmodell finden Sie im SharePoint Server 2013 Software Developers Kit (SDK), das auf MSDN verfügbar ist.
  
## <a name="infopath-development-environment"></a>InfoPath-Entwicklungsumgebung

Die Entwicklung von Geschäftslogik in InfoPath 2013-Formularvorlagen kann mithilfe von Visual Studio 2012 mit installierten [Microsoft Visual Studio-Tools für Anwendungen 2012-Add-Ons](https://www.microsoft.com/en-us/download/details.aspx?id=38807) ausgeführt werden. 
  
> [!NOTE]
> In InfoPath 2013 wird das Erstellen oder Bearbeiten von Formularvorlagen, die mit JScript oder VBScript geschriebene Geschäftslogik verwenden, nicht unterstützt, obwohl InfoPath Filler das Öffnen skriptbasierter Formularvorlagen unterstützt, die in früheren Versionen von InfoPath erstellt wurden. 
  
## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)
- [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

