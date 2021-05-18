---
title: Weitere Konzepte zur InfoPath-Formularsicherheit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: Das Sicherheitsmodell von Microsoft InfoPath basiert auf dem von Internet Explorer implementierten Sicherheitsmodell. Das Sicherheitsmodell von Internet Explorer schützt Ihren Computer mithilfe von Sicherheitszonen und -stufen vor unsicheren Vorgängen. Zusammen mit dem Sicherheitsmodell von Internet Explorer bietet InfoPath zwei Formularbereitstellungsarten, die die Funktionsweise eines InfoPath-Formulars innerhalb dieses Sicherheitsmodells beeinflussen.
ms.openlocfilehash: 00b0e306507db19f55059fba91277af1ad1714b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303773"
---
# <a name="additional-infopath-form-security-concepts"></a>Weitere Konzepte zur InfoPath-Formularsicherheit

Das Sicherheitsmodell von Microsoft InfoPath basiert auf dem von Internet Explorer implementierten Sicherheitsmodell. Das Sicherheitsmodell von Internet Explorer schützt Ihren Computer mithilfe von Sicherheitszonen und -stufen vor unsicheren Vorgängen. Zusammen mit dem Sicherheitsmodell von Internet Explorer bietet InfoPath zwei Formularbereitstellungsarten, die die Funktionsweise eines InfoPath-Formulars innerhalb dieses Sicherheitsmodells beeinflussen.
  
- **URL-basierte Formulare** Diese Bereitstellungsmethode ist die Standardeinstellung beim Veröffentlichen eines Formulars von InfoPath auf einem Webserver, in einer SharePoint Foundation-Formularbibliothek oder einer Dateifreigabe. Diese Formulare werden als URL-basierte Formulare bezeichnet, da ein Benutzer das Formular in der Regel über die URL öffnet, unter der das Formular veröffentlicht wurde. Die URL ist im **publishUrl**-Attribut des **xDocumentClass**-Elements in der Formulardefinitionsdatei (XSF) angegeben. URL-basierte Formulare werden als Sandkastenformulare bezeichnet, weil sie nur über eingeschränkten Zugriff auf Systemressourcen und andere potenzielle Risikobereiche verfügen. Ein URL-basiertes Formular besitzt die gleiche Berechtigungsstufe wie eine Webseite, die vom gleichen Speicherort wie die Formularvorlagendatei (XSN) geöffnet wird.
    
- **URN-basierte Formulare** Diese Bereitstellungsmethode ist für Formulare geeignet, die Zugriff auf Systemressourcen und andere externe Ressourcen benötigen, z. B. ActiveX-Steuerelemente und andere Softwarekomponenten. Sie können InfoPath-Formulare als voll vertrauenswürdige Formulare bereitstellen. Solche Formulare werden auch als URN-basierte Formulare bezeichnet, da sie anstelle des **publishUrl**-Attributs einen URN (Uniform Resource Name) im **Name**-Attribut des **xDocumentClass**-Elements in der Formulardefinitionsdatei (XSF) angeben. Diese Formularklasse kann volle Vertrauenswürdigkeit anfordern, wenn das **requireFullTrust**-Attribut des **xDocumentClass**-Elements in der Formulardefinitionsdatei (XSF) auf `"yes"` festgelegt ist. URN-basierte Formulare müssen von einem Installationsprogramm oder Skript auf dem Clientcomputer registriert werden. In diesem Fall erhält das Formular die gleichen Berechtigungen wie eine Anwendung, die auf dem lokalen Computer ausgeführt wird. 
    
In Verbindung mit diesen beiden Methoden der Formularbereitstellung weist jede Methode und Eigenschaft des InfoPath-Objektmodells eine Sicherheitsstufe auf, die bestimmt, wann diese Methode oder Eigenschaft von einem im Formular ausgeführten Skript aufgerufen werden kann.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Grundlegendes zur InfoPath-Integration in das Sicherheitsmodell von Internet Explorer

