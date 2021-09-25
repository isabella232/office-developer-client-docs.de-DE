---
title: Sicherheitsstufen, E-Mail-Bereitstellung und Remote-Formularvorlagen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: Microsoft InfoPath unterstützt das Verschieben von Formularvorlagen von einem Speicherort an einen anderen, das Senden als Anlage an eine E-Mail-Nachricht und das Erstellen voll vertrauenswürdiger Formularvorlagen, die digital signiert oder installiert sind.
ms.openlocfilehash: 3980563547796ff22942fba7177e051221535199
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614598"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Sicherheitsstufen, E-Mail-Bereitstellung und Remote-Formularvorlagen

Microsoft InfoPath unterstützt das Verschieben von Formularvorlagen von einem Speicherort an einen anderen, das Senden als Anlage an eine E-Mail-Nachricht und das Erstellen voll vertrauenswürdiger Formularvorlagen, die digital signiert oder installiert sind.
  
## <a name="security-levels"></a>Sicherheitsebenen

Formularvorlagen können je nach Speicherort eine der folgenden drei Sicherheitsstufen aufweisen. Diese drei Sicherheitsstufen werden in den folgenden Abschnitten beschrieben.  
  
### <a name="restricted"></a>Restricted

Mit der Sicherheitsstufe Eingeschränkt ist keine Kommunikation außerhalb der Formularvorlage zulässig. Diese Sicherheitsstufe soll verhindern, dass gefährliche Formulare Daten von Ihrem Computer an gefährliche Angreifer übertragen. Bei der Ausführung in diesem Sicherheitsmodus sind die folgenden Features nicht funktionsfähig:
  
- HTML-Aufgabenbereiche  
- SharePoint-Abfrage
- SharePoint senden
- XML-Dateiabfrage
- Datenbankabfrage
- Datenbank senden
- Webdienstabfrage
- Webdienst senden
- Benutzerdefinierten Code senden
- Hostumgebung senden
- ActiveX-Steuerelemente
- Rollen
- SharePoint-Workflow
- Regeln zum Öffnen eines neuen Dokuments
- Verwalteter Code
- Externe Druckansicht
- Verknüpfte Bilder
    
### <a name="domain"></a>Domäne

Mit der Sicherheitsstufe Domäne wird ein Formular auf eine bestimmte Internetdomäne eingeschränkt, und dessen Berechtigungen werden auf die Internet Explorer-Einstellungen für die Sicherheitszone eingeschränkt, in der sich die Domäne befindet. Das Formular kann mit anderen Datenquellen innerhalb der eigenen Domäne kommunizieren. Das Abrufen von Daten aus anderen Domänen ist jedoch in der Regel nicht zulässig, außer die Sicherheitszone erlaubt die domänenübergreifende Kommunikation. Dies ist die zulässige Mindestsicherheitsstufe für browserkompatible Formularvorlagen.
  
### <a name="full-trust"></a>Voll vertrauenswürdig

Mit der Sicherheitsstufe "Voll vertrauenswürdig" können Sie ein Formular mit voller Vertrauenswürdigkeit auf dem Computer ausführen, auf dem das Formular verwendet wird. Diese Sicherheitsstufe kann nur verwendet werden, wenn Sie mit einem Formular arbeiten, das sich auf einem Server befindet, der mit einer Signatur signiert ist, die einem vertrauenswürdigen Stammherausgeber auf Ihrem Computer entspricht, oder indem Sie das Formular installieren. Beide Methoden erfordern das Festlegen des **requireFullTrust-Attributs** auf "ja". Mithilfe dieser Einstellung kann das Formular auf Objektmodellaufrufe wie das Speichern von Dateien zugreifen, und bestimmte Sicherheitsaufforderungen, die angezeigt werden, wenn Sie auf einer restriktiveren Sicherheitsebene ausgeführt werden, sind deaktiviert. 
  
