---
title: Problembehandlung bei Office-Dateien und benutzerdefinierte Lösungen mit dem Telemetrieprotokoll
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ef88e30e-7537-488e-bc72-8da29810f7aa
description: Verwenden Sie das Telemetrieprotokoll für Office 2013, um Kompatibilitätsprobleme zwischen Office 2013 und Lösungen zu ermitteln, die für vorherige Versionen von Office entwickelt wurden.
localization_priority: Priority
ms.openlocfilehash: 3954662a9476dca0cbb9bf4b8197979783b7e11e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715165"
---
# <a name="troubleshooting-office-files-and-custom-solutions-with-the-telemetry-log"></a>Problembehandlung bei Office-Dateien und benutzerdefinierte Lösungen mit dem Telemetrieprotokoll

Verwenden Sie das Telemetrieprotokoll für Office 2013, um Kompatibilitätsprobleme zwischen Office 2013 und Lösungen zu ermitteln, die für vorherige Versionen von Office entwickelt wurden.
  
Der folgende Artikel beschreibt das Telemetrieprotokoll und dessen Verwendung. Weitere Informationen über spezifische Ergebnisse, die im Telemetrieprotokoll angezeigt werden, finden Sie unter [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md).

Microsoft hat im Laufe der Zeit viele Versionen von Tools und Frameworks für die Anpassung, Automatisierung und Erweiterung von Office bereitgestellt. Dadurch haben Unternehmen und Benutzer die Möglichkeit, Lösungen oder Add-Ins für Office-Anwendungen zu erstellen, um deren Produktivität und Effizienz zu steigern. Die Komplexität dieser Lösungen ist ganz unterschiedlich und reicht von einfachen VBA-Makros (Visual Basic for Applications) bis hin zu robusten .NET Framework-Anpassungen. Viele Benutzer, die diese Lösungen besitzen, setzen sie bei der Ausführung geschäftskritischer Aufgaben ein und wissen möglicherweise gar nicht, dass sie eine Anpassung ihrer Office-Anwendungen verwenden.
  
Bei einer solchen Vielfalt an Office-Lösungen können Upgrades von Office-Versionen sehr komplex werden. Unternehmen und Benutzer wissen nicht, ob ihre wichtigen und wertvollen Lösungen mit der neuen Version vollständig kompatibel sind. Ihre Lösungen verwenden möglicherweise inzwischen veraltete Features und Computercode aus vorherigen Versionen von Office. Wenn eine Lösung, die ein veraltetes Feature verwendet, in die "Hostanwendung" geladen wird, verhält sich die Lösung möglicherweise anders als erwartet, verursacht einen Fehler, lädt nicht oder führt dazu, dass die Hostanwendung nicht richtig ausgeführt wird.
  
Telemetrieprotokoll für Office 2013 ist ein auf Excel 2013 basierendes Tool und hilft Entwicklern und erfahrenen Benutzern bei der Diagnose von Kompatibilitätsproblemen durch die Anzeige von Ereignissen, die innerhalb ausgewählter Office 2013-Anwendungen auftreten. Anhand dieses Tools können Benutzer potenzielle Probleme mit Add-Ins ermitteln, die sie in ihrer Arbeitsumgebung verwenden. Die Entscheidungsträger im Unternehmen erhalten so die Informationen, die sie benötigen, um für oder gegen ein Upgrade auf Office 2013 zu entscheiden. Telemetrieprotokoll liefert zudem detailliertes Feedback zu bestimmten Änderungen oder veralteten Features in den Objektmodellen für die Office 2013-Anwendungen, damit Entwickler problematischen Code oder problematische Steuerelemente schneller identifizieren und umgestalten können. IT-Experten können mit Telemetriedashboard für Office 2013, einem ergänzenden Tool zu Telemetrieprotokoll, Trends in der Funktionsweise der Lösung über mehrere Clients anzeigen.
  
Weitere Informationen finden Sie im Artikel [Bereitstellen des Office-Telemetriedashboards](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717).
  