Internet Explorer implementiert Sicherheitszonen, mit denen Sie die Zugriffsebene für Ihren Computer durch die von Ihnen geöffneten Webseiten steuern können. InfoPath bestimmt mithilfe einiger dieser Zonen die Zugriffsebene, die Formulare für die Ressourcen auf Ihrem Computer erhalten. Standardmäßig werden InfoPath-Formulare in einem zwischengespeicherten Speicherort ausgeführt, dem der Zugriff auf wichtige Systemressourcen verweigert wird. Formulare mit Vollzugriff auf Systemressourcen werden als voll vertrauenswürdige Formulare bezeichnet. Voll vertrauenswürdige Formulare werden gewöhnlich mithilfe eines Installationsprogramms oder Skripts installiert und registriert, oder sie sind digital signiert, sodass ihnen eine höhere Berechtigungsstufe erteilt werden kann.
  
Zwischengespeicherte InfoPath-Formulare werden durch die URL oder den URN identifiziert, die in der Formulardefinitionsdatei (XSF) des Formulars angegeben sind. Die Art der verwendeten Identifikation und die Domäne (Standort), von der aus die Formularvorlage geöffnet wird, bestimmen die Internet Explorer-Sicherheitszonenberechtigungen, die das Formular erbt. Durch eine URL identifizierte Formulare werden auf dem Computer des Benutzers zwischengespeichert, was die Offlineverwendung des Formulars ermöglicht. Diese URL-basierten Formulare erben Sicherheitsberechtigungen und spezielle Zugriffsrechte, z. B. domänenübergreifenden Zugriff, aus den Internet Explorer-Sicherheitseinstellungen für den ursprünglichen Speicherort der Formularvorlage. Auf einem Webserver oder einem Server mit SharePoint Foundation gespeicherte Formularvorlagen werden, abhängig von der Domäne des Servers, in der Internetzone oder der lokalen Intranetzone ausgeführt. Dagegen erben installierte Formulare, die durch einen URN identifiziert werden, die Berechtigungen von der Zone „Lokaler Computer“, die eine Berechtigungsstufe ähnlich der für HTML-Anwendungsdateien (.hta) gewährt.
  
Voll vertrauenswürdige Formulare werden durch ihren URN identifiziert und dadurch, ob das **requireFullTrust**-Attribut des **xDocumentClass**-Elements in der Formulardefinitionsdatei (.xsf) auf `"yes"` festgelegt ist. In InfoPath werden voll vertrauenswürdige Formulare nach der Installation auf der Registerkarte **Neu** in der Microsoft Office Backstage-Ansicht von InfoPath-Editor angezeigt. 
  
