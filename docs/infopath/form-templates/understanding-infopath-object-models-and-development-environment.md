---
title: Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, Objektmodelle, Objektmodelle [InfoPath 2007], InfoPath 2007, Entwicklungsumgebungen
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen zum Entwickeln von Geschäftslogik in Formularvorlagen und unterstützt die externe Automatisierung von verwaltetem Code.
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303458"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Grundlegendes zu Objektmodellen und zur Entwicklungsumgebung in InfoPath

Microsoft InfoPath 2013 unterstützt zwei Arten von Programmiermodellen zum Entwickeln von Geschäftslogik in Formularvorlagen und unterstützt die externe Automatisierung von verwaltetem Code.
  
InfoPath Forms Services, das in SharePoint Server 2013 verfügbar ist, bietet eine Webbrowser Umgebung zum Ausfüllen von InfoPath-Formularen. Bei der Bereitstellung auf einem Server, auf dem InfoPath Forms Services ausgeführt werden, können Formulare, die auf browserkompatiblen Formularvorlagen (XSN) basieren, in einem Webbrowser von Computern aus geöffnet werden, auf denen InfoPath nicht installiert ist, aber Sie werden in InfoPath geöffnet, wenn es installiert wird. InfoPath Forms Services stellt auch ein Objektmodell zum Automatisieren von Serveraufgaben im Zusammenhang mit der Veröffentlichung und Verwaltung von InfoPath-Formularvorlagen bereit.
  
InfoPath 2013 unterstützt die Programmierumgebung von Visual Studio 2012 und die dazugehörigen Programmiersprachen, die weiter unten in diesem Thema beschrieben werden.
  
## <a name="infopath-programming-models"></a>InfoPath-Programmiermodelle

InfoPath 2013 unterstützt zwei Objektmodelle für die Entwicklung von Geschäftslogik in Formularvorlagen:
  
- Das InfoPath-Objektmodell mit verwaltetem Code
    
- Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code
    
Darüber hinaus ermöglicht InfoPath 2013 das Schreiben von verwaltetem Code, um InfoPath aus einer externen Anwendung zu automatisieren.
  
InfoPath Forms Services stellt ein Objektmodell zum Automatisieren von Serveraufgaben bereit, beispielsweise zum Überprüfen und Hochladen von Formularvorlagen aus Code, der auf dem Server ausgeführt wird und für den Server Administratorzugriff und-Berechtigungen erforderlich ist.
  
> [!NOTE]
> Der InfoPath Filler 2013 kann in früheren Versionen von InfoPath erstellte InfoPath-Formularvorlagen Lösungen öffnen und ausführen, die mit Skriptsprachen geschriebene Geschäftslogik (JScript und VBScript) verwenden. Das Erstellen oder Ändern von Formularvorlagen, in denen mit Skripts geschriebene Geschäftslogik verwendet wird, wird von InfoPath Designer 2010 jedoch nicht unterstützt. 
  
### <a name="the-infopath-managed-code-object-model"></a>Das InfoPath-Objektmodell mit verwaltetem Code

Das InfoPath 2013-Objektmodell mit verwaltetem Code wird in zwei Assemblys mit dem Namen Microsoft. Office. InfoPath. dll implementiert.
  
Eine Version der Assembly implementiert eine Teilmenge des InfoPath-Objektmodells, die nur die Typen und Elemente enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt werden, die auf SharePoint Server 2013 mit InfoPath Forms Services. Formularvorlagen mit Geschäftslogik, die für diese Assembly geschrieben wurden, werden in InfoPath Filler und in einem Webbrowser ausgeführt.
  
Die andere Version der Assembly implementiert zusätzliche Typen und Member mit Funktionalität, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird. Formularvorlagen mit Geschäftslogik, die mit den zusätzlichen Klassen und Elementen in dieser Assembly geschrieben wurden, werden nur im InfoPath Filler-Editor geöffnet und ausgeführt.
  