## <a name="how-the-telemetry-log-works"></a>So funktioniert Telemetrieprotokoll
<a name="OEV_Types"> </a>

Wenn eine Office-Datei oder -Lösung geladen, verwendet oder geschlossen wird oder einen Fehler in einer der ausgewählten Office 2013-Anwendungen auslöst, fügt die Anwendung einen Datensatz in einem lokalen Datenspeicher (einer Datenbank auf demselben Computer) hinzu, der Informationen über das Ereignis enthält. Der Datensatz umfasst einen Titel für das Ereignis, den Namen der Anwendung, die das Ereignis protokolliert hat, die Uhrzeit, den Namen der Datei oder Lösung, den Schweregrad und eine kurze Beschreibung eventueller Fehler, die aufgetreten sind. Nach einer Aktualisierung zeigt die Telemetrieprotokoll-Arbeitsmappe eine Liste der im lokalen Datenspeicher enthaltenen Datensätze an.
  
> [!NOTE]
> Der Standardspeicherort für den lokalen Datenspeicher ist %Users%\[Current user]\AppData\Local\Microsoft\Office\15.0\Telemetry. Die standardmäßige Maximalgröße für den Datenspeicher beträgt 5 MB (5.120 KB). 
  
Ausgewählte Office 2013-Anwendungen verfügen über eine Laufzeitprotokollierungs-API, die einen Datensatz im lokalen Datenspeicher erstellt, wann immer eine Datei oder eine Lösung eines der folgenden Ereignisse auslöst:
  
- **OnLoad**: Ein Datensatz wird im lokalen Datenspeicher protokolliert, wenn eine Datei oder eine Lösung in bestimmte Office 2013-Anwendungen geladen wird. Die Laufzeitfehlerprotokollierung erfasst den Dateinamen, den Speicherort sowie andere Informationen im lokalen Arbeitsspeicher, wenn ein **OnLoad**-Ereignis ausgelöst wird. 
    
- **OnClose**: Ein Datensatz wird protokolliert, wenn eine Datei oder eine Lösung innerhalb der Anwendung geschlossen wird. Der Datensatz umfasst den Namen der Lösung bzw. Datei, ihren Speicherort und den Namen der Anwendung, die das Ereignis protokolliert hat.
    
- **OnError**: Ein Datensatz wird protokolliert, wenn in einer Lösung für bestimmte Office 2013-Anwendungen ein Fehler gefunden wird. Der Datensatz umfasst den Namen der Lösung oder Datei und den Laufzeitfehler oder das Kompatibilitätsproblem, der/das aufgetreten ist. Soweit möglich werden Fehler bekannten Kompatibilitätsproblemen zugeordnet und als solche in Telemetrieprotokoll angezeigt.
    
Telemetrieprotokoll zeigt Informationen über eine Vielzahl von Dateien und Lösungstypen für eine Auswahl von Office 2013-Anwendungen an. Die Art der Dateien und Lösungen, die durch Laufzeitprotokollierungs-APIs überwacht werden, ist je nach Anwendung unterschiedlich. Tabelle 1 liefert Informationen darüber, welche Arten von Lösungen überwacht werden.
  
### <a name="table-1-types-of-office-files-and-solutions-tracked-in-telemetry-log"></a>Tabelle 1: Typen von Office-Dateien und -Lösungen, die in Telemetrieprotokoll protokolliert werden
<a name="OEV_Table1"> </a>

