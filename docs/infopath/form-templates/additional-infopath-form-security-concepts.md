---
title: Zusätzliche Sicherheitskonzepte für InfoPath-Formulare
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: Das Sicherheitsmodell von Microsoft InfoPath basiert auf dem Sicherheitsmodell von Internet Explorer implementiert. Das Sicherheitsmodell von Internet Explorer trägt zum Schutz von Ihrem Computers vor unsicheren Vorgängen mithilfe von Sicherheitszonen und Sicherheitsstufen. Zusammen mit dem Sicherheitsmodell von Internet Explorer arbeiten, bietet InfoPath für zwei Arten der Formular-Bereitstellung, die beeinflussen, wie ein InfoPath-Formular innerhalb dieses Sicherheitsmodell funktioniert.
ms.openlocfilehash: dc155e2c2962e2cca2b4465e5a9632f92488cef9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790715"
---
# <a name="additional-infopath-form-security-concepts"></a>Zusätzliche Sicherheitskonzepte für InfoPath-Formulare

Das Sicherheitsmodell von Microsoft InfoPath basiert auf dem Sicherheitsmodell von Internet Explorer implementiert. Das Sicherheitsmodell von Internet Explorer trägt zum Schutz von Ihrem Computers vor unsicheren Vorgängen mithilfe von Sicherheitszonen und Sicherheitsstufen. Zusammen mit dem Sicherheitsmodell von Internet Explorer arbeiten, bietet InfoPath für zwei Arten der Formular-Bereitstellung, die beeinflussen, wie ein InfoPath-Formular innerhalb dieses Sicherheitsmodell funktioniert.
  
- **URL-basierte Formulare** Diese Bereitstellungsmethode ist die Standardeinstellung beim Veröffentlichen eines Formulars von InfoPath-Formularen auf einem Webserver, SharePoint Foundation-Formularbibliothek oder Dateifreigabe. Diese Formulare werden als URL-basierte Formulare bezeichnet, da ein Benutzer öffnet das Formular in der Regel von der URL, in dem das Formular veröffentlicht wird, und, die URL im **PublishUrl** -Attribut des **xDocumentClass** -Element in der Formulardefinitionsdatei (XSF) angegeben ist. URL-basierte Formulare werden als sandboxed, da sie über eingeschränkten Zugriff auf Systemressourcen und andere potenzielle Bereiche der Risiko haben. Ein URL-basiertes Formular verfügt über dieselben Berechtigungen als Webseite, die in den gleichen Speicherort wie die Formularvorlagendatei (XSN) geöffnet ist.
    
- **URN-basierte Formulare** Diese Bereitstellungsmethode ist für Formulare, die Zugriff auf Systemressourcen und andere externen Ressourcen, wie ActiveX-Steuerelemente und sonstige Softwarekomponenten erforderlich. Sie können InfoPath-Formulare als voll vertrauenswürdige Formulare bereitstellen. Solche Formulare werden auch bekannt als URN-basierte Formulare, da anstelle von **PublishUrl** -Attribut angeben, diese Uniform Resource Name (URN) im **Name** -Attribut des **xDocumentClass** -Element in der Formulardefinitionsdatei (XSF) angeben. Diese Klasse des Formulars kann volle Vertrauenswürdigkeit anfordern, wenn das **RequireFullTrust** -Attribut des **xDocumentClass** -Element, um festgelegt ist `"yes"` in der Formulardefinitionsdatei (XSF). URN-basierte Formulare müssen von einem Installationsprogramm oder Skript auf dem Clientcomputer registriert werden. In diesem Fall erhält das Formular dieselben Berechtigungen wie für eine Anwendung, die auf dem lokalen Computer ausgeführt wird. 
    
In Verbindung mit diesen beiden Methoden der Formularbereitstellung weist jede Methode und Eigenschaft des InfoPath-Objektmodells eine Sicherheitsstufe auf, die bestimmt, wann diese Methode oder Eigenschaft von einem im Formular ausgeführten Skript aufgerufen werden kann.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Grundlegendes zur InfoPath-Integration mit dem Sicherheitsmodell von Internet Explorer