Eine ausführliche Erläuterung der Funktionsweise voll vertrauenswürdiger Formulare und wie sie erstellt und bereitgestellt werden finden Sie unter [Grundlegendes zu voll vertrauenswürdigen Formularen](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Installierten Formularen vertrauen

Die Verwendung vertrauenswürdiger Formulare kann auf einzelnen Computern aktiviert bzw. deaktiviert werden. Wenn ein Computer so konfiguriert ist, dass installierten Formularen vertraut wird, können die Benutzer Formulare ausfüllen, die den Zugriff auf die Ressourcen des Computers erfordern.
  
Im InfoPath-Editor konfigurieren Sie installierte Formulare auf einem Computer als in Backstage vertrauenswürdig, indem Sie auf **Optionen**, **Trust Center** und **Einstellungen für das Trust Center** klicken und anschließend im Dialogfeld **Trust Center** auf der Registerkarte **Vertrauenswürdige Herausgeber** das Kontrollkästchen **Ausführung vollständig vertrauenswürdiger Formulare auf diesem Computer zulassen** aktivieren. 
  
## <a name="using-security-features-in-infopath"></a>Verwenden von Sicherheitsfeatures in InfoPath

Das Sicherheitsmodell von InfoPath schützt die Benutzer vor den folgenden Bedrohungen durch von böswilligen Benutzern erstellten Vorlagen:
  
- Dem Potenzial für die Weitergabe vertraulicher Informationen von Ihrem lokalen Computer oder von Remotedatenquellen.
    
- Der Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten.
    
- Der Verwendung von Eigenschaften und Methoden aus dem InfoPath-Objektmodell mit böswilligen Absichten.
    
## <a name="cross-domain-data-access"></a>Domänenübergreifender Datenzugriff

Ein wesentliches Sicherheitsrisikoszenario wird als domänenübergreifender Datenzugriff bezeichnet.
  
Das Internet Explorer-Sicherheitsmodell, auf dem InfoPath basiert, enthält die Einstellung **Auf Datenquellen über Domänengrenzen hinweg zugreifen**. Standardmäßig wird mit dieser Einstellung der domänenübergreifende Zugriff für InfoPath-Formulare, die sich in den Sicherheitszonen „Internet“ und „Eingeschränkte Sites“ befinden, deaktiviert. Der Benutzer wird gefragt, ob der domänenübergreifende Zugriff für InfoPath-Formulare in der Sicherheitszone Lokales Intranet zugelassen werden soll, und der domänenübergreifende Zugriff für InfoPath-Formulare in den Zonen **Vertrauenswürdige Sites** oder **Lokaler Computer** wird aktiviert. 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Verwenden des HTML-Aufgabenbereichs von InfoPath

Der HTML-Aufgabenbereich von InfoPath ermöglicht das Rendern von Webseiten, wie z. B. HTM-, ASP- und HTA-Dateien. Die Seiten, auf die in Aufgabenbereichen verwiesen wird, können sich innerhalb oder außerhalb der Formularvorlage befinden. Bezüglich der Verweismöglichkeiten von außerhalb der Formularvorlage gilt lediglich die Einschränkung, dass sich die Webseite in derselben Domäne wie die Formularvorlage befinden muss, oder dass die Sicherheitszone der Vorlage die domänenübergreifenden Zugriffsberechtigungen zum Laden des Aufgabenbereichs zulassen muss.
  
Im Aufgabenbereich wird keine Adressleiste oder Statusleiste verfügbar gemacht. Deshalb ist der Benutzer nicht in der Lage, den Speicherort der Quelle für den Aufgabenbereich bzw. den Zugriff auf diesen Speicherort über einen verschlüsselten Kanal (HTTPS) zu bestätigen. Aus diesem Grund sollten Sie die Verwendung des Aufgabenbereichs zum Anzeigen oder Eingeben vertraulicher Informationen vermeiden. Der Aufgabenbereich ist für die Anzeige von dynamischen Hilfeinformationen und Steuerelementen für die Navigation zwischen Ansichten und anderen Elementen einer integrierten Lösung vorgesehen. Darüber hinaus können die Geschäftslogik und das Skript einer Formularvorlage im Aufgabenbereich interagieren. Diese Interaktion ist jedoch nur zulässig, wenn sich die Formularvorlage und der Aufgabenbereich in derselben Domäne befinden, wodurch verhindert wird, dass Informationen domänenübergreifend ausgetauscht werden.
  
## <a name="cross-domain-data-access-prompts"></a>Bestätigung für domänenübergreifenden Datenzugriff

Falls sich eine Formularvorlage, die den domänenübergreifenden Zugriff erfordert, in einer Sicherheitszone befindet, für die der domänenübergreifende Datenzugriff bestätigt werden muss (die Standardeinstellung für die Zone Lokales Intranet), wird der Benutzer gefragt, ob der Zugriff zugelassen werden soll. Die Auswahl des Benutzers gilt dann so lange, wie das Formular geöffnet ist. Wenn Sie InfoPath-Formularvorlagen bereitstellen müssen, die domänenübergreifenden Datenzugriff erfordern, sollten Sie diese Vorlagen als voll vertrauenswürdige Formulare bereitstellen oder aber sie auf einem Server in der Sicherheitszone Vertrauenswürdige Sites zur Verfügung stellen, damit die Benutzer den Zugriff nicht bestätigen müssen. Die Benutzer sollten nicht angewiesen werden, die Sicherheitsstufe der Zone Lokales Intranet zu reduzieren, um diese Bestätigungen zu vermeiden.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formulare ohne publishURL-Attribut

Wenn InfoPath eine Formularvorlage vom lokalen Computer lädt, deren **publishUrl**-Attribut leer ist oder fehlt, wird das Formular in einer eingeschränkteren Sicherheitszone abgelegt. Dadurch soll die Bedrohung durch böswillige Formularvorlagen verringert werden, die per E-Mail verteilt werden. Wenn der Benutzer diese Formularvorlage auf der Festplatte speichert, kann sie daher nicht mit den Berechtigungen eines Formulars ausgeführt werden, das sich in der Zone **Lokaler Computer** befindet. 
  
## <a name="unsafe-activex-controls"></a>Unsichere ActiveX-Steuerelemente

Das gängigste Szenario für die Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten ist denkbar, wenn ein Autor ein Skript mit einem ActiveX-Steuerelement verwendet, das Methoden für den Zugriff auf das Dateisystem bereitstellt, um persönliche Dateien und Kennwortlisten abzurufen, Dateien zu löschen oder das System des Benutzers zu deaktivieren. Ein InfoPath-Formular kann ActiveX-Steuerelemente nur in einem Skript in der Hauptskriptdatei eines Formulars (script.js) oder in einem Skript in einem Aufgabenbereich verwenden. In InfoPath dürfen mit einem Skript in InfoPath-Ansichten keine ActiveX-Steuerelemente ausgeführt werden.
  
Das Sicherheitsmodell von Internet Explorer, auf dem Microsoft InfoPath basiert, enthält die Einstellung **ActiveX-Steuerelemente initialisieren und ausführen, die nicht sicher sind**, die standardmäßig zu den folgenden Aktionen für InfoPath-Formulare oder Aufgabenbereiche führt, in denen versucht wird, als nicht sicher markierte ActiveX-Steuerelemente zu initialisieren und auszuführen. 
  
|**Sicherheitszone/Bereitstellung**|**Aktion**|
|:-----|:-----|
|Internet  <br/> |Deaktiviert  <br/> |
|Lokales Intranet  <br/> |Deaktiviert  <br/> |
|Eingeschränkte Sites  <br/> |Deaktiviert  <br/> |
|Vertrauenswürdige Sites  <br/> |Eingabeaufforderung  <br/> |
|Arbeitsplatz  <br/> |Eingabeaufforderung  <br/> |
|Voll vertrauenswürdiges Formular  <br/> |Aktivieren  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Verwendung des InfoPath-Objektmodells mit böswilligen Absichten

Ähnlich wie von Skript aufgerufene ActiveX-Steuerelemente können von Code aufgerufene InfoPath-Methoden und -Eigenschaften verschiedene Risikostufen darstellen. Beispielsweise kann die [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)-Methode der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)-Klasse zum Schreiben von Daten an einer beliebigen Stelle im Dateisystem verwendet werden. 
  