|**Lösungstyp**|**Anwendungen**|**Beschreibung**|
|:-----|:-----|:-----|
|Aufgabenbereich-Apps  <br/> |Excel 2013, Word 2013, Project 2013  <br/> |Dies sind Office-Add-Ins, die in einem Aufgabenbereich innerhalb der Clientanwendung gehostet werden.  <br/> |
|Inhalts-Apps  <br/> |Excel 2013  <br/> |Dies sind Office-Add-Ins, die in den Inhalt der Office-Datei integriert sind.  <br/> |
|Mail-Apps  <br/> |Outlook 2013  <br/> |Dies sind Apps, die in Outlook 2013 angezeigt werden, wenn bestimmte Bedingungen erfüllt sind (der Nachrichtentext oder der Betreff enthält bestimmte Wörter oder Phrasen).  <br/> |
|Aktive Dokumente  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> | Aktive Dokumente sind alle Office-Dokumentdateien, mit Ausnahme der sonstigen Lösungstypen, die in dieser Tabelle aufgeführt sind. Dazu gehören:  <br/>  Office-Dateien im Binärformat (DOC, PPT, PPS, XLS)  <br/>  Office-Dateien im OpenXML-Format (DOCX, PPTX, PPSX, XLSX)  <br/>  Makroaktivierte Dateien mit VBA-Code (DOCM, DOTM, PPTM, POTM, XLSM, XLTM)  <br/>  Dateien mit ActiveX-Steuerelementen  <br/>  Dateien mit externen Datenverbindungen  <br/> |
|COM-Add-Ins  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> Outlook 2013  <br/> |COM-Add-Ins umfassen Office-Entwicklungstools in Visual Studio 2010-Add-Ins auf Anwendungsebene.  <br/> |
|Excel-Automatisierungs-Add-Ins  <br/> |Excel 2013  <br/> |Dieser Lösungstyp beinhaltet vorherige Versionen von Excel-unterstützten Automatisierungs-Add-Ins, die auf COM-Add-Ins gründen. Funktionen in Automatisierungs-Add-Ins können von Formeln in Excel-Arbeitsblättern aufgerufen werden.  <br/> |
|Excel XLL-Add-Ins  <br/> |Excel 2013  <br/> |XLL-Add-Ins (XLL) sind für Excel spezifisch und werden mit Compilern erstellt, die die Erstellung von DLLs (Dynamic Link Library) unterstützen. Sie müssen weder installiert noch registriert werden. XLL-Add-Ins enthalten auch DLLs, die benutzerdefinierte Befehle und Funktionen umfassen.  <br/> |
|Excel-XLS-RTD-Add-Ins  <br/> |Excel 2013  <br/> |XLS RTD-Add-Ins (Real-Time Data) sind Excel-Arbeitsblätter, die die **RealTimeData**-Arbeitsblattfunktion zum Aufrufen eines Automatisierungsservers verwenden, um Daten in Echtzeit abzurufen.  <br/> |
|Word WLL-Add-Ins  <br/> |Word 2013  <br/> |WLL-Add-Ins (WLL) betreffen nur Word und werden mit einem beliebigen Compiler erstellt, der das Erstellen von DLLs unterstützt.  <br/> |
|Anwendungs-Add-Ins  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Bei Anwendungs-Add-Ins handelt es sich um anwendungsspezifische Dateien, die VBA-Code enthalten. Hierzu zählen Word-Vorlagen mit Makros (DOTM), Excel-Add-Ins (XLA, XLAM) und PowerPoint-Add-Ins (PPA, PPAM).  <br/> |
|Vorlagen  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Vorlagen enthalten Dokument- (DOT, DOTX), Arbeitsblatt- (XLT, XLTX) oder Präsentationsvorlagen (POT, POTX), die an eine Office-Datei angehängt sind.  <br/> |
   
## <a name="using-the-office-telemetry-log"></a>Verwenden von Office Telemetry Log
<a name="OEV_Using"> </a>

Wenn Sie Office 2013 installieren, wird Telemetrieprotokoll installiert, der lokale Datenspeicher auf demselben Computer erstellt, und die Laufzeitprotokollierungs-APIs werden in den zuvor aufgeführten Office 2013-Anwendungen aktiviert. Allerdings muss eine Lösung bzw. eine Datei in der Anwendung geladen oder geöffnet werden, bevor Telemetrieprotokoll mit der Überwachung beginnen kann.
  
Gehen Sie folgendermaßen vor, um die erfassten Office-Probleme in Telemetrieprotokoll anzuzeigen. 
  
### <a name="to-use-the-telemetry-log"></a>So verwenden Sie Telemetrieprotokoll