> [!NOTE]
> Allen im InfoPath-Designer erstellten Formularen wird eine Sicherheitsstufe zugeordnet. Formulare werden von InfoPath mit der zugeordneten Sicherheitsstufe geöffnet. Das Formular wird nicht geöffnet, wenn die dem Formular zugeordnete Sicherheitsstufe höher als die für dieses Formular zulässige Sicherheitsstufe ist. 
  
Die Sicherheitsstufe Voll vertrauenswürdig kann nur für installierte oder signierte Formularvorlagen festgelegt werden. Andernfalls ist Domäne die maximal zulässige Vertrauensebene. Die Sicherheitsstufe wird von InfoPath nicht automatisch auf Voll vertrauenswürdig festgelegt.
  
Formularen werden basierend auf dem Speicherort, in dem das jeweilige Formular geöffnet wird, Sicherheitsstufen zugewiesen.
  
## <a name="trust-levels"></a>Vertrauensebenen

Die höchste Vertrauensebene, die einer Formularvorlage erteilt werden kann, wird wie in der folgenden Tabelle beschrieben durch den Geöffnet von-Speicherort und weiteren Überprüfungscode bestimmt. Bei den in der Tabelle aufgeführten Attributen (z. B. HTTP, UNC,  *requireFullTrust)* handelt es sich um Einträge, die verwendet werden, um die Vertrauensebene zu bestimmen, die einem Formular erteilt werden kann, und die auf Formulare angewendet werden, die im InfoPath-Client geöffnet werden. 
  
|Höchste erteilte Vertrauensebene|Voll vertrauenswürdig|Clientcomputer (mit eingeschränkter Sicherheitsstufe)|Intranet (mit eingeschränkter Sicherheitsstufe)|Internet (mit eingeschränkter Sicherheitsstufe)|Restricted|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**Datei: Zugriffspfad=Geöffnet von-Speicherort** <br/> |||X  <br/> |||
|**Datei: Vom Speicherort geöffneter Zugriffspfad \<\> oder kein Zugriffspfad (unabhängig davon, woher das Formular stammt)** <br/> |||||X  <br/> |
|**Geöffnet von-Speicherort: Intranet-HTTP oder -HTTPS** <br/> |||X  <br/> |||
|**Geöffnet von-Speicherort: Internet-HTTP oder -HTTPS** <br/> ||||X  <br/> ||
|**Geöffnet von-Speicherort: UNC** <br/> |||X  <br/> |||
|**Installierte Vorlage (requireFullTrust="yes")** <br/> |X  <br/> |||||
|**Installierte Vorlage (requireFullTrust="no")** <br/> ||X  <br/> ||||
|**Vorlage mit vertrauenswürdigem Herausgeberzertifikat** <br/> |X  <br/> |||||
|**Exportierte Formulardateien** <br/> |||X  <br/> |||
   
## <a name="form-open-behavior"></a>Verhalten beim Öffnen von Formularen

Für alle im InfoPath-Editor geöffnete Formulardateien gelten Bedingungen, die bestimmen, mit welcher Sicherheitsstufe das Formular geöffnet wird und ob es geöffnet wird. Wenn ein InfoPath-Formular im Editor geöffnet wird, wird es entweder mit einer entsprechenden Sicherheitsstufe geöffnet oder es wird nicht geladen. Falls ein Formular eine höhere Sicherheitsstufe erfordert, als für das Formular zulässig ist (ein Formular kann mit dem Attribut **trustLevel** oder **requireFullTrust** eine bestimmte Sicherheitsstufe erfordern), kann es nicht geladen werden. Andernfalls wird das Formular mit der angeforderten Sicherheitsstufe geladen. Falls die Formularvorlage nicht mit der angeforderten Sicherheitsstufe geöffnet werden kann, kann der Benutzer das Formular nicht öffnen, und es wird eine entsprechende Fehlermeldung angezeigt. 
  
In der folgenden Tabelle werden die Bedingungen, die zum Öffnen eines Formulars auf den verschiedenen Sicherheitsstufen erforderlich sind, sowie das Verhalten beim Öffnen des Formulars beschrieben.
  