Internet Explorer implementiert Sicherheitszonen, mit denen Sie steuern, welche Zugriffstyp an Ihren Computer durch die Webseiten, die Sie öffnen. InfoPath verwendet einige dieser Zonen, um die Zugriffsebene zu ermitteln, die Formulare, die die Ressourcen auf Ihrem Computer erteilt werden. Standardmäßig werden InfoPath-Formulare in einem zwischengespeicherten Speicherort, der Zugriff auf kritische Systemressourcen verweigert wird ausgeführt. Formulare, die vollen Zugriff auf Systemressourcen werden voll vertrauenswürdige Formulare bezeichnet. Voll vertrauenswürdige Formulare in der Regel installiert und registriert, indem ein Installationsprogramm oder Skript, oder sie sind digital signiert, damit eine höhere Berechtigungen gewährt werden können.
  
Zwischengespeicherte InfoPath-Formulare werden durch die URL oder in der Formulardefinitionsdatei (XSF) des Formulars angegebenen URN identifiziert. Die Art der verwendeten Identifikation und die Domäne (Speicherort), von der aus die Formularvorlage geöffnet wird, bestimmt, welche Internet Explorer-Zone Sicherheitsberechtigungen die das Formular erben. Durch eine URL identifizierte Formulare werden auf dem Computer des Benutzers, zwischengespeichert Offlineverwendung des Formulars ermöglicht. Diese URL-basierte Formulare erben ihre Sicherheitsberechtigungen und ihren spezifischen Zugriffsrechten wie domänenübergreifenden Zugriff, von der Einstellungen für Internet Explorer-Sicherheit für den ursprünglichen Speicherort der Formularvorlage gelten. Formularvorlagen, die auf einem Webserver oder einem Server mit SharePoint Foundation ausführen in das Internet oder der lokalen Intranetzone, abhängig von der Domäne des Servers gespeichert. Installierte Formulare, die mit einem URN identifiziert werden erben die Berechtigungen andererseits, von der Zone lokaler Computer, eine Berechtigungsstufe für HTML-Anwendungsdateien (.hta) ähnlich gewährt.
  
Voll vertrauenswürdige Formulare werden durch ihren URN und gibt an, ob das **RequireFullTrust** -Attribut des **xDocumentClass** -Element in der Formulardefinitionsdatei (XSF) festgelegt ist identifiziert `"yes"`. In InfoPath Wenn voll vertrauenswürdige Formulare installiert sind, werden sie angezeigt auf der Registerkarte **neu** in Microsoft Office Backstage des InfoPath-Editor. 
  