1. Gehen Sie folgendermaßen vor, um Telemetrieprotokoll zu öffnen:
    
   - **Für Windows 7:** Wählen Sie im **Startmenü** **Alle Programme**. Erweitern Sie dann in der Liste der Programme **Microsoft Office 2013** und **Office 2013 Tools**, und klicken Sie dann auf **Office 2013 Telemetry Log**.
    
     In Excel 2013 wird eine neue Arbeitsmappe geöffnet. Die neue Arbeitsmappe enthält drei Arbeitsblätter: **Ereignisse**, **Systeminfo** und **Anleitung**.
    
   - **Für Windows 8:** Machen Sie eine Streifbewegung, um die App-Leiste anzuzeigen, wählen Sie **Alle Apps**, und wählen Sie dann **Office 2013 Telemetry Log**.
    
     In Excel 2013 wird eine neue Arbeitsmappe geöffnet. Die neue Arbeitsmappe enthält drei Arbeitsblätter: **Ereignisse**, **Systeminfo** und **Anleitung**.
    
2. Um eine aktuelle Ereignisliste anzuzeigen, klicken Sie oben auf dem Arbeitsblatt **Ereignisse** auf **Aktualisieren**.
    
3. Um die Ereignisdaten einzusehen, die von Office 2013-Anwendungen gesammelt werden, prüfen Sie die Tabelle auf dem Arbeitsblatt **Ereignisse**. 
    
4. Um Informationen über den Computer zu erhalten, auf dem Office 2013 und Telemetrieprotokoll installiert sind, prüfen Sie die Informationen auf dem Arbeitsblatt **Systeminfo**. 
    
> [!NOTE]
> Es ist nicht erforderlich, das Telemetrieprotokoll-Arbeitsblatt in Excel 2013 zu speichern, um die Ergebnisse als Datensatz abzulegen, da die Informationen im lokalen Datenspeicher (der unabhängig von Telemetrieprotokoll ist) gespeichert werden. Durch Speichern des Arbeitsblatts wird Telemetrieprotokoll aber auch nicht beschädigt. 
  
Telemetrieprotokoll zeigt einige einfache Informationen über die erfassten Ereignisse an. Jeder in Telemetrieprotokoll angezeigte Datensatz enthält einen Titel und gibt den Schweregrad des angezeigten Ereignisses an. Bei Fehlern liefern die Datensätze zudem eine Beschreibung des Fehlers sowie eine Anleitung zur Abhilfe. Denken Sie daran, dass nicht alle der angezeigten Datensätze Fehler angeben, die von Office-Lösungen verursacht wurden. Telemetrieprotokoll zeigt auch an, wenn Lösungen und Dateien erfolgreich geladen oder geschlossen werden. 
  
Beispielsweise wird das Problem mit dem Titel "OM ausgeblendet: Comment.Initial-Eigenschaft" angezeigt, wenn eine Lösung oder eine in Word 2013 geöffnete makroaktivierte Datei versucht, die Initialen eines Kommentierenden abzurufen, der einem Kommentar zugeordnet ist. Word 2013 bietet eine verbesserte Kommentarfunktion, die die Initialen des Kommentierenden nicht standardmäßig anzeigt. Die mit dem älteren Kommentarmodell verknüpften APIs sind im Word 2013-Objektmodell ausgeblendet worden, bleiben jedoch für die Rückwärtskompatibilität erhalten. Das Problem "OM ausgeblendet: Comment.Initial" in gibt die Datei, die versucht hat, die API zu verwenden, die Anwendung, die das Ereignis ausgelöst hat (Word 2013), das Datum und die Uhrzeit des Ereignisses und die Kurzbeschreibung des Fehlers sowie die Abhilfemaßnahme an.
  
**Abbildung 1. Office-Telemetrieprotokoll**
  
![Die Office-Ereignisanzeige zeigt Datensätze an.](media/off15_OfficeEventViewer_SD.png "Die Office-Ereignisanzeige zeigt Datensätze an")
  