Für den Schutz vor der Verwendung von InfoPath-Objektmodellmembern mit böswilligen Absichten implementiert das InfoPath-Objektmodell drei Sicherheitsstufen, die bestimmen, wie und wo ein bestimmtes Objektmodellmember verwendet werden kann. Im InfoPath-Objektmodell gibt es drei Sicherheitsstufen:
  
- **0** Objektmodellmember, auf die uneingeschränkt zugegriffen werden kann. Diese Objektmodellmember sind sicher, weshalb uneingeschränkt darauf zugegriffen werden kann. 
    
- 2 Objektmodellmember, auf die nur über Formulare zugegriffen werden kann, die in derselben Domäne wie das zurzeit geöffnete Formular ausgeführt werden, oder über Formulare, denen Berechtigungen für den domänenübergreifende Datenzugriff erteilt wurden. Eingeschränkte Formularvorlagen, die Objektmodellmethoden der Sicherheitsstufe 2 aufrufen, sind nur erfolgreich, wenn auf in der Formularvorlage selbst enthaltene Ressourcen zugegriffen wird. 
    
- **3** Objektmodellmember, auf die nur über voll vertrauenswürdige Formulare zugegriffen werden kann. 
    
- Alle Themen für die Eigenschaften und Methoden in der Referenz zum InfoPath-Objektmodell enthalten einen Abschnitt zur Sicherheit, in dem die für diesen Objektmodellmember geltende Sicherheitsstufe beschrieben wird.
    