|Editor wird geöffnet/meldet einen Fehler|Voll vertrauenswürdig (requireFullTrust="yes")|Domänenvertrauensstellung (trustLevel="Domain" oder leer)|Eingeschränkt (trustLevel="Restricted")|
|:-----|:-----|:-----|:-----|
|**Vertrauenswürdig (installiertes oder vertrauenswürdiges Zertifikat)** <br/> |Editor wird mit der Sicherheitsstufe "Voll vertrauenswürdig" geöffnet  <br/> |Nicht zutreffend  <br/> |Nicht zutreffend  <br/> |
|**Domänenvertrauensstellung: Clientcomputer** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird auf Domänenebene geöffnet  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Domänenvertrauensstellung: Intranet** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird auf Domänenebene geöffnet  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Domänenvertrauensstellung: Internet** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird auf Domänenebene geöffnet  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Restricted** <br/> |Kann nicht geöffnet werden  <br/> |Kann nicht geöffnet werden  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
   
## <a name="specifying-a-security-level"></a>Angeben einer Sicherheitsstufe

Die entsprechende Sicherheitsstufe (Eingeschränkt oder Domäne) wird vom InfoPath-Formular-Designer anhand der von Ihnen im Formular verwendeten Features automatisch ausgewählt. Die Sicherheitseinstellung ist immer so restriktiv wie möglich, beginnend bei Eingeschränkt, um einen umfangreicheren Schutz für Sie und Ihre Daten sicherzustellen. Die Benutzer können diese automatische Einstellung manuell überschreiben, um eine für das Formular besser geeignete Sicherheitsstufe auszuwählen, indem sie die folgenden Schritte ausführen:
  
1. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
2. Klicken Sie in der Liste **Kategorien** auf **Sicherheit und Vertrauensstellung**.
    
3. Deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln (empfohlen)**. 
    
4. Wählen Sie die gewünschte Sicherheitsstufe aus.
    
## <a name="mail-deployment-and-browser-enabled-form-templates"></a>E-Mail-Bereitstellung und browserfähige Formularvorlagen

Mit InfoPath können Sie Ihre Formularvorlagen als Anlage an eine E-Mail-Nachricht senden und von einem Speicherort an einen anderen verschieben. Die Bereitstellung per E-Mail ist eine einfache und effektive Methode zum Verteilen von Formularen für die firmeninterne Verwendung und zum Bereitstellen von Formularen für Remotebenutzer.
  
Wenn Sie Microsoft SharePoint Server 2010 mit InfoPath Forms Services verfügbar haben, können Sie alternativ Formularvorlagen erstellen, mit denen Benutzer, die InfoPath nicht installiert haben, Formulare in einem Webbrowser ausfüllen können.
  
## <a name="understanding-form-identity"></a>Grundlegendes zur Formularidentität

Alle Formulare im InfoPath-Designer werden mit einer Identität erstellt. Mithilfe dieser Identitätsinformation kann InfoPath Formularen Formularvorlagen im Cache zuordnen und Aktualisierungen für Formulare abrufen, wenn diese in einem freigegebenen Speicherort verfügbar gemacht werden. Standardmäßig werden von InfoPath zwei Identitäten für Formularvorlagen erstellt: eine Formular-ID und ein Zugriffspfad.  
  
### <a name="form-id"></a>Formular-ID

Die Formular-ID ist eine eindeutige ID basierend auf einem Präfix, dem Formularnamen und dem Formularnamespace. Diese ID sollte ein eindeutiger Name sein, mit dem Formulardateien die zugehörige Formularvorlage im Clientcomputercache ordnungsgemäß zugeordnet werden kann. Die Formular-ID wird als Namensattribut (z.  `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"` B. ) in der Formulardefinitionsdatei (XSF) angegeben. 
  
### <a name="access-path"></a>Zugriffspfad