> [!NOTE]
>  Das Arbeitsblatt **Systeminfo** im Telemetrieprotokoll enthält Informationen über den Computer, auf dem Office 2013 installiert ist. Dieses Arbeitsblatt enthält die folgenden Informationen: 
> - Name des Benutzers
> - Den vollständigen Namen des Computers
> - Die Architektur des Betriebssystems (x64/64 Bit oder x86/32 Bit)
> - Die auf dem Computer installierte Version von Windows
> - Zeitzone für die Systemuhr des Computers
> - Version des Telemetrieprotokolls
> - Office-Version, die auf dem Computer installiert ist
> 
> Diese Informationen können nützlich sein, wenn Sie die im Arbeitsblatt **Ereignisse** aufgelisteten Probleme und Ereignisse interpretieren. 
  
In Telemetrieprotokoll wird zusammen mit den bekannten Problemen der Schweregrad angegeben. Wie im vorherigen Beispiel hat ein Problem, bei dem ein Teil des Objektmodells ausgeblendet wurde, meist den Schweregrad "Informationell". Andere bekannte Probleme können aber schwerwiegender sein und ein sofortiges Eingreifen erfordern. In Telemetrieprotokoll werden die folgenden Abstufungen nach Schweregrad vorgenommen:
  
- **Informative** Das Problem hat möglicherweise keine sofortigen Auswirkungen auf die Anwendungskompatibilität, aber der Benutzer muss möglicherweise zu einem späteren Zeitpunkt Maßnahmen ergreifen. Viele Probleme des Typs "OM hidden" haben diesen Schweregrad. 
    
- **Warning** Das Problem könnte zu Datenverlust oder verminderter Darstellungstreue führen. 
    
- **Critical** Das Problem könnte einen signifikanten Verlust an Funktionalität verursachen oder zum Absturz der Anwendung führen. 
    
### <a name="table-2-types-of-events-displayed-in-the-telemetry-log"></a>Tabelle 2: In Telemetrieprotokoll angezeigte Ereignistypen
<a name="OEV_Table2"> </a>

Interpretieren Sie die in Telemetrieprotokoll angezeigten Datensätze anhand der folgenden Tabelle (Tabelle 2).
  