- Die Sicherheitsstufe **1** ist für künftige Zwecke vorbehalten. 
    
## <a name="summary"></a>Zusammenfassung

Die folgende Tabelle enthält eine Zusammenfassung der Standardberechtigungen für die verschiedenen Methoden der Formularbereitstellung in InfoPath. Die Berechtigungen basieren auf der Sicherheitszone für die Domänen, aus der die Formularvorlage stammt.
  
|**Sicherheitszone**|**Bereitstellung**|**Standardberechtigungen**|
|:-----|:-----|:-----|
||**URL-basiert** <br/> |**URN-basiert** <br/> |**ActiveX als unsicher für Skripts markiert** <br/> |**Domänenübergreifender Datenzugriff** <br/> |**Objektmodell-Sicherheitsstufe** <br/> |
|Eingeschränkte Sites  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |
|Internet  <br/> |X  <br/> ||Deaktivieren  <br/> |Deaktivieren  <br/> |2  <br/> |
|Lokales Intranet  <br/> |X  <br/> ||Deaktivieren  <br/> |Eingabeaufforderung  <br/> |2  <br/> |
|Vertrauenswürdige Sites  <br/> |X  <br/> ||Eingabeaufforderung  <br/> |Aktivieren  <br/> |2  <br/> |
|Lokaler Computer  <br/> |X  <br/> |X  <br/> |Deaktivieren  <br/> |Eingabeaufforderung  <br/> |2  <br/> |
|Voll vertrauenswürdiges Formular  <br/> |X (signiert von einem vertrauenswürdigen Herausgeber)  <br/> |X  <br/> |Aktivieren  <br/> |Aktivieren  <br/> |3  <br/> |
|Voll vertrauenswürdiges Formular  <br/> ||X  <br/> |Aktivieren  <br/> |Aktivieren  <br/> |3  <br/> |
|Eingeschränkt  <br/> ||X  <br/> |Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
|Eingeschränkt  <br/> |X  <br/> ||Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
|Eingeschränkt  <br/> |X  <br/> |X  <br/> |Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
   