Der Zugriffspfad ist eine Speicherort-ID, mit der der entsprechende Speicherort für die Formularvorlage sowie der Speicherort für Aktualisierungen bestimmt wird. Beim Speichern oder Veröffentlichen der Formularvorlage wird der Pfad, in dem diese gespeichert oder veröffentlicht wird, zum Standardzugriffspfad. Jedes Mal, wenn ein Formular auf dem Clientcomputer geöffnet wird, wird versucht, das Formular einem zwischengespeicherten Formular zuzuordnen. Dabei wird in der folgenden Reihenfolge vorgegangen:
  
1. Suchen nach einer voll vertrauenswürdigen Formularvorlage mit einer passenden Formular-ID.
    
2. Suchen nach einer Formularvorlage im Cache mit einem passenden Zugriffspfad.
    
3. Suchen nach einer Formularvorlage im Cache mit einer passenden Formular-ID.
    
Nach der Übereinstimmung wird das Formular mit der zugeordneten Formularvorlage geöffnet. In Fällen, in denen die Übereinstimmung mit einem Zugriffspfad vorgenommen wurde, verwendet InfoPath den Zugriffspfad, um Aktualisierungen der Formularvorlage abzurufen. Diese Methode vereinfacht die Verwaltung, Wartung und Aktualisierung von Formularen im Unternehmen. In Fällen, in denen die Übereinstimmung nicht vorgenommen werden kann und die Vertrauensebene "Domäne" lautet, wird das Formular nicht geöffnet. Der Zugriffspfad wird als **publishUrl-Attribut** in der Formulardefinitionsdatei (XSF) angegeben. 
  
So wie es für jede Formularvorlage zwei Identifikationseigenschaften gibt, gibt es eine Reihe heuristischer Elemente, um die resultierenden Einträge im Cache basierend auf dem Status der Formularvorlage (ob ein Zugriffspfad und/oder eine Formular-ID vorhanden ist) und dem Status der Netzwerkverbindung zu bestimmen.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Entwerfen eines Formulars zum Senden als Anlage an eine E-Mail-Nachricht

Alle Formulare, die im InfoPath-Designer erstellt werden, können als Anlage zu einer E-Mail-Nachricht an Benutzer gesendet werden. Die E-Mail-Bereitstellung ist eine einfache und effektive Methode zum Verteilen von Formularen für die interne Verwendung sowie zum Bereitstellen von Formularen für Remotebenutzer.
  
### <a name="to-mail-a-form-template-to-other-users"></a>So senden Sie eine Formularvorlage per E-Mail an andere Benutzer

1. Klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf **"Veröffentlichen"** und dann auf die Schaltfläche **"E-Mail".** 
    
2. Füllen Sie die nächsten beiden Seiten des **Veröffentlichungs-Assistenten** aus und klicken Sie auf **"Weiter",** um nach jeder Seite fortzufahren, und klicken Sie dann auf **"Veröffentlichen".**
    
3. Es wird eine E-Mail-Nachricht angezeigt, mit der Sie die Liste der Empfänger und alle zusätzlichen Anweisungen, die Sie möglicherweise für sie haben, ausfüllen können.
    
4. Wenn Sie alle Informationen eingegeben haben, klicken Sie auf **Senden**. Das Formular und die Formularvorlage werden an die Nachricht angefügt.
    
## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>E-Mail-Bereitstellung: Eingeschränkte Formularvorlagen, Domänenvorlagen und Voll vertrauenswürdige Formularvorlagen

Die E-Mail-Bereitstellung von eingeschränkten Formularvorlagen ermöglicht das Öffnen dynamischer Formulare ohne Datenverbindungen von überall aus. Empfänger können Formularvorlagen, die als E-Mail-Anlagen gesendet werden, entweder direkt von Microsoft Outlook 2010 oder von überall dort öffnen, wo der Empfänger die Anlage gespeichert hat. Darüber hinaus können Benutzer mit Outlook 2010 Formulare direkt in der Nachricht bearbeiten.
  