|**Ereignis-ID**|**Titel**|**Schweregrad**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|1  <br/> |Das Dokument wurde erfolgreich geladen  <br/> ||Die in der Spalte **File** angegebene Datei wurde in der Office-Anwendung ohne Probleme geöffnet.  <br/> |
|2  <br/> |Das Dokument konnte nicht geladen werden.  <br/> |Warnung  <br/> | Die Anwendung konnte die Datei nicht laden. Möglicherweise ist ein zugrunde liegendes Kompatibilitätsproblem die Ursache.  <br/><br/>Weitere Informationen dazu, wie Sie eine beschädigte Arbeitsmappe in Excel 2013 reparieren, finden Sie unter [Reparieren einer beschädigten Arbeitsmappe](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Weitere Informationen zur Reparatur eines beschädigten Dokuments in Word 2013 finden Sie unter [Speichern und Wiederherstellen einer Sicherungskopie eines Dokuments](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|3  <br/> |Die Vorlage wurde erfolgreich geladen.  <br/> ||Die in der Spalte **File** angegebene Vorlagendatei wurde in der Office-Anwendung ohne Probleme geöffnet.  <br/> |
|4  <br/> |Die Vorlage konnte nicht geladen werden.  <br/> |Warnung  <br/> | Die Anwendung konnte die Vorlagendatei nicht laden. Möglicherweise ist ein zugrunde liegendes Kompatibilitätsproblem die Ursache, oder die Vorlagenverfügbarkeit hat sich geändert.  <br/><br/>Weitere Informationen dazu, wie Sie eine beschädigte Arbeitsmappe in Excel 2013 reparieren, finden Sie unter [Reparieren einer beschädigten Arbeitsmappe](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Weitere Informationen zur Reparatur eines beschädigten Dokuments in Word 2013 finden Sie unter [Speichern und Wiederherstellen einer Sicherungskopie eines Dokuments](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|5  <br/> |Das Add-In wurde erfolgreich geladen.  <br/> ||Das in der Spalte **File** angegebene Add-In wurde erfolgreich in die Office-Anwendung geladen. Es wurden keine Kompatibilitätsprobleme ermittelt.  <br/> |
|6  <br/> |Fehler beim Laden von Add-In  <br/> |Kritisch  <br/> | Die Anwendung konnte das in der Spalte **File** angegebene Add-In nicht laden.  <br/><br/>Weitere Informationen dazu, wie Sie eine beschädigte Arbeitsmappe in Excel 2013 reparieren, finden Sie unter [Reparieren einer beschädigten Arbeitsmappe](https://office.microsoft.com/en-us/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx). <br/><br/>  Weitere Informationen zur Reparatur eines beschädigten Dokuments in Word 2013 finden Sie unter [Speichern und Wiederherstellen einer Sicherungskopie eines Dokuments](https://office.microsoft.com/en-us/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|7  <br/> |Das Add-In-Manifest wurde erfolgreich heruntergeladen.  <br/> ||Die Host-Anwendung hat das Manifest für die Office-Add-In erfolgreich heruntergeladen.  <br/> |
|8  <br/> |Das Add-In-Manifest konnte nicht heruntergeladen werden.  <br/> |Kritisch  <br/> |Die Hostanwendung konnte die Manifestdatei für die Office-Add-In nicht aus dem SharePoint-Katalog, dem Unternehmenskatalog oder aus dem Office Store laden.  <br/> |
|9  <br/> |Das Add-In-Manifest konnte nicht analysiert werden.  <br/> |Kritisch  <br/> |Die Hostanwendung hat das Office-Add-In-Manifest für das Add-In geladen, konnte jedoch das XML-Markup nicht lesen.  <br/> |
|10  <br/> |Die CPU-Nutzung des Add-Ins ist zu hoch.  <br/> |Kritisch  <br/> |Die Office-Add-In hat über eine begrenzte Zeitspanne mehr als 90 % der CPU-Ressourcen beansprucht.  <br/> |
|11  <br/> |Anwendung beim Laden abgestürzt  <br/> |Kritisch  <br/> |Die Office-Anwendung hat beim Start versucht, ein Dokument oder eine Lösung zu laden. Probleme mit dem Dokument bzw. der Lösung haben den Start der Anwendung verhindert.  <br/> |
|12  <br/> |Die Anwendung wurde aufgrund eines Problems geschlossen.  <br/> |Kritisch  <br/> |In der Anwendung ist ein kritischer Fehler aufgetreten. Sie musste geschlossen werden.  <br/> |
|13  <br/> |Das Dokument wurde erfolgreich geschlossen  <br/> ||Die in der Spalte **File** aufgeführte Datei ist erfolgreich geschlossen worden.  <br/> |
|14  <br/> |Die Anwendungssitzung wurde verlängert.  <br/> ||Anwendungssitzungen, bei denen ein bestimmtes Dokument oder eine bestimmte Lösung geöffnet ist, sollten nicht länger als 24 Stunden dauern. Wenn eine Sitzung länger als 24 Stunden dauert, erstellt die Hostanwendung eine neue Sitzung.  <br/> |
|15  <br/> |Das Add-In wurde aufgrund eines Timeouts bei der Zeichenfolgensuche deaktiviert.  <br/> ||Mail-Add-Ins durchsuchen die Betreffzeile und die Nachricht einer E-Mail, um zu ermitteln, ob sie mithilfe eines regulären Ausdrucks angezeigt werden sollte. Das Mail-Add-In, das in der Spalte **File** angegeben ist, wurde von Outlook 2013 deaktiviert, weil es bei dem Versuch, einen regulären Ausdruck zuzuordnen, mehrfach zu einer Zeitüberschreitung gekommen ist.  <br/> |
|16  <br/> |Dokument geöffnet beim Absturz der Anwendung  <br/> |Kritisch  <br/> |Die in der Spalte **File** angegebene Datei war geöffnet, als die Anwendung (in der Spalte **Application** angegeben) abgestürzt ist. Möglicherweise ist die Datei für den Absturz der Anwendung verantwortlich.  <br/> |
|17  <br/> |Das Add-In wurde erfolgreich geschlossen.  <br/> |Informativ  <br/> |Die Anwendung konnte das Add-In erfolgreich herunterfahren. successfully.  <br/> |
|18  <br/> |Die App wurde erfolgreich geschlossen.  <br/> ||Die Hostanwendung konnte die Office-Add-In erfolgreich schließen.  <br/> |
|19  <br/> |Für das Add-In ist ein Laufzeitfehler aufgetreten, der lokal protokolliert wurde.  <br/> |Kritisch  <br/> |Bei der Office-Add-In ist ein Problem aufgetreten, das zu einem Fehler geführt hat. Weitere Einzelheiten können Sie dem Protokoll der Microsoft Office-Benachrichtigungen entnehmen. Zeigen Sie das Protokoll mit der Windows-Ereignisanzeige auf dem Computer an, auf dem der Fehler aufgetreten ist.  <br/> |
|20  <br/> |Das Add-In konnte die Lizenzierung nicht überprüfen.  <br/> |Kritisch  <br/> |Die Lizenzinformationen für die Office-Add-In konnten nicht überprüft werden. Möglicherweise ist die Lizenz abgelaufen. Weitere Einzelheiten können Sie dem Protokoll der Microsoft Office-Benachrichtigungen entnehmen. Zeigen Sie das Protokoll mit der Windows-Ereignisanzeige auf dem Computer an, auf dem der Fehler aufgetreten ist.  <br/> |
|Verschiedene  <br/> |"OM Behavior Change: ..."  <br/> |Informativ  <br/> |Der von einem Add-In oder Makro aktivierte Dokumentcode verwendet ein Objekt, ein Element, eine Auflistung, eine Aufzählung oder eine Konstante, das bzw. die sich anders verhält als in früheren Versionen von Office.<br/><br/> Weitere Informationen hierzu finden Sie unter [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md).  <br/> |
|Verschiedene  <br/> |"OM Removed: …"  <br/> |Kritisch  <br/> |Der von einem Add-In oder Makro aktivierte Dokumentcode verwendet ein Objekt, ein Element, eine Auflistung, eine Aufzählung oder eine Konstante, das bzw. die aus dem Objektmodell entfernt wurde.<br/><br/>Weitere Informationen hierzu finden Sie unter [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md).  <br/> |
|Verschiedene  <br/> |"OM Hidden: …"  <br/> |Informativ  <br/> |Der von einem Add-In oder Makro aktivierte Dokumentcode verwendet ein Objekt, ein Element, eine Auflistung, eine Aufzählung oder eine Konstante, das bzw. die aus dem Objektmodell ausgeblendet wurde.<br/><br/>Weitere Informationen hierzu finden Sie unter [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md).  <br/> |
|Verschiedene  <br/> |"Control: …"  <br/> ||Die Datei enthält ein Steuerelement, das in Office 2013 oder vom Betriebssystem des Computers möglicherweise nicht unterstützt wird.<br/><br/>Weitere Informationen hierzu finden Sie unter [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md).  <br/> |
   
## <a name="conclusion"></a>Schlussbemerkung
<a name="OEV_Conclusion"> </a>

Telemetrieprotokoll bietet großen Unternehmen, einzelnen Benutzern und Entwicklern ein einfaches Instrument für die Überwachung wichtiger Office-Lösungen. Indem Unternehmen problematische Office-Lösungen vor einem groß angelegten Upgrade identifizieren, können sie die Kosten einer Einführung von Office 2013 besser abschätzen.
  
## <a name="see-also"></a>Siehe auch
<a name="OEV_Additional"> </a>

- [Office Developer Center](https://msdn.microsoft.com/office/aa905340.aspx)
- [Kompatibilitätsprobleme in Office](compatibility-issues-in-office.md)
- [Bereitstellen des Office-Telemetriedashboards](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717)
- [Office Developer Center](https://msdn.microsoft.com/office/aa905340)
    