> [!NOTE]
> Es ist möglich, bedingte Logik zu schreiben, die die Eigenschaften der [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse verwendet, um zu bestimmen, in welcher Umgebung (InfoPath Filler oder Webbrowser) die Formularvorlage läuft. Mithilfe dieser bedingten Logik kann sich Ihre Geschäftslogik zwischen Code verzweigen, der in einem Webbrowser funktioniert, und Code, der mit Klassen und Membern geschrieben wird, die nur im InfoPath Filler-Editor funktionieren. Weitere Informationen finden Sie unter [Schreiben von bedingter Logik zur Bestimmung der Laufzeitumgebung](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
Die Assembly, die InfoPath beim Hinzufügen und Kompilieren von Geschäftslogik für die Formularvorlage verwendet, hängt davon ab, ob Sie die Formularvorlage **leeres** Formular oder **leeres Formular (InfoPath Filler)** auf der **neuen** Registerkarte von Microsoft Office backstaging auswählen, wenn Sie beginnen mit dem Entwerfen eines neuen Formulars im InfoPath-Designer. Formulare, die mit der Formularvorlage **Leeres Formular** erstellt wurden, verwenden die Assembly, die nur die Typen und Member enthält, die in der Geschäftslogik von Formularvorlagen unterstützt werden, die als browserfähige Formularvorlagen bereitgestellt sind. Formulare, die mit der Formularvorlage **leeres Formular** erstellt wurden, können sowohl im Webbrowser als auch im InfoPath-Füller geöffnet werden. Formulare, die mit der Formularvorlage **leeres Formular (InfoPath Filler)** erstellt wurden, verwenden die Assembly, die zusätzliche Typen und Member implementiert, die Funktionalität bereitstellen, die in der Geschäftslogik von browserfähigen Formularvorlagen nicht unterstützt wird und nur im InfoPath-Füller geöffnet. 
  
> [!TIP]
> Nachdem Sie mit dem Entwerfen einer Formularvorlage begonnen haben, können Sie die verwendete Assembly ändern, indem Sie die Einstellungen für die Formular Kompatibilität ändern. Hierzu klicken Sie auf **Sprache** auf der Registerkarte **Entwickler** und dann auf **Kompatibilität** in der Liste **Kategorie**. Wählen Sie **** in der Liste Formulartyp die Option **Webbrowserformular** aus, um ein Formular zu erstellen, das als Browser kompatibles Formular auf SharePoint Server 2013 bereitgestellt werden kann. Wählen Sie **InfoPath Filler-Formular** aus, um ein Formular zu erstellen, das nur im InfoPath Filler-Editor ausgeführt werden kann. Die anderen Optionen in der **** Liste Formulartyp bieten Unterstützung für die Kompatibilität mit InfoPath 2007 und InfoPath 2003. 
  
Die Klassen und Elemente beider Versionen dieses Objektmodells werden über den [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace verfügbar gemacht. In der folgenden Tabelle ist aufgeführt, wo sich die Assemblys in den Verzeichnissen einer InfoPath 2013-Installation befinden. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft. Office. InfoPath. dll (befindet sich in C:\Programme\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |Die Teilmenge des Objektmodells, die nur Typen und Elemente enthält, die in der Geschäftslogik einer Formularvorlage ausgeführt werden, die auf einem Server bereitgestellt wird, auf dem InfoPath Forms Services ausgeführt wird.  <br/> |
|Microsoft. Office. InfoPath. dll (befindet sich in C:\Programme\Microsoft Office\Office15\InfoPathOM)  <br/> |Das vollständige Objektmodell einschließlich der Typen und Elemente, die nicht in der Geschäftslogik einer Formularvorlage ausgeführt werden, die für InfoPath Forms Services bereitgestellt wird.  <br/> |
   
> [!NOTE]
> Die weiter oben in diesem Abschnitt genannten Assemblys werden zur Entwurfszeit beim Schreiben und Kompilieren von Code verwendet. Zur Laufzeit befindet sich die beim Öffnen einer Formularvorlage in InfoPath verwendete Assembly im globalen Assemblycache (GAC) des Computers, auf dem InfoPath installiert ist. Wenn eine Formularvorlage auf einem Server mit InfoPath Forms Services in einem Webbrowser geöffnet wird, befindet sich die verwendete Assembly auf dem Server. 
  
Wenn zwei Assemblys bereitgestellt werden, können Sie sicherstellen, dass Ihre Geschäftslogik nur Aufrufe der entsprechenden Objektmodellelemente für die unterstützten Formular-Editoren (Webbrowser oder InfoPath Filler) enthält. Wenn Sie beispielsweise Ihren Code bearbeiten, werden IntelliSense-Features wie die Anweisungsvervollständigung und die Inline Dokumentation nur für die entsprechenden Objektmodellelemente für die Zielformular-Editoren angezeigt und funktionieren.
  
In beiden Versionen des verwalteten Codeobjekt Modells, das von der Microsoft. Office. InfoPath-Assembly verfügbar gemacht wird, erfordert das Navigieren und Aktualisieren von XML-Daten speichern in der Geschäftslogik Aufrufe der Member der **System. Xml. XPath. XPathNavigator** -Klasse. In InfoPath 2003 erfordert das Navigieren und Aktualisieren von XML-Daten speichern das Aufrufen von Membern von MSXML-Klassen (für Geschäftslogik, die mithilfe von JScript oder VBScript erstellt wurde) oder durch Aufrufen der Wrapper für MSXML-Klassen, die vom ** Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace (für die Geschäftslogik, die mit C# oder Visual Basic erstellt wurde, und dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .net). 
  
Durch die Verwendung von Membern der **XPathNavigator** -Klasse kann derselbe Geschäftslogikcode die DOM-Manipulation für Formularvorlagen unterstützen, die sowohl im InfoPath-Client als auch in webfähigen Formularen geöffnet werden, die von SharePoint Server 2013 mit InfoPath-Formularen geöffnet werden. Dienste in einem Webbrowser. 
  
Weitere Informationen zum Arbeiten mit Membern der **XPathNavigator** -Klasse in der Geschäftslogik von InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)".
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code

Das InfoPath 2003-kompatible Objektmodell mit verwaltetem Code wurde in InfoPath 2003 Service Pack 1 zusammen mit dem Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET zum Schreiben von Geschäftslogik in Formularvorlagen mit verwaltetem Code eingeführt. Dieses Objektmodell wird von InfoPath 2013 weiterhin unterstützt, um Kompatibilität mit InfoPath 2003 bereitzustellen.
  
Die Klassen und Member dieses Objektmodells werden über den [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace verfügbar gemacht. Dieses Objektmodell wird in der folgenden Assemblydatei implementiert, die sich im Ordner C:\Programme\Microsoft Office\Office14 befindet. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft. Office. Interop. InfoPath. SemiTrust. dll  <br/> |Stellt COM-Interop für das InfoPath-COM-Objektmodell für die Formularvorlagen-Geschäftslogik bereit, die mit C# oder Visual Basic geschrieben wurde.  <br/> |
   
> [!NOTE]
> Das Erstellen von Geschäftslogik mit dem von der Microsoft. Office. Interop. InfoPath. SemiTrust-Assembly bereitgestellten COM-Interop-Objektmodell mit verwaltetem Code wird von InfoPath 2013 weiterhin unterstützt, Geschäftslogik, die mit diesem Objektmodell geschrieben wurde, wird nicht unterstützt browserfähige Formularvorlagen, die in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden. Browser fähige Formularvorlagen müssen das InfoPath-Objektmodell mit verwaltetem Code für benutzerdefinierte Geschäftslogik verwenden. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatisieren von InfoPath aus verwaltetem Code

Zusätzlich zum Schreiben von Geschäftslogik mit verwaltetem Code können Entwickler InfoPath automatisieren, indem Sie verwalteten Code verwenden, der in einer externen Anwendung läuft. Diese Funktionalität und die zum Schreiben von Code erforderlichen Assemblys wurden in InfoPath 2003 Service Pack 1 eingeführt. Die Objekte und Member für die Automatisierung von InfoPath wurden aktualisiert und bieten zusätzliche Funktionalität, wenn Sie externen Automatisierungscode für InfoPath 2013 schreiben.
  
Die Klassen und Elemente, die für die externe Automatisierung verwendet werden, werden über die Namespaces [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) und [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) verfügbar gemacht. Die für das Schreiben von Automatisierungscode erforderlichen Assemblydateien befinden sich im Ordner C:\Programme\Microsoft Office\Office14. 
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft. Office. Interop. InfoPath. dll  <br/> |Stellt COM-Interop für das InfoPath-COM-Objektmodell für externen Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben wurde.  <br/> |
|Microsoft. Office. Interop. InfoPath. Xml. dll  <br/> |Stellt COM-Interop für MSXML für XML-DOM-Vorgänge in externem Automatisierungscode bereit, der mit C# oder Visual Basic geschrieben ist.  <br/> |
   
Weitere Informationen zu den Objektmodellen, die von den Namespaces **Microsoft. Office. Interop. InfoPath** und **Microsoft. Office. Interop. InfoPath. XML** bereitgestellt werden, sind ausschließlich zum Automatisieren der InfoPath-Anwendung mithilfe von verwalteter Code aus externen Anwendungen finden Sie im [InfoPath Developer Center](https://msdn.microsoft.com/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>Das InfoPath Forms Services-Objektmodell

Das Objektmodell für verwalteten Code zum Automatisieren von InfoPath Forms Services-Verwaltungsaufgaben wird in der Microsoft. Office. InfoPath. Server. dll implementiert, die \<sich\>unter Laufwerk: \Programme\Microsoft Office Server\15.0\Bin auf einer Microsoft SharePoint Server 2013-Installation.
  
|**Assembly**|**Beschreibung**|
|:-----|:-----|
|Microsoft. Office. InfoPath. Server. dll  <br/> |Das Objektmodell zum Automatisieren von InfoPath Forms Services-Aufgaben wie hochladen, aktivieren oder Deaktivieren von browserfähigen Formularvorlagen.  <br/> |
   
Weitere Informationen zum InfoPath Forms Services-Objektmodell finden Sie im SharePoint Server 2013 Software Developers Kit (SDK), das auf MSDN verfügbar ist.
  
## <a name="infopath-development-environment"></a>InfoPath-Entwicklungsumgebung

Die Entwicklung der Geschäftslogik in InfoPath 2013-Formularvorlagen kann mithilfe von Visual Studio 2012 mit [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) Add-on installiert werden. 
  
> [!NOTE]
> InfoPath 2013 unterstützt nicht das Erstellen oder Bearbeiten von Formularvorlagen, die mit JScript oder VBScript geschriebene Geschäftslogik verwenden, obwohl InfoPath Filler das Öffnen skriptbasierter Formularvorlagen unterstützt, die in früheren Versionen von InfoPath erstellt wurden. 
  
## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)
- [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