Formularvorlagen mit der Domänenvertrauensstufe müssen von ihrem veröffentlichten Speicherort aus geöffnet werden, aber durch veröffentlichen in einer Liste von E-Mail-Empfängern im Veröffentlichungs-Assistenten können sie als Anlage an eine E-Mail-Nachricht gesendet werden. Wenn die Anlage geöffnet wird, fungiert sie als Link zum tatsächlichen veröffentlichten Speicherort der Vorlage. Die Formularvorlage an diesem Speicherort wird tatsächlich im InfoPath-Editor geöffnet.
  
Die Verwendung einer Formularvorlage auf Domänenebene, die als E-Mail-Anlage gesendet wird, ähnelt der Verwendung anderer Dokumentarten. Beispielsweise eine Microsoft Excel Arbeitsmappe oder ein Microsoft Word Dokument. Der Benutzer kann einfach auf das Formular klicken, um es zu öffnen und zu verwenden. Darüber hinaus können die Benutzer alle Vorteile von Aktualisierungen auf Domänenebene nutzen.
  
Sie können Formularvorlagen per E-Mail senden, die den Voll vertrauenswürdigen Zugriff anfordern, aber diese Vorlagen müssen signiert sein, oder sie dürfen nicht geöffnet werden. Formularvorlagen, die den Domänen- oder eingeschränkten Zugriff anfordern, müssen nicht signiert werden, um als E-Mail-Anlage gesendet zu werden. InfoPath überprüft oder überprüft die Signatur nicht, auch wenn die Vorlage signiert ist, außer um zu sehen, ob sie automatisch aktualisiert werden kann. Sie können eine Formularvorlage "Domäne" oder "Eingeschränkt" digital signieren und verfügen trotzdem über eine automatische Updatefunktion. In diesem Fall verhindert die digitale Signatur, dass Cachekonfliktnachrichten angezeigt werden.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Freigeben von Formularen nach E-Mail-Nachricht oder von einem gemeinsamen freigegebenen Speicherort

Beim Erstellen eines Formulars, das per E-Mail bereitgestellt wird, sollten bestimmte Fragen berücksichtigt werden.
  
- **Wird das Formular regelmäßig aktualisiert?** Wenn Sie ein Formular entwerfen, das regelmäßig aktualisiert werden muss, sollte das Formular in einem freigegebenen Speicherort veröffentlicht werden, bevor es an andere Benutzer gesendet wird. Auf diese Weise können Sie das Formular aktualisieren, indem Sie neuere Versionen in dem freigegebenen Speicherort veröffentlichen. Sie können aber auch die Formularvorlage sofort an Benutzer verteilen, die möglicherweise keinen Zugriff auf den freigegebenen Speicherort haben. 
    
   Wenn ein Formular aktualisiert und dann per E-Mail verteilt wird, erhalten Benutzer beim Versuch, das neue Formular zu öffnen, eine Cachekonfliktnachricht, wenn sie eine ältere Version auf ihrem Computer gespeichert haben und sich der Zugriffspfad geändert hat. Der Benutzer wird aufgefordert, die gewünschte Version auszuwählen. Selbst wenn das aktualisierte Formular mit dem Formular auf dem Computer des Benutzers identisch ist, wird eine Cachekonfliktmeldung angezeigt, und der Benutzer wird aufgefordert, die gewünschte Version auszuwählen. Im letzteren Fall empfiehlt es sich, das Formular stattdessen von einem freigegebenen Speicherort aus zu verwenden.
    
- **Greift Ihr Formular auf eine Datenverbindung zu oder verwendet es andere Features, die auf der Sicherheitsstufe "Eingeschränkt" nicht unterstützt werden?** Wenn Sie ein Formular entwickeln, das Sicherheit auf Domänenebene erfordert, müssen Sie das Formular in InfoPath an einem freigegebenen Speicherort veröffentlichen, damit Benutzer es öffnen können. Da Formularvorlagen nur auf der von ihnen angeforderten Sicherheitsstufe geöffnet werden, werden Formulare, die direkt aus einer E-Mail-Nachricht geöffnet werden, nicht geöffnet, wenn InfoPath keine Sicherheit auf Domänenebene gewähren kann. 
    