Weitere Informationen zu allgemeinen Sicherheitsrichtlinien beim Entwickeln von Formularen finden Sie unter [Sicherheitsrichtlinien für das Entwickeln von InfoPath-Formularen](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Grundlegendes zu weiteren Sicherheitsfeatures

InfoPath bietet weitere Sicherheitsmaßnahmen für Formulare, wie beispielsweise den Schutz des Formularentwurfs mithilfe digitaler Signaturen, die Verwaltung bestimmter Formularvorgänge wie das Zusammenführen und Senden sowie die Vertrauenswürdigkeit installierter Formulare. In den folgenden Abschnitten werden diese Sicherheitsmaßnahmen für Formulare beschrieben und es wird darauf hingewiesen, wo diese in InfoPath aktiviert werden.
  
## <a name="digital-signatures"></a>Digitale Signaturen

Die Daten in einem Formular können digital signiert werden, um sicherzustellen, dass dessen Inhalt nicht geändert wird.
  
Sie konfigurieren die Verwendung digitaler Signaturen in einem Formular, indem Sie im Dialogfeld **Formularoptionen** im Abschnitt **Digitale Signaturen** die Option **Signieren des gesamten Formulars erlauben** oder **Signieren von Teilen des Formulars erlauben** auswählen. Dieses Dialogfeld ist in Microsoft Office Backstage im InfoPath-Formulardesigner verfügbar. Beim Ausfüllen des Formulars können die Benutzer dann Formulare signieren und überprüfen, indem sie in Microsoft Office Backstage auf der Registerkarte **Info** auf die Schaltfläche **Formular signieren** klicken. Wenn das Formular erneut geöffnet wird, wird der Benutzer gewarnt, falls der Inhalt des Formulars geändert wurde. 
  
-  Digitale Signaturen können für das gesamte Formular oder für bestimmte Gruppen von Daten in dem Formular aktiviert werden, die separat signiert werden können. 
    
- Sie können festlegen, dass anstelle des gesamten Formulars nur bestimmte Abschnitte eines Formulars signiert werden können.
    
- Sie können angeben, ob einzelne oder mehrere Signaturen zulässig sind. Außerdem können Sie für jede signierbare Datengruppe angeben, in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Mit dem InfoPath-Objektmodell können Sie dem Signaturblock in einem voll vertrauenswürdigen Formular programmgesteuert benutzerdefinierte Informationen hinzufügen.
    
- Die Sicherheit digitaler Signaturen können Sie durch die Erfassung und Einbindung zusätzlicher Informationen (wie z. B. einen Zeitstempel) als Nichtabstreitbarkeitsnachweis optimieren. Da der zusätzliche Nachweis Bestandteil der Signatur ist, kann er nicht entfernt werden, ohne dass die Signatur ungültig wird. Diese Daten können jederzeit erneut aufgerufen oder analysiert werden, indem Sie im Formular auf eine digitale Signatur klicken, oder indem Sie in der im Dialogfeld **Digitale Signatur** angezeigten Liste der digitalen Signaturen eine digitale Signatur auswählen. 
    
-  Sie können eine Signatur im Dokument einfügen und anzeigen sowie das Formular so anzeigen, wie es jeder signierenden Person vorgelegt wurde. 
    
- Die digitale Signatur enthält auch eine Momentaufnahme der Ansicht, so wie diese für die signierende Person beim Signieren des Formulars angezeigt wurde. Die Momentaufnahme wird als Base64-codiertes Bild im standardmäßigen PNG-Dateiformat gespeichert.  
    
## <a name="email-deployment"></a>E-Mail-Bereitstellung

Sie können Ihre Formularvorlagen als E-Mail-Anlage bereitstellen und die Formularvorlagen zwischen Speicherorten verschieben. Die Bereitstellung per E-Mail ist eine einfache und effektive Methode zum Verteilen von Formularen für die firmeninterne Verwendung und zum Bereitstellen von Formularen für Remotebenutzer.
  
Sie können eine von Ihnen entworfene Formularvorlage digital signieren und anschließend die Sicherheitsstufe für diese Formularvorlage auf Voll vertrauenswürdig festlegen. Darüber hinaus können signierte voll vertrauenswürdige Formulare, die als E-Mail-Anlage bereitgestellt werden, einfacher und effizienter aktualisiert werden.
  
Alle Formulare in InfoPath Designer werden mit einer Identität erstellt. Mit diesen Informationen kann InfoPath Formularen Formularvorlagen im Cache zuordnen und Aktualisierungen für Formulare abrufen, wenn diese in einem freigegebenen Speicherort verfügbar gemacht werden. Standardmäßig werden von InfoPath zwei Identitäten für Formularvorlagen erstellt: eine Formular-ID und ein Zugriffspfad (auch als **publishURL**-Attribut bezeichnet). Weitere Informationen zur Bereitstellung per E-Mail finden Sie im Thema [Sicherheitsstufen, E-Mail-Bereitstellung und Remoteformularvorlagen](security-levels-email-deployment-and-remote-form-templates.md).
  
## <a name="activex-controls"></a>ActiveX-Steuerelemente

InfoPath unterstützt das Hosten von ActiveX-Steuerelementen in Formularen, die im InfoPath-Editor geöffnet werden. Die ActiveX-Steuerelemente können (mit einigen Einschränkungen) bereits vorhandenen sein oder speziell für die Verwendung mit InfoPath geschrieben werden. ActiveX-Steuerelemente, die in InfoPath-Formularen verwendet werden, werden nicht automatisch von Websites heruntergeladen. Stattdessen müssen CAB-Dateien für die ActiveX-Steuerelemente, die noch nicht auf dem Computer des Benutzers vorhanden sind, zur Formularvorlagendatei hinzugefügt werden.
  
Wenn ein ActiveX-Steuerelement in einem Formular verwendet wird und das Steuerelement nicht auf dem Computer des Benutzers registriert ist, hängt das Verhalten beim Öffnen des Formulars von den Einstellungen des ActiveX-Steuerelements innerhalb des Formulars ab. Das Formular wird von InfoPath nicht geöffnet, falls in der Formularvorlagendatei keine CAB-Datei vorhanden ist. InfoPath startet einen Installationsvorgang, falls die CAB-Datei in der Formularvorlagendatei vorhanden ist. Die Datei muss signiert sein, und die Signatur muss von einem vertrauenswürdigen Herausgeber stammen, damit eine CAB-Datei von InfoPath installiert wird. Wenn der Herausgeber noch nicht in der Liste vertrauenswürdiger Herausgeber des Benutzers aufgeführt ist, für die ein Zertifikat vorhanden ist (mit einer Vertrauenskette zu einem vertrauenswürdigen Stammzertifikat), wird der Benutzer aufgefordert, die Vertrauensstellung für den Herausgeber anzunehmen oder abzulehnen. Vertraut der Benutzer dem Herausgeber nicht, wird die CAB-Datei für das Steuerelement nicht installiert, und das Formular wird nicht von InfoPath geöffnet.
  
> [!NOTE]
> ActiveX-Steuerelemente müssen als Safe for scripting und Safe for initialization with untrusted data markiert sein, um in InfoPath verwendet zu werden. 
  
## <a name="net-security"></a>.NET-Sicherheit

Neben InfoPath-spezifischen Sicherheitsstufen werden von Formularvorlagen mit verwaltetem Code zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von Microsoft .NET Framework ausgeführt wird.
  
Wenn Ihr Formular voll vertrauenswürdig ist, kann damit automatisch auf Ressourcen außerhalb der Formularvorlage zugegriffen werden. Jede Assembly kann im Geschäftslogikcode verwendet werden. Den Berechtigungssatz, der einer Formularvorlage mit verwaltetem Code hinzugefügt wird, können Sie mit dem Microsoft .NET Framework-Konfigurationstool oder dem Sicherheitsrichtlinientool für den Codezugriff (Caspol.exe) anpassen. InfoPath sucht nach einer vordefinierten Codegruppe und wendet den unter dieser Gruppe definierten Berechtigungssatz auf die Anwendungsdomäne (AppDomain) an, in der der verwaltete Code geladen wird und in der er ausgeführt wird. Benutzerdefinierte .NET-Sicherheitsrichtlinien müssen auf Clientcomputern bereitgestellt werden, auf denen die Formularvorlage mit verwaltetem Code ausgeführt wird.
  
Beachten Sie, dass von der .NET-Sicherheit der Berechtigungssatz Internet nur für verwalteten Code erteilt wird, der in Internet Explorer als vertrauenswürdige Sites ausgeführt wird. Deshalb werden Formulare mit verwaltetem Code von InfoPath nicht ausgeführt, wenn sie in einer vertrauenswürdigen Site veröffentlicht werden.
  
## <a name="merging-forms"></a>Zusammenführen von Formularen

Sie können das Zusammenführen von Formularen deaktivieren, um zu verhindern, dass Benutzer Daten aus mehreren Formularen in ein einziges Formular importieren.
  
Sie aktivieren oder deaktivieren das Zusammenführen von Formularen mithilfe des Kontrollkästchens **Zusammenführen von Formularen aktivieren** im Dialogfeld **Formularoptionen** im Abschnitt **Erweitert**. Das Dialogfeld ist beim Entwerfen des Formulars über die Registerkarte **Info** von Microsoft Office Backstage verfügbar. Wenn das Zusammenführen von Formularen deaktiviert ist, können Benutzer beim Ausfüllen eines Formulars in Microsoft Office Backstage nicht auf der Registerkarte **Freigeben** auf **Formulare zusammenführen** klicken. 
  
## <a name="submitting-forms"></a>Senden von Formularen

Sie können das Feature zum Senden von Formularen deaktivieren, um Benutzer am Senden von Formularen zu hindern.
  
Das Senden von Formularen können Sie im Dialogfeld **Absendeoptionen** aktivieren bzw. deaktivieren. Dieses Dialogfeld wird angezeigt, wenn Sie im Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen** klicken. Wenn das Senden von Formularen deaktiviert ist, können Benutzer beim Ausfüllen eines Formulars nicht auf der Registerkarte **Start** auf **Absenden** klicken. 
  

