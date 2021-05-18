---
title: Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, Objektmodelle,Objektmodelle [InfoPath 2007],InfoPath 2007, Entwicklungsumgebungen
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen für die Entwicklung von Geschäftslogik in Formularvorlagen und unterstützt die externe Automatisierung aus verwalteten Code.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303458"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath

Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen für die Entwicklung von Geschäftslogik in Formularvorlagen und unterstützt die externe Automatisierung aus verwalteten Code.
  
InfoPath Forms Services, das in SharePoint Server 2013 verfügbar ist, bietet eine Webbrowsererfahrung zum Ausfüllen von InfoPath-Formularen. Wenn sie auf einem Server bereitgestellt werden, der InfoPath Forms Services ausgeführt wird, können Formulare, die auf browserkompatiblen Formularvorlagen (XSN) basieren, in einem Webbrowser von Computern geöffnet werden, auf denen InfoPath nicht installiert ist, sie werden jedoch bei der Installation in InfoPath geöffnet. InfoPath Forms Services bietet auch ein Objektmodell zum Automatisieren von Serveraufgaben im Zusammenhang mit der Veröffentlichung und Verwaltung von InfoPath-Formularvorlagen.
  
InfoPath 2013 unterstützt die Visual Studio 2012-Programmierumgebung und die zugehörigen Programmiersprachen, die weiter unten in diesem Thema beschrieben werden.
  
## <a name="infopath-programming-models"></a>InfoPath-Programmiermodelle

InfoPath 2013 unterstützt zwei Objektmodelle zum Entwickeln von Geschäftslogik in Formularvorlagen:
  
- Das InfoPath-Objektmodell mit verwaltetem Code
    
- Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code
    
Darüber hinaus ermöglicht InfoPath 2013 das Schreiben von verwalteten Code, um InfoPath aus einer externen Anwendung zu automatisieren.
  
InfoPath Forms Services stellt ein Objektmodell für die Automatisierung von Serveraufgaben bereit, z. B. das Überprüfen und Hochladen von Formularvorlagen aus Code, der auf dem Server ausgeführt wird, was Serveradministratorzugriff und -berechtigungen erfordert.
  
> [!NOTE]
> InfoPath Filler 2013 kann InfoPath-Formularvorlagenlösungen öffnen und ausführen, die in früheren Versionen von InfoPath erstellt wurden und Geschäftslogik verwenden, die mit Skriptsprachen (JScript und VBScript) geschrieben wurde. Das Erstellen oder Ändern von Formularvorlagen, in denen mit Skripts geschriebene Geschäftslogik verwendet wird, wird von InfoPath Designer 2010 jedoch nicht unterstützt. 
  
### <a name="the-infopath-managed-code-object-model"></a>Das InfoPath-Objektmodell mit verwaltetem Code

Das Objektmodell für verwalteten Code in InfoPath 2013 wird in zwei Assemblys implementiert, die beide den Namen Microsoft.Office.Infopath.dll.
  
Eine Version der Assembly implementiert eine Teilmenge des InfoPath-Objektmodells, das nur die Typen und Member enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt werden, die auf SharePoint Server 2013 mit InfoPath Forms Services. Formularvorlagen mit Geschäftslogik, die für diese Assembly geschrieben wurden, werden im InfoPath Filler und in einem Webbrowser geöffnet und ausgeführt.
  
Die andere Version der Assembly implementiert zusätzliche Typen und Member mit Funktionalität, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird. Formularvorlagen mit Geschäftslogik, die für die zusätzlichen Klassen und Member in dieser Assembly geschrieben wurden, werden nur im InfoPath Filler-Editor geöffnet und ausgeführt.
  