## <a name="benefits-of-using-signed-form-templates"></a>Vorteile der Verwendung signierter Formularvorlagen

- Die Formularvorlage kann mit der Sicherheitsstufe Voll vertrauenswürdig geöffnet werden.
    
- Die Cachekonfliktmeldung wird vermieden, wenn das Formular in einen neuen Speicherort verschoben wird.
    
Eine signierte Formularvorlage bietet außerdem den Vorteil der automatischen Aktualisierungsfunktion. Weitere Informationen finden Sie unter [Bereitstellen signierter InfoPath-Formularvorlagen.](deploying-signed-infopath-form-templates.md)
  
### <a name="example-updating-domain-or-restricted-templates"></a>Beispiel: Aktualisieren von Domänen- oder eingeschränkten Vorlagen

Das folgende Beispiel zeigt, wie eine aktualisierte, signierte Formularvorlage, die entweder "Domäne" oder "Eingeschränkter Zugriff" anfordert, eine ältere Kopie überschreiben kann: 
  
1. "A" sendet eine signierte Formularvorlage an "B".
    
2. "B" öffnet die Formularvorlage.
    
3. "A" aktualisiert die Formularvorlage (fügt z. B. zusätzliche Felder hinzu).
    
4. "A" sendet die aktualisierte Formularvorlage an "B".
    
5. "B" öffnet die aktualisierte Formularvorlage.
    
### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Beispiel: Bereitstellen eingeschränkter Formularvorlagen in einem Extranet
  
1. Speichern Sie die Formularvorlage "Domäne" auf einer Website, auf der Microsoft SharePoint Foundation 2010 ausgeführt wird.
    
2. Ändern Sie die Sicherheitsstufe der Formularvorlage in Eingeschränkt.
    
3. Speichern Sie die Formularvorlage auf dem Computerdesktop.
    
4. Entfernen Sie die URL (nur erforderlich, wenn die Benutzer Zugriff auf den ursprünglichen Veröffentlichungsspeicherort haben).
    
5. Senden Sie das Formular an Benutzer in einem Extranet.
    
6. Fordern Sie die Benutzer auf, das Formular zu installieren.
    
7. Fordern Sie die Benutzer auf, das ausgefüllte Formular an Sie zurückzusenden.
    
8. Speichern Sie das Formular wieder auf der Website, auf der SharePoint Foundation 2010 ausgeführt wird, und verknüpfen Sie das Formular erneut, indem Sie die Option **"Dokumente mit dieser Bibliothek** erneut verknüpfen" auf der Seite **"Formularbibliothek Einstellungen"** verwenden. 
    
## <a name="signature-verification-failure"></a>Signaturüberprüfungsfehler

Eine signierte Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, deren Signatur aber nicht authentifiziert werden kann, wird nicht geöffnet. Die Signaturüberprüfung kann augrund der folgenden Ursachen fehlschlagen:
  
- Das Stammzertifikat befindet sich nicht im Speicher für vertrauenswürdige Stammzertifikate.
    
- Das zum Signieren der Formularvorlage verwendete Zertifikat ist abgelaufen.
    
- Das zum Signieren der Formularvorlage verwendete Zertifikat wurde widerrufen.
    
- Die Signatur in der Formularvorlage ist fehlerhaft (ein Hinweis darauf, dass die Formularvorlage nach dem Signieren geändert wurde).
    
Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, wird die Signatur von InfoPath nicht überprüft. Es wird lediglich festgestellt, ob die Vorlage automatisch aktualisiert werden kann.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Infrastrukturregistrierungsschlüssel für das Öffnen von Formularmigrationsverhalten