Eine ausführliche Erläuterung der Funktionsweise voll vertrauenswürdiger Formulare und zum Erstellen und Bereitstellen finden Sie unter [Grundlegendes zu voll vertrauenswürdigen Formularen](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Vertrauenswürdigkeit installierter Formulare

Die Verwendung vertrauenswürdiger Formulare kann auf einzelnen Computern aktiviert bzw. deaktiviert werden. Wenn ein Computer so konfiguriert ist, dass installierten Formularen vertraut wird, können die Benutzer Formulare ausfüllen, die den Zugriff auf die Ressourcen des Computers erfordern.
  
In der InfoPath-Editor konfigurieren Sie einen Computer installierte Formulare in der Backstage-Ansicht als vertrauenswürdig, indem Sie auf **Optionen**, **Trust Center**, **Trust Center-Einstellungen**und dann auswählen das Kontrollkästchen **Zulassen voll vertrauenswürdige Formulare auf meinem Computer ausgeführt** Feld auf der Registerkarte **Vertrauenswürdige Herausgeber** im Dialogfeld **Sicherheitscenter** . 
  
## <a name="using-security-features-in-infopath"></a>Verwenden von Sicherheitsfeatures in InfoPath

Das Sicherheitsmodell von InfoPath schützt die Benutzer vor den folgenden Bedrohungen durch von böswilligen Benutzern erstellten Vorlagen:
  
- Dem Potenzial für die Weitergabe vertraulicher Informationen von Ihrem lokalen Computer oder von Remotedatenquellen.
    
- Der Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten.
    
- Der Verwendung von Eigenschaften und Methoden aus dem InfoPath-Objektmodell mit böswilligen Absichten.
    
## <a name="cross-domain-data-access"></a>Domänenübergreifender Datenzugriff

Sicherheitsrisiko wird als domänenübergreifender Datenzugriff bezeichnet.
  
Das Sicherheitsmodell für Internet Explorer, dem InfoPath basiert enthält eine Einstellung namens **auf Datenquellen über Domänengrenzen hinweg zugreifen**. Diese Einstellung deaktiviert standardmäßig domänenübergreifenden Zugriff für InfoPath-Formulare, die sich in der Internet- und eingeschränkte Sites Sicherheitszonen befinden. Es fordert den Benutzer zulassen oder Verweigern des domänenübergreifenden Zugriffs für InfoPath-Formulare, die sich in der lokalen Intranetzone befinden, und dadurch können domänenübergreifenden Zugriff für InfoPath-Formulare, die sich in den Zonen **Vertrauenswürdige Sites** oder einem **Lokalen Computer** befinden. 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Verwenden des HTML-Aufgabenbereichs von InfoPath

Der HTML-Aufgabenbereich von InfoPath ermöglicht das Rendern von Webseiten, wie z. B. HTM-, ASP- und HTA-Dateien. Die Seiten, auf die in Aufgabenbereichen verwiesen wird, können sich innerhalb oder außerhalb der Formularvorlage befinden. Bezüglich der Verweismöglichkeiten von außerhalb der Formularvorlage gilt lediglich die Einschränkung, dass sich die Webseite in derselben Domäne wie die Formularvorlage befinden muss, oder dass die Sicherheitszone der Vorlage die domänenübergreifenden Zugriffsberechtigungen zum Laden des Aufgabenbereichs zulassen muss.
  
Im Aufgabenbereich wird keine Adressleiste oder Statusleiste verfügbar gemacht. Deshalb ist der Benutzer nicht in der Lage, den Speicherort der Quelle für den Aufgabenbereich bzw. den Zugriff auf diesen Speicherort über einen verschlüsselten Kanal (HTTPS) zu bestätigen. Aus diesem Grund sollten Sie die Verwendung des Aufgabenbereichs zum Anzeigen oder Eingeben vertraulicher Informationen vermeiden. Der Aufgabenbereich ist für die Anzeige von dynamischen Hilfeinformationen und Steuerelementen für die Navigation zwischen Ansichten und anderen Elementen einer integrierten Lösung vorgesehen. Darüber hinaus können die Geschäftslogik und das Skript einer Formularvorlage im Aufgabenbereich interagieren. Diese Interaktion ist jedoch nur zulässig, wenn sich die Formularvorlage und der Aufgabenbereich in derselben Domäne befinden, wodurch verhindert wird, dass Informationen domänenübergreifend ausgetauscht werden.
  
## <a name="cross-domain-data-access-prompts"></a>Bestätigung für domänenübergreifenden Datenzugriff

Falls sich eine Formularvorlage, die den domänenübergreifenden Zugriff erfordert, in einer Sicherheitszone befindet, für die der domänenübergreifende Datenzugriff bestätigt werden muss (die Standardeinstellung für die Zone Lokales Intranet), wird der Benutzer gefragt, ob der Zugriff zugelassen werden soll. Die Auswahl des Benutzers gilt dann so lange, wie das Formular geöffnet ist. Wenn Sie InfoPath-Formularvorlagen bereitstellen müssen, die domänenübergreifenden Datenzugriff erfordern, sollten Sie diese Vorlagen als voll vertrauenswürdige Formulare bereitstellen oder aber sie auf einem Server in der Sicherheitszone Vertrauenswürdige Sites zur Verfügung stellen, damit die Benutzer den Zugriff nicht bestätigen müssen. Die Benutzer sollten nicht angewiesen werden, die Sicherheitsstufe der Zone Lokales Intranet zu reduzieren, um diese Bestätigungen zu vermeiden.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formulare ohne publishURL-Attribut

Wenn InfoPath eine Formularvorlage aus dem lokalen Computer lädt, und es ein leerer **PublishUrl** -Attribut wurde oder das Attribut fehlt, wird das Formular in einer restriktiveren Sicherheitszone platziert werden. Dies wird ausgeführt, um die Bedrohung einer böswilligen Formularvorlage per e-Mail verteilt wird zu reduzieren. Vorkommen, wenn der Benutzer auf der Festplatte gespeichert werden kann nicht mit den Berechtigungen eines Formulars ausgeführt werden, die in der Zone des **Lokalen Computers** befindet. 
  
## <a name="unsafe-activex-controls"></a>Unsichere ActiveX-Steuerelemente

Das gängigste Szenario für die Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten ist denkbar, wenn ein Autor ein Skript mit einem ActiveX-Steuerelement verwendet, das Methoden für den Zugriff auf das Dateisystem bereitstellt, um persönliche Dateien und Kennwortlisten abzurufen, Dateien zu löschen oder das System des Benutzers zu deaktivieren. Ein InfoPath-Formular kann ActiveX-Steuerelemente nur in einem Skript in der Hauptskriptdatei eines Formulars (script.js) oder in einem Skript in einem Aufgabenbereich verwenden. In InfoPath dürfen mit einem Skript in InfoPath-Ansichten keine ActiveX-Steuerelemente ausgeführt werden.
  
Das Sicherheitsmodell für Internet Explorer, dem Microsoft InfoPath basiert, bietet die eine Einstellung für die **als nicht sicher markiert ActiveX-Steuerelemente initialisieren und Ausführen** , die in der Standardeinstellung führt die folgenden Aktionen für InfoPath-Formulare oder Aufgabenbereiche, die versuchen zum Initialisieren und ausführen, ActiveX-Steuerelemente, die als unsicher für Skripts markiert sind. 
  
|**Sicherheitszone/Bereitstellung**|**Aktion**|
|:-----|:-----|
|Internet  <br/> |Deaktiviert  <br/> |
|Lokales Intranet  <br/> |Deaktiviert  <br/> |
|Eingeschränkte Sites  <br/> |Deaktiviert  <br/> |
|Vertrauenswürdige Sites  <br/> |Eingabeaufforderung  <br/> |
|Arbeitsplatz  <br/> |Eingabeaufforderung  <br/> |
|Voll vertrauenswürdiges Formular  <br/> |Aktivieren  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Verwendung des InfoPath-Objektmodells mit böswilligen Absichten

In ähnlicher Weise können ActiveX-Steuerelemente wird vom Skript aufgerufen, InfoPath-Methoden und Eigenschaften, die aus Code aufgerufen verschiedene Risiko darstellen. Beispielsweise kann die [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) -Methode der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zum Schreiben von Daten an einer beliebigen Stelle im Dateisystem verwendet werden. 
  
Für den Schutz vor der Verwendung von InfoPath-Objektmodellmembern mit böswilligen Absichten implementiert das InfoPath-Objektmodell drei Sicherheitsstufen, die bestimmen, wie und wo ein bestimmtes Objektmodellmember verwendet werden kann. Im InfoPath-Objektmodell gibt es drei Sicherheitsstufen:
  
- **0** -Objektmodellmember, die uneingeschränkt zugegriffen werden können. Diese Elemente des Objektmodells sicher sind und daher uneingeschränkt zugegriffen werden können. 
    
- **2** -Objektmodellmember, die nur durch Formulare, die in derselben Domäne wie das zurzeit geöffnete Formular ausgeführt wird, oder durch Formulare, die domänenübergreifenden Datenzugriff erteilt wurden zugegriffen werden können Zugriffsberechtigungen. Eingeschränkte Formularvorlagen, die Sicherheit Ebene 2 Methoden aufrufen nur erfolgreich, wenn sie in der Formularvorlage selbst enthaltene Ressourcen zugreifen. 
    
- **3** Objektmodellmember, die nur durch voll vertrauenswürdige Formulare zugegriffen werden können. 
    
- Alle Themen für die Eigenschaften und Methoden in der Referenz zum InfoPath-Objektmodell enthalten einen Abschnitt zur Sicherheit, in dem die für diesen Objektmodellmember geltende Sicherheitsstufe beschrieben wird.
    
- Sicherheit Ebene **1** ist für die zukünftige Verwendung reserviert. 
    
## <a name="summary"></a>Zusammenfassung

Die folgende Tabelle enthält eine Zusammenfassung der Standardberechtigungen für die verschiedenen Methoden der Formularbereitstellung in InfoPath. Die Berechtigungen basieren auf der Sicherheitszone für die Domänen, aus der die Formularvorlage stammt.
  
|**Sicherheitszone**|**Bereitstellung**|**Standardberechtigungen**|
|:-----|:-----|:-----|
||**URL-basierte** <br/> |**URN-basierte** <br/> |**ActiveX als unsicher für Skripts markiert** <br/> |**Cross-Domain Data Access** <br/> |**Sicherheitsebene des Objektmodells** <br/> |
|Eingeschränkte Sites  <br/> |N/v  <br/> |n/v  <br/> |n/v  <br/> |n/v  <br/> |N/v  <br/> |
|Internet  <br/> |X  <br/> ||Deaktivieren  <br/> |Deaktivieren  <br/> |2  <br/> |
|Lokales Intranet  <br/> |X  <br/> ||Deaktivieren  <br/> |Eingabeaufforderung  <br/> |2  <br/> |
|Vertrauenswürdige Sites  <br/> |X  <br/> ||Eingabeaufforderung  <br/> |Aktivieren  <br/> |2  <br/> |
|Lokaler Computer  <br/> |X  <br/> |X  <br/> |Deaktivieren  <br/> |Eingabeaufforderung  <br/> |2  <br/> |
|Voll vertrauenswürdiges Formular  <br/> |X (signiert von einem vertrauenswürdigen Herausgeber)  <br/> |X  <br/> |Aktivieren  <br/> |Aktivieren  <br/> |3  <br/> |
|Voll vertrauenswürdiges Formular  <br/> ||X  <br/> |Aktivieren  <br/> |Aktivieren  <br/> |3  <br/> |
|Eingeschränkt  <br/> ||X  <br/> |Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
|Eingeschränkt  <br/> |X  <br/> ||Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
|Eingeschränkt  <br/> |X  <br/> |X  <br/> |Kein ActiveX (außer einer beschränkten hartcodierten Liste)  <br/> |Deaktivieren  <br/> |2  <br/> |
   
Weitere Informationen zur allgemeinen Sicherheit bei der Entwicklung von Formularen finden Sie unter [Sicherheitsrichtlinien für das Entwickeln von InfoPath-Formularen](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Grundlegendes zu weiteren Sicherheitsfeatures

InfoPath bietet weitere Sicherheitsmaßnahmen für Formulare, wie beispielsweise den Schutz des Formularentwurfs mithilfe digitaler Signaturen, die Verwaltung bestimmter Formularvorgänge wie das Zusammenführen und Senden sowie die Vertrauenswürdigkeit installierter Formulare. In den folgenden Abschnitten werden diese Sicherheitsmaßnahmen für Formulare beschrieben und es wird darauf hingewiesen, wo diese in InfoPath aktiviert werden.
  
## <a name="digital-signatures"></a>Digitale Signaturen

Die Daten in einem Formular können digital signiert werden, um sicherzustellen, dass dessen Inhalt nicht geändert wird.
  
Konfigurieren Sie ein Formular, um digitale Signaturen verwenden, indem Sie die Option **Zulassen Signieren des gesamten Formulars** oder **Teile des Formulars signieren zulassen** auf Abschnitt **Digitale Signaturen** im Dialogfeld **Formularoptionen** auswählen das aus verfügbar ist die Microsoft Office Backstage im InfoPath-Formular-Designer. Beim Ausfüllen des Formulars können Benutzer dann anmelden und Formulare überprüfen, indem Sie auf die Schaltfläche **Sign-Formular** auf der Registerkarte **Info** die Microsoft Office Backstage. Wenn das Formular erneut geöffnet wird, wird der Benutzer benachrichtigt werden, wenn der Inhalt des Formulars geändert wurde. 
  
-   Digitale Signaturen können für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können, zugelassen werden. 
    
- Sie können festlegen, dass anstelle des gesamten Formulars nur bestimmte Abschnitte eines Formulars signiert werden können.
    
- Sie können angeben, ob einzelne oder mehrere Signaturen zulässig sind. Außerdem können Sie für jede signierbare Datengruppe angeben, in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Mit dem InfoPath-Objektmodell können dem Signaturblock in einem voll vertrauenswürdigen Formular programmgesteuert benutzerdefinierte Informationen hinzugefügt werden.
    
- Sie können die Sicherheit von digitalen Signaturen durch das Erfassen und einschließlich zusätzlicher Informationen, wie einen Zeitstempel, als Beweis der Nichtabstreitbarkeit verbessern. Da der zusätzliche Beweis Teil der Signatur ist, kann es der Signatur entfernt werden. Sie können jederzeit jederzeit zurückrufen oder die erfassten Daten untersuchen, indem Sie auf eine digitale Signatur im Formular oder, indem Sie eine digitale Signatur aus der Liste der digitalen Signaturen im Dialogfeld **Digitale Signaturen** angezeigt. 
    
-   Sie können eine Signatur im Dokument einfügen und anzeigen sowie das Formular so anzeigen, wie es jeder signierenden Person vorgelegt wurde. 
    
- Die digitale Signatur enthält auch eine Momentaufnahme der Ansicht, so wie diese für die signierende Person beim Signieren des Formulars angezeigt wurde. Die Momentaufnahme wird als Base64-codiertes Bild im standardmäßigen PNG-Dateiformat gespeichert.  
    
## <a name="email-deployment"></a>E-Mail-Bereitstellung

Bereitstellen von Formularvorlagen als Anlage einer e-Mail-Nachricht und die Formularvorlagen von einem Speicherort in einen anderen verschieben können. E-Mail-Bereitstellung ist ein einfaches und effektives Mittel zum Verteilen von Formularen für innerbetrieblichen Gebrauch und zum Bereitstellen von Formularen für Remotebenutzer.
  
Sie können eine Formularvorlage digital signieren, zu entwerfen, und Sie die Sicherheitsstufe für diese Formularvorlage auf voll vertrauenswürdig legen. Darüber hinaus können signierte voll vertrauenswürdige Formulare, wenn sie als e-Mail-Anlage bereitgestellt werden einfacher und effizienter aktualisiert werden.
  
Alle Formulare im InfoPath-Designer werden mit der Identität erstellt. Mithilfe dieser Informationen können InfoPath-Formularvorlagen im Cache ordnen Sie Formulare und Abrufen von Updates für Formulare, wenn sie in einem freigegebenen Speicherort bereitgestellt werden. Standardmäßig erstellt InfoPath zwei Identitäten für Formularvorlagen: eine Formular-ID und ein Zugriffspfad (auch bekannt als das **PublishURL** -Attribut). Weitere Informationen zur e-Mail-Bereitstellung finden im Thema [Sicherheitsstufen, Bereitstellung, per E-Mail und Remoteformularvorlagen](security-levels-email-deployment-and-remote-form-templates.md).
  
## <a name="activex-controls"></a>ActiveX-Steuerelemente

InfoPath unterstützt das hostende von ActiveX-Steuerelementen in Formularen, die in der InfoPath-Editor geöffnet werden. Die ActiveX-Steuerelemente können (mit einigen Einschränkungen) bereits vorhandene werden oder speziell für die Verwendung mit InfoPath geschrieben werden können. ActiveX-Steuerelemente, die in InfoPath-Formularen verwendet werden, werden nicht automatisch von Websites heruntergeladen. Stattdessen müssen CAB-Dateien für die ActiveX-Steuerelemente, die nicht bereits auf dem Computer des Benutzers vorhanden sind die Formularvorlagendatei hinzugefügt werden.
  
Wenn ein ActiveX-Steuerelement in einem Formular verwendet wird und das Steuerelement nicht auf dem Computer des Benutzers registriert ist, hängt das Verhalten beim Öffnen des Formulars von den Einstellungen des ActiveX-Steuerelements innerhalb des Formulars ab. Das Formular wird von InfoPath nicht geöffnet, falls in der Formularvorlagendatei keine CAB-Datei vorhanden ist. InfoPath startet einen Installationsvorgang, falls die CAB-Datei in der Formularvorlagendatei vorhanden ist. Die Datei muss signiert sein, und die Signatur muss von einem vertrauenswürdigen Herausgeber stammen, damit eine CAB-Datei von InfoPath installiert wird. Wenn der Herausgeber noch nicht in der Liste vertrauenswürdiger Herausgeber des Benutzers aufgeführt ist, für die ein Zertifikat vorhanden ist (mit einer Vertrauenskette zu einem vertrauenswürdigen Stammzertifikat), wird der Benutzer aufgefordert, die Vertrauensstellung für den Herausgeber anzunehmen oder abzulehnen. Vertraut der Benutzer dem Herausgeber nicht, wird die CAB-Datei für das Steuerelement nicht installiert, und das Formular wird nicht von InfoPath geöffnet.
  
> [!NOTE]
> ActiveX-Steuerelemente müssen als Safe for scripting und Safe for initialization with untrusted data markiert sein, um in InfoPath verwendet zu werden. 
  
## <a name="net-security"></a>.NET-Sicherheit

Neben InfoPath-spezifischen Sicherheitsstufen werden von Formularvorlagen mit verwaltetem Code zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von Microsoft .NET Framework ausgeführt wird.
  
Wenn Ihr Formular voll vertrauenswürdig ist, kann damit automatisch auf Ressourcen außerhalb der Formularvorlage zugegriffen werden. Jede Assembly kann im Geschäftslogikcode verwendet werden. Den Berechtigungssatz, der einer Formularvorlage mit verwaltetem Code hinzugefügt wird, können Sie mit dem Microsoft .NET Framework-Konfigurationstool oder dem Sicherheitsrichtlinientool für den Codezugriff (Caspol.exe) anpassen. InfoPath sucht nach einer vordefinierten Codegruppe und wendet den unter dieser Gruppe definierten Berechtigungssatz auf die Anwendungsdomäne (AppDomain) an, in der der verwaltete Code geladen wird und in der er ausgeführt wird. Benutzerdefinierte .NET-Sicherheitsrichtlinien müssen auf Clientcomputern bereitgestellt werden, auf denen die Formularvorlage mit verwaltetem Code ausgeführt wird.
  
Beachten Sie, dass von der .NET-Sicherheit der Berechtigungssatz Internet nur für verwalteten Code erteilt wird, der in Internet Explorer als vertrauenswürdige Sites ausgeführt wird. Deshalb werden Formulare mit verwaltetem Code von InfoPath nicht ausgeführt, wenn sie in einer vertrauenswürdigen Site veröffentlicht werden.
  
## <a name="merging-forms"></a>Zusammenführen von Formularen

Das Feature zum Zusammenführen von Formularen kann deaktiviert werden, um zu verhindern, dass Benutzer Daten aus mehreren Formularen in ein einziges Formular importieren.
  
Aktivieren oder deaktivieren das Kontrollkästchen **Zusammenführen von Formularen aktivieren** auf den Abschnitt **Erweitert** im Dialogfeld **Formularoptionen** , die auf der Registerkarte **Info** von der Microsoft Office Backstage ist, wenn Sie das Formular entwerfen mit Zusammenführen von Formularen . Wenn das Zusammenführen von Formularen deaktiviert ist, können Benutzer beim Ausfüllen eines Formulars nicht auf **Formulare zusammenführen** auf der Registerkarte **Freigeben** von der Microsoft Office Backstage klicken. 
  
## <a name="submitting-forms"></a>Senden von Formularen

Sie können das Feature zum Senden von Formularen deaktivieren, um Benutzer am Senden von Formularen zu hindern.
  
Sie aktivieren oder Deaktivieren des Sendens von Formularen mithilfe von im Dialogfeld **Optionen zu übermitteln** , die zur Verfügung steht, indem Sie **Optionen zum Absenden** auf der Registerkarte **Daten** im Menü im Entwurfsmodus. Beim Senden von Formularen deaktiviert ist, können Benutzer beim Ausfüllen eines Formulars nicht auf **Absenden** auf der Registerkarte **Start** klicken. 
  