> [!NOTE]
> Es ist möglich, bedingte Logik zu schreiben, die die Eigenschaften der [Environment-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) verwendet, um zu bestimmen, in welcher Umgebung (InfoPath Filler oder webbrowser) die Formularvorlage ausgeführt wird. Mithilfe dieser bedingten Logik kann Ihre Geschäftslogik zwischen Code verzweigen, der in einem Webbrowser funktioniert, und Code, der für Klassen und Member geschrieben wurde, die nur im InfoPath Filler-Editor funktionieren. Weitere Informationen finden Sie unter [Write Conditional Logic That Determines the Run-time Environment](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
Die Assembly, die InfoPath beim Hinzufügen und Kompilieren von Geschäftslogik für die Formularvorlage verwendet, hängt davon  ab, ob Sie die Formularvorlage Leeres Formular oder Leeres Formular **(InfoPath Filler)** auf der Registerkarte Neu der Microsoft Office Backstage auswählen, wenn Sie mit dem Entwerfen eines neuen Formulars im InfoPath Designer beginnen.  Formulare, die mit der Formularvorlage **Leeres Formular** erstellt wurden, verwenden die Assembly, die nur die Typen und Member enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt sind. Formulare, die mithilfe der **Formularvorlage Leere** Formulare erstellt werden, können sowohl im Webbrowser als auch im InfoPath Filler geöffnet werden. Formulare, die mithilfe der Formularvorlage Leeres **Formular (InfoPath Filler)** erstellt werden, verwenden die Assembly, die zusätzliche Typen und Member implementiert, die Funktionen bereitstellen, die in der Geschäftslogik browserfähiger Formularvorlagen nicht unterstützt werden und nur im InfoPath Filler geöffnet werden können. 
  
> [!TIP]
> Nachdem Sie mit dem Entwerfen einer Formularvorlage beginnen, können Sie ändern, welche Assembly verwendet wird, indem Sie die Einstellungen für die Formularkompatibilität ändern. Hierzu klicken Sie auf **Sprache** auf der Registerkarte **Entwickler** und dann auf **Kompatibilität** in der Liste **Kategorie**. Wählen Sie **in** der Liste Formulartyp die Option **Webbrowserformular** aus, um ein Formular zu erstellen, das als browserkompatibles Formular auf SharePoint Server 2013 bereitgestellt werden kann. Wählen **Sie InfoPath Filler Form aus,** um ein Formular zu erstellen, das nur im InfoPath Filler-Editor ausgeführt werden kann. Die anderen Auswahlen in der **Liste Formulartyp** bieten Unterstützung für die Kompatibilität mit InfoPath 2007 und InfoPath 2003. 
  
Die Klassen und Member beider Versionen dieses Objektmodells werden über [microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) In der folgenden Tabelle ist aufgeführt, wo sich die Assemblys in den Verzeichnissen einer InfoPath 2013-Installation befinden. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (befindet sich in C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |Die Teilmenge des Objektmodells, die nur Typen und Member enthält, die in der Geschäftslogik einer Formularvorlage ausgeführt werden, die auf einem Server bereitgestellt wird, auf dem InfoPath Forms Services.  <br/> |
|Microsoft.Office.InfoPath.dll (befindet sich in C:\Program Files\Microsoft Office\Office15\InfoPathOM)  <br/> |Das "vollständige" Objektmodell, einschließlich Typen und Member, die nicht in der Geschäftslogik einer Formularvorlage ausgeführt werden, die für die InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> Die weiter oben in diesem Abschnitt genannten Assemblys werden zur Entwurfszeit beim Schreiben und Kompilieren von Code verwendet. Zur Laufzeit befindet sich die Assembly, die beim Öffnen einer Formularvorlage in InfoPath verwendet wird, im globalen Assemblycache (Global Assembly Cache, GAC) des Computers, auf dem InfoPath installiert ist. Wenn eine Formularvorlage in einem Webbrowser von einem Server geöffnet wird, auf dem InfoPath Forms Services, befindet sich die verwendete Assembly auf dem Server. 
  
Das Bereitstellen von zwei Assemblys trägt dazu bei, dass Ihre Geschäftslogik nur Aufrufe an die entsprechenden Objektmodellmitglieder für die unterstützten Formulareditoren (Webbrowser oder InfoPath Filler) enthält. Wenn Sie ihren Code beispielsweise bearbeiten, werden IntelliSense Features wie anweisungsabschluss und in-line-Dokumentation nur angezeigt und für die entsprechenden Objektmodellmmitglieder für Ihre Zielformular-Editoren verwendet.
  
In beiden Versionen des verwalteten Codeobjektmodells, das von Microsoft verfügbar gemacht wird. Office. Die InfoPath-Assembly, das Navigieren und Aktualisieren von XML-Datenspeichern in der Geschäftslogik erfordert Aufrufe an die Mitglieder **derSystem.Xml. XPath.XPathNavigator-Klasse.** In InfoPath 2003 Das Navigieren und Aktualisieren von XML-Datenspeichern erfordert das Aufrufen von Membern von MSXML-Klassen (für Geschäftslogik, die mithilfe von JScript oder VBScript erstellt wurde) oder durch Aufrufen der Wrapper für MSXML-Klassen, die vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellt werden (für Geschäftslogik, die mithilfe von C# oder Visual Basic und dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET erstellt wird). 
  
Die Verwendung von Mitgliedern der **XPathNavigator-Klasse** ermöglicht demselben Geschäftslogikcode die Unterstützung der DOM-Manipulation für Formularvorlagen, die sowohl im InfoPath-Client als auch in webfähigen Formularen geöffnet werden, die von SharePoint Server 2013 mit InfoPath Forms Services in einem Webbrowser geöffnet werden. 
  
Informationen zum Arbeiten mit Mitgliedern der **XPathNavigator-Klasse** in der Geschäftslogik von Formularvorlagen mit verwalteten Code von InfoPath finden Sie unter Arbeiten mit den [Klassen XPathNavigator und XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code

Das InfoPath 2003-kompatible Objektmodell für verwalteten Code wurde in InfoPath 2003 Service Pack 1 zusammen mit dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET zum Schreiben von Geschäftslogik in Formularvorlagen mit verwalteten Code eingeführt. Dieses Objektmodell wird weiterhin von InfoPath 2013 unterstützt, um die Kompatibilität mit InfoPath 2003 zu gewährleisten.
  
Die Klassen und Member dieses Objektmodells werden über den [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) verfügbar gemacht. Dieses Objektmodell wird in der folgenden Assemblydatei implementiert, die sich im Ordner "C:\Program Files\Microsoft Office\Office14" befindet. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Stellt COM-Inop für das InfoPath COM-Objektmodell für die Geschäftslogik der Formularvorlage zur Verfügung, die mithilfe von C# oder Visual Basic.  <br/> |
   
> [!NOTE]
> Obwohl die Geschäftslogik mit dem com-Interop-Objektmodell mit verwalteten Code erstellt wird, das von Microsoft bereitgestellt wird. Office.Interop.InfoPath.SemiTrust-Assembly wird weiterhin von InfoPath 2013 unterstützt. Geschäftslogik, die mit diesem Objektmodell geschrieben wurde, wird nicht für browserfähige Formularvorlagen unterstützt, die auf SharePoint Server 2013 mit InfoPath Forms Services. Browserfähige Formularvorlagen müssen das Objektmodell für verwalteten Code von InfoPath für benutzerdefinierte Geschäftslogik verwenden. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatisieren von InfoPath aus verwaltetem Code

Zusätzlich zum Schreiben von Geschäftslogik mit verwalteten Code können Entwickler InfoPath mithilfe von verwalteten Code automatisieren, der in einer externen Anwendung ausgeführt wird. Diese Funktionalität und die Assemblys, die zum Schreiben von Code erforderlich sind, wurden in InfoPath 2003 Service Pack 1 eingeführt. Die Objekte und Member für die Automatisierung von InfoPath wurden aktualisiert, um zusätzliche Funktionen bereitzustellen, wenn Sie externen Automatisierungscode für InfoPath 2013 schreiben.
  
Die klassen und member, die für die externe Automatisierung verwendet werden, werden über die [Namespaces Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) [und](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)Microsoft.Office.Interop.InfoPath.Xmlverfügbar gemacht. Die Assemblydateien, die zum Schreiben von Automatisierungscode erforderlich sind, befinden sich im Ordner "C:\Programme\Microsoft Office\Office14". 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Stellt COM-Inop für das InfoPath COM-Objektmodell für externen Automatisierungscode zur Verfügung, der mithilfe von C# oder Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Stellt COM-Interop für MSXML für XML-DOM-Vorgänge in externem Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben ist.  <br/> |
   
Weitere Informationen zu den Objektmodellen, die von den **Namespaces Microsoft.Office.Interop.InfoPath** und **Microsoft.Office.Interop.InfoPath.Xml** bereitgestellt werden, die ausschließlich zum Automatisieren der InfoPath-Anwendung mithilfe von verwalteten Code aus externen Anwendungen verwendet werden, finden Sie im [InfoPath Developer Center](https://msdn.microsoft.com/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>Das InfoPath Forms Services-Objektmodell

Das Objektmodell für verwalteten Code für die Automatisierung InfoPath Forms Services Verwaltungsaufgaben wird in der Microsoft.Office.InfoPath.Server.dll implementiert, die sich auf dem Laufwerk \< \> :\Programme\Microsoft Office Server\15.0\Bin auf einer Microsoft SharePoint Server 2013-Installation befindet.
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |Das Objektmodell zum Automatisieren InfoPath Forms Services Aufgaben wie hochladen, Aktivieren oder Deaktivieren browserfähiger Formularvorlagen.  <br/> |
   
Weitere Informationen zum InfoPath Forms Services finden Sie im SharePoint Server 2013 Software Developers Kit (SDK), das auf MSDN verfügbar ist.
  
## <a name="infopath-development-environment"></a>InfoPath-Entwicklungsumgebung

Die Entwicklung von Geschäftslogik in InfoPath 2013-Formularvorlagen kann mithilfe von Visual Studio 2012 durchgeführt werden, wenn [das Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On](https://www.microsoft.com/en-us/download/details.aspx?id=38807) installiert ist. 
  
> [!NOTE]
> InfoPath 2013 unterstützt nicht das Erstellen oder Bearbeiten von Formularvorlagen, die Geschäftslogik verwenden, die mit JScript oder VBScript geschrieben wurde, obwohl der InfoPath Filler das Öffnen skriptbasierter Formularvorlagen unterstützt, die in früheren Versionen von InfoPath erstellt wurden. 
  
## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)
- [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