Wenn ein Benutzer versucht, ein Formular zu öffnen, und das Formular anhand seiner Formular-ID mit einer Formularvorlage abgeglichen wird, zeigt InfoPath eine Fehlermeldung an, wenn die Formularvorlage über eine Domänenvertrauensstufe verfügt und die Domäne nicht mit dem  *href-Attribut*  des Formulars übereinstimmt. Dadurch wird verhindert, dass Formulare geöffnet werden, die nicht explizit mithilfe der Formularvorlage erstellt wurden. 
  
In InfoPath ist die Koexistenz von Formularvorlagen mit der gleichen Formular-ID nicht zulässig. Mithilfe von vier zusätzlichen Registrierungsschlüsseln bieten Systemadministratoren den Benutzern die Möglichkeit, das Öffnen der XML-Datei für eine Formularvorlage zuzulassen. Hiermit können die Administratoren für Formulare auch das gewünschte Verhalten beim Öffnen festlegen.
  
In der folgenden Tabelle werden die Standardeinstellungen für die Registrierungsschlüssel beschrieben. Falls diese Registrierungsschlüssel fehlen, wird der in der Tabelle angegebene Standardwert verwendet.
  
Die Namenswerte entsprechen den Domäneneinstellungen von Internet Explorer. Dieser Werte bestimmen das Verhalten beim Öffnen eines Formulars in diesen Sicherheitszonen, indem das Öffnen des Formulars zugelassen bzw. blockiert wird oder indem die Benutzer die Möglichkeit erhalten, das Formular zu öffnen.
  
|**Name-Wert**|**Blockieren**|**User Interface**|**Zulassen**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Clientcomputer** <br/> |||X  <br/> |
|**Vertrauenswürdige Site** <br/> |||X  <br/> |
   
Der Registrierungsschlüsselpfad lautet `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors` .

Das Verhalten beim Öffnen eines Formulars wird wie folgt definiert:
  
- `Block [REG_DWORD = 0]`– Es wird ein Fehlerdialogfeld mit einer Hilfeschaltfläche angezeigt. InfoPath lässt nicht zu, dass die XML-Datei geöffnet wird, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und nicht mit der Vorlagendomäne übereinstimmt. 
    
- `User Interface [REG_DWORD = 1]`- Das Dialogfeld Ja/Nein wird angezeigt. InfoPath fordert den Benutzer auf, die XML-Datei für die Formularvorlage zu öffnen, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und nicht mit der Vorlagendomäne übereinstimmt. 
    
- `Allow [REG_DWORD = 2]`– Die XML-Datei wird ohne Fehler- oder Warnungsdialogfeld geöffnet. Die XML-Datei kann geöffnet werden, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und nicht mit der Domäne der Vorlage übereinstimmt. 
    
Wenn ein Formular für eine Formularvorlage geöffnet wird, die auf der Domänensicherheitsstufe ausgeführt wird, und die Sicherheitsdomäne des Speicherorts "zwischengespeichert von" der Vorlage (d. h. von wo das Formular zwischengespeichert wird) und das **href-Attribut** des Formulars nicht übereinstimmen, überprüft InfoPath die Registrierung, um das Verhalten beim Öffnen des Formulars zu definieren. Das zulässige Verhalten basiert auf der Sicherheitszone, in der sich die Vorlage befindet (der *CachedFromLocation-Wert).* 
  
Wenn z. B. ein Formular mit einer Formularvorlage bezüglich der Formular-ID, aber nicht bezüglich des Zugriffspfads übereinstimmt, und die Formularvorlage aus einem Internetspeicherort zwischengespeichert wird, zeigt InfoPath ein Fehlerdialogfeld mit einer Schaltfläche Hilfe an.
  
> [!NOTE]
> InfoPath-Formulare werden nicht geöffnet, wenn es sich bei der Domäne um eine eingeschränkte Internet Explorer-Domäne handelt. Deshalb gibt es keinen Registrierungsschlüssel für eingeschränkte Sites in Internet Explorer. 
  

