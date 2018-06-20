---
title: Sicherheitsstufen, e-Mail-Bereitstellung und Remoteformularvorlagen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: Microsoft InfoPath unterstützt Verschieben von Formularvorlagen von einer Position an eine andere, sie als Anlage einer e-Mail-Nachricht gesendet werden und das Erstellen voll vertrauenswürdiger Formularvorlagen, die digital signiert oder installiert werden.
ms.openlocfilehash: ea0145eb45f6a03dc8637ba5ec1dc1c80d240006
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790838"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Sicherheitsstufen, e-Mail-Bereitstellung und Remoteformularvorlagen

Microsoft InfoPath unterstützt Verschieben von Formularvorlagen von einer Position an eine andere, sie als Anlage einer e-Mail-Nachricht gesendet werden und das Erstellen voll vertrauenswürdiger Formularvorlagen, die digital signiert oder installiert werden.
  
## <a name="security-levels"></a>Sicherheitsebenen

Formularvorlagen können je nach Speicherort eine der folgenden drei Sicherheitsstufen aufweisen. Diese drei Sicherheitsstufen werden in den folgenden Abschnitten beschrieben.  
  
### <a name="restricted"></a>Eingeschränkt

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

Die Sicherheitsstufe Voll vertrauenswürdig können Sie ein Formular mit voller Vertrauenswürdigkeit ausgeführt auf dem Computer, auf dem das Formular verwendet werden. Diese Sicherheitsstufe kann nur verwendet werden, bei der Arbeit mit einem Formular befindet sich auf einem Server, der mit einer Signatur, die mit einem vertrauenswürdigen Stammzertifizierungsstellen Herausgeber auf Ihrem Computer oder signiert ist durch Installieren des Formulars übereinstimmt. Beide Methoden ist erforderlich, wenn **RequireFullTrust** -Attribut auf "yes" festlegen. Mit dieser Einstellung Objektmodellaufrufe wie etwa-Datei speichern auf das Formular zugreifen kann, und bestimmte Sicherheitshinweise, die angezeigt werden, bei der Ausführung auf einem restriktiveren Sicherheitsstufe sind deaktiviert. 
  
> [!NOTE]
> Alle Formulare im InfoPath-Designer generiert haben eine Sicherheitsstufe zugeordnet. InfoPath wird Formulare auf der zugeordneten Sicherheitsstufe geöffnet. Wenn die dem Formular zugeordnete Sicherheitsstufe höher ist als die Sicherheitsstufe ist, die es gewährt werden können, wird das Formular nicht geöffnet. 
  
Die Sicherheitsstufe Voll vertrauenswürdig kann nur für installierte oder signierte Formularvorlagen festgelegt werden. Andernfalls ist Domäne die maximal zulässige Vertrauensebene. Die Sicherheitsstufe wird von InfoPath nicht automatisch auf Voll vertrauenswürdig festgelegt.
  
Formularen werden basierend auf dem Speicherort, in dem das jeweilige Formular geöffnet wird, Sicherheitsstufen zugewiesen.
  
## <a name="trust-levels"></a>Vertrauensebenen

Die höchste Stufe der Vertrauenswürdigkeit, die einer Formularvorlage gewährt werden können, wird durch die geöffnet von-Speicherort und andere Überprüfungscode bestimmt, wie in der folgenden Tabelle beschrieben. Die Attribute aufgeführt, die die Tabelle (beispielsweise HTTP, UNC, *RequireFullTrust*) Einträge, mit denen der Vertrauensebene zu ermitteln, die ein Formular erteilt werden können und anwenden auf Formulare im InfoPath-Client geöffnet sind. 
  
|Höchste erteilte Vertrauensebene |Voll vertrauenswürdig|Clientcomputer (mit eingeschränkter Sicherheitsstufe)|Intranet (mit eingeschränkter Sicherheitsstufe)|Internet (mit eingeschränkter Sicherheitsstufe)|Eingeschränkt|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**Datei: Zugriffspfad = geöffnet von-Speicherort** <br/> |||X  <br/> |||
|**Datei: Zugriffspfad\<\>geöffnet von-Speicherort oder kein Zugriffspfad (unabhängig davon, wo das Formular stammt)** <br/> |||||X  <br/> |
|**Geöffnet von-Speicherort: Intranet HTTP oder HTTPS** <br/> |||X  <br/> |||
|**Geöffnet von-Speicherort: Internet HTTP oder HTTPS** <br/> ||||X  <br/> ||
|**Geöffnet von-Speicherort: UNC** <br/> |||X  <br/> |||
|**Installierte Vorlage (RequireFullTrust = "yes")** <br/> |X  <br/> |||||
|**Installierte Vorlage (RequireFullTrust = "no")** <br/> ||X  <br/> ||||
|**Vorlage mit vertrauenswürdigem Herausgeberzertifikat** <br/> |X  <br/> |||||
|**Exportierte Formulardateien** <br/> |||X  <br/> |||
   
## <a name="form-open-behavior"></a>Verhalten beim Öffnen eines Formulars

Alle Formulardateien in InfoPath-Editor geöffnet werden durch eine Reihe von Bedingungen gebunden, mit die bestimmt die Sicherheitsstufe an dem das Formular geöffnet wird und ob es geöffnet wird. Wenn ein InfoPath-Formular im Editor geöffnet ist, werden entweder mit einer geeigneten Sicherheitsstufe geöffnet oder wird nicht geladen. Wenn ein Formular fordert eine höhere Sicherheitsstufe als gewährt werden kann (ein Formular kann anfordern eine bestimmten Sicherheitsstufe mithilfe des Attributs **TrustLevel** oder **RequireFullTrust** ), es kann nicht geladen werden. Andernfalls wird es mit der Sicherheitsstufe geladen im Zwischenspeicherbereich befinden. Wenn die Formularvorlage nicht zulässig ist, mit der angeforderten Sicherheitsstufe zu öffnen, wird der Benutzer werden nicht das Formular zu öffnen und erhält eine Fehlermeldung angezeigt. 
  
In der folgenden Tabelle werden die Bedingungen, die zum Öffnen eines Formulars auf den verschiedenen Sicherheitsstufen erforderlich sind, sowie das Verhalten beim Öffnen des Formulars beschrieben.
  
|Editor wird geöffnet/meldet einen Fehler|Voll vertrauenswürdig (requireFullTrust="yes")|Domänenvertrauensstellung (trustLevel="Domain" oder leer)|Eingeschränkt (trustLevel="Restricted")|
|:-----|:-----|:-----|:-----|
|**Vertrauenswürdig (installiertes oder vertrauenswürdiges Zertifikat)** <br/> |Editor wird mit der Sicherheitsstufe "Voll vertrauenswürdig" geöffnet  <br/> |N/v  <br/> |n/v  <br/> |
|**Domänenvertrauensstellung: Clientcomputer** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird geöffnet, auf Domänenebene  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Domänenvertrauensstellung: Intranet** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird geöffnet, auf Domänenebene  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Domänenvertrauensstellung: Internet** <br/> |Kann nicht geöffnet werden  <br/> |Editor wird geöffnet, auf Domänenebene  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
|**Restricted** <br/> |Kann nicht geöffnet werden  <br/> |Kann nicht geöffnet werden  <br/> |Editor wird mit der eingeschränkten Sicherheitsstufe geöffnet  <br/> |
   
## <a name="specifying-a-security-level"></a>Angeben einer Sicherheitsstufe

Die entsprechende Sicherheitsstufe (Eingeschränkt oder Domäne) wird vom InfoPath-Formular-Designer anhand der von Ihnen im Formular verwendeten Features automatisch ausgewählt. Die Sicherheitseinstellung ist immer so restriktiv wie möglich, beginnend bei Eingeschränkt, um einen umfangreicheren Schutz für Sie und Ihre Daten sicherzustellen. Die Benutzer können diese automatische Einstellung manuell überschreiben, um eine für das Formular besser geeignete Sicherheitsstufe auszuwählen, indem sie die folgenden Schritte ausführen:
  
1. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
2. Klicken Sie in der Liste **Kategorien** auf **Sicherheit und Vertrauensstellung**.
    
3. Deaktivieren Sie die **Sicherheitsstufe automatisch ermitteln (empfohlen)** das Kontrollkästchen. 
    
4. Wählen Sie die gewünschte Sicherheitsstufe aus.
    
## <a name="mail-deployment-and-browser-enabled-form-templates"></a>Bereitstellung per e-Mail und browserfähige Formularvorlagen

InfoPath können Sie Formularvorlagen als Anlage einer e-Mail-Nachricht senden und von einem Speicherort an einen anderen verschieben. E-Mail-Bereitstellung ist ein einfaches und effektives Mittel zum Verteilen von Formularen für innerbetrieblichen Gebrauch sowie zum Bereitstellen von Formularen für Remotebenutzer.
  
Wenn Sie Microsoft SharePoint Server 2010 mit InfoPath Forms Services zur Verfügung haben, können Sie alternativ Formularvorlagen erstellen, die Benutzern, die nicht installiert sind ermöglichen, die Formulare in einem Webbrowser ausfüllen InfoPath verfügen.
  
## <a name="understanding-form-identity"></a>Grundlegendes zur Formularidentität

Alle Formulare im InfoPath-Designer werden mit einer Identität erstellt. Mithilfe dieser Identitätsinformation kann InfoPath Formularen Formularvorlagen im Cache zuordnen und Aktualisierungen für Formulare abrufen, wenn diese in einem freigegebenen Speicherort verfügbar gemacht werden. Standardmäßig werden von InfoPath zwei Identitäten für Formularvorlagen erstellt: eine Formular-ID und ein Zugriffspfad.  
  
### <a name="form-id"></a>Formular-ID

Der Formular-ID ist eine eindeutige ID, die basierend auf einem Präfix, den Namen des Formulars und der Formularnamespace. Der Bezeichner sollte einen eindeutigen Namen, mit denen ordnungsgemäß Formulardateien der zugehörigen Formularvorlage im Cache Clientcomputers zugeordnet werden können. Der Formular-ID wird angegeben, wie das Namensattribut (z. B. `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"`) in der Formulardefinitionsdatei (XSF). 
  
### <a name="access-path"></a>Zugriffspfad

Der Zugriffspfad ist eine Speicherort-ID, mit der der entsprechende Speicherort für die Formularvorlage sowie der Speicherort für Aktualisierungen bestimmt wird. Beim Speichern oder Veröffentlichen der Formularvorlage wird der Pfad, in dem diese gespeichert oder veröffentlicht wird, zum Standardzugriffspfad. Jedes Mal, wenn ein Formular auf dem Clientcomputer geöffnet wird, wird versucht, das Formular einem zwischengespeicherten Formular zuzuordnen. Dabei wird in der folgenden Reihenfolge vorgegangen:
  
1. Suchen nach einer voll vertrauenswürdigen Formularvorlage mit einer passenden Formular-ID.
    
2. Suchen nach einer Formularvorlage im Cache mit einem passenden Zugriffspfad.
    
3. Suchen nach einer Formularvorlage im Cache mit einer passenden Formular-ID.
    
Nachdem übereinstimmt, wird das Formular mit der zugeordneten Formularvorlage geöffnet. In Fällen, in denen die Übereinstimmung mit einem Zugriffspfad hergestellt wurde, wird InfoPath Zugriffspfad verwenden, um Updates für die Formularvorlage abzurufen. Diese Methode vereinfacht die Verwaltung von Unternehmen, Wartung und Aktualisierung von Formularen. In Fällen, in dem die Übereinstimmung ist nicht möglich, und die Vertrauensebene Domäne ist wird das Formular nicht geöffnet. Der Zugriffspfad wird als **PublishUrl** -Attribut in der Formulardefinitionsdatei (XSF) angegeben. 
  
So wie es für jede Formularvorlage zwei Identifikationseigenschaften gibt, gibt es eine Reihe heuristischer Elemente, um die resultierenden Einträge im Cache basierend auf dem Status der Formularvorlage (ob ein Zugriffspfad und/oder eine Formular-ID vorhanden ist) und dem Status der Netzwerkverbindung zu bestimmen.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Entwerfen eines Formulars als Anlage einer e-Mail-Nachricht senden

Alle Formulare, die im InfoPath-Designer erstellt werden, können als Anlage einer e-Mail-Nachricht an Benutzer gesendet werden. E-Mail-Bereitstellung ist ein einfaches und effektives Mittel zum Verteilen von Formularen für innerbetrieblichen Gebrauch sowie zum Bereitstellen von Formularen für Remotebenutzer.
  
### <a name="to-mail-a-form-template-to-other-users"></a>So senden Sie eine Formularvorlage per E-Mail an andere Benutzer

1. Klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Veröffentlichen**, und klicken Sie dann auf die Schaltfläche **E-Mail** . 
    
2. Füllen Sie die nächsten beiden Seiten des **Veröffentlichungs-Assistenten** auf **Weiter** , um Seiten gelangen, und klicken Sie dann auf **Veröffentlichen**.
    
3. Eine e-Mail-Nachricht wird angezeigt, aktivieren Sie in der Liste der Empfänger und etwaige zusätzliche Anweisungen, die Sie möglicherweise für sie ausfüllen.
    
4. Wenn Sie fertig sind, klicken Sie auf **Senden**. Das Formular und die Formularvorlage werden an die Nachricht angefügt werden soll.
    
## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>E-Mail-Bereitstellung: eingeschränkt, Domäne und voll vertrauenswürdige Formularvorlagen

E-Mail-Bereitstellung von Formularvorlagen mit eingeschränkter ermöglicht die dynamische Formulare ohne datenverbindungen unabhängig vom Standort geöffnet werden soll. Empfänger können Formularvorlagen als e-Mail-Anlagen gesendet werden, entweder direkt aus Microsoft Outlook 2010 oder dorthin, wo der Empfänger die Anlage gespeichert haben, öffnen. Darüber hinaus erlaubt Outlook 2010 Benutzer Formulare direkt in der Nachricht zu bearbeiten.
  
Formularvorlagen mit der Vertrauensstufe Domäne müssen vom veröffentlichten Speicherort geöffnet werden, aber durch Veröffentlichung auf eine Liste von e-Mail-Empfängern im Veröffentlichen-Assistenten, können sie als Anlage einer e-Mail-Nachricht gesendet werden. Wenn die Anlage geöffnet wird, funktioniert es als einen Link zu den tatsächlichen veröffentlichten Speicherort der Vorlage. Die Formularvorlage an dieser Stelle ist, was tatsächlich in der InfoPath-Editor geöffnet ist.
  
Verwenden einer gesendeten, wie e-Mail-Anlage ähnelt mit einer anderen Art des Dokuments auf Domänenebene Formularvorlage; eine Microsoft Excel-Arbeitsmappe oder ein Microsoft Word-Dokument. Ein Benutzer kann nur klicken Sie auf Öffnen und verwenden sie das Formular. Darüber hinaus sind alle Vorteile des Updates auf Domänenebene für Benutzer verfügbar.
  
Senden Sie eine e-Mail-Formularvorlagen, die voll vertrauenswürdig Zugriff anfordern, aber diese Vorlagen müssen signiert sein oder sie kann nicht geöffnet. Formularvorlagen, die Domäne oder eingeschränkt erfordert Zugriff anfordern müssen nicht angemeldet sein, um als e-Mail-Anlage gesendet werden. InfoPath überprüfen oder die Signatur überprüfen, selbst wenn die Vorlage signiert ist, mit Ausnahme von an finden Sie unter, ob es automatisch aktualisiert werden kann, nicht. Digitales Signieren einer Formularvorlage Domäne oder eingeschränkt erfordert, und noch immer automatisch aktualisiert werden kann. In diesem Fall wird die digitale Signatur dennoch nicht angezeigt werden.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Freigeben von Formularen per e-Mail oder aus einem allgemeinen freigegebenen Speicherort

Bestimmte Fragen sollten berücksichtigt werden, wenn Sie ein Formular erstellen, die e-Mail-Nachricht bereitgestellt wird.
  
- **Wird das Formular regelmäßig werden aktualisiert?** Wenn Sie ein Formular entwickeln, das regelmäßig aktualisiert werden muss, sollte das Formular an einem freigegebenen Speicherort veröffentlicht werden, bevor sie an andere Benutzer gesendet wird. Diese Vorgehensweise können Sie das Formular durch veröffentlichen neuere Versionen zu dem freigegebenen Speicherort aktualisieren, aber auch die Möglichkeit, sofort die Formularvorlage an Benutzer verteilen, die nicht auf den freigegebenen Speicherort zugreifen können. 
    
   Wenn ein Formular aktualisiert und dann durch e-Mail-Nachricht verteilt, erhalten Benutzer Meldung zu einem Konflikt angezeigt, wenn sie versuchen, das das neue Formular zu öffnen, wenn sie eine ältere Version auf ihrem Computer gespeichert haben, und der Zugriffspfad geändert wurde. Der Benutzer aufgefordert werden, auswählen, welche Version sie verwenden möchten. Auch wenn das aktualisierte Formular auf dem Computer des Benutzers identisch ist, wird der Benutzer erhalten die Meldung zu einem Konflikt angezeigt und aufgefordert, welche Kopieren wählen sie verwenden möchten. Im letzteren Fall verwenden die bewährte Methode besteht darin, das Formular aus einem freigegebenen Speicherort stattdessen freizugeben.
    
- **Ihr Formular Zugriff auf eine Datenverbindung oder verwenden Sie andere Features, die nicht mit der eingeschränkten Sicherheitsstufe unterstützt?** Wenn Sie ein Formular, die Sicherheit auf Domänenebene erforderlich sind entwickeln, müssen InfoPath veröffentlichen Sie das Formular an einem freigegebenen Speicherort für Benutzer zu können, um ihn zu öffnen. Da Formularvorlagen nur mit der Sicherheitsstufe, den, die Sie anfordern geöffnet werden, werden direkt aus einer e-Mail-Nachricht geöffnete Formulare nicht geöffnet, wenn InfoPath auf Domänenebene Sicherheit erteilen kann nicht. 
    
## <a name="benefits-of-using-signed-form-templates"></a>Vorteile der Verwendung signierter Formularvorlagen

- Die Formularvorlage kann mit der Sicherheitsstufe Voll vertrauenswürdig geöffnet werden.
    
- Die Cachekonfliktmeldung wird vermieden, wenn das Formular in einen neuen Speicherort verschoben wird.
    
Wenn eine Formularvorlage signiert ist, erhalten Sie den Vorteil, die automatische Updatefunktion. Weitere Informationen finden Sie unter [Bereitstellen signierter InfoPath Formularvorlagen](deploying-signed-infopath-form-templates.md).
  
### <a name="example-updating-domain-or-restricted-templates"></a>Beispiel: Aktualisieren von Domänen oder eingeschränkten Vorlagen

Das folgende Beispiel zeigt, wie eine aktualisierten, signierten Formularvorlage Domäne oder eingeschränkt erfordert Zugriff anfordern eine ältere Kopie überschrieben werden kann: 
  
1. "A" sendet eine signierte Formularvorlage an "B".
    
2. "B" öffnet die Formularvorlage.
    
3. "A" aktualisiert die Formularvorlage (fügt z. B. zusätzliche Felder hinzu).
    
4. "A" sendet die aktualisierte Formularvorlage an "B".
    
5. "B" öffnet die aktualisierte Formularvorlage.
    
### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Beispiel: Bereitstellen von eingeschränkt Formularvorlagen in einem extranet
  
1. Speichern Sie die Domänenformularvorlage auf einer Website, auf dem Microsoft SharePoint Foundation 2010 ausgeführt wird.
    
2. Ändern Sie die Sicherheitsstufe der Formularvorlage in Eingeschränkt.
    
3. Speichern Sie die Formularvorlage auf dem Computerdesktop.
    
4. Entfernen Sie die URL (nur erforderlich, wenn die Benutzer Zugriff auf den ursprünglichen Veröffentlichungsspeicherort haben).
    
5. Senden Sie das Formular an Benutzer in einem Extranet.
    
6. Fordern Sie die Benutzer auf, das Formular zu installieren.
    
7. Fordern Sie die Benutzer auf, das ausgefüllte Formular an Sie zurückzusenden.
    
8. Speichern Sie das Formular wieder auf die Website, die SharePoint Foundation 2010 ausgeführt wird, und verknüpfen Sie das Formular mithilfe der Option **Dokumente in dieser Bibliothek erneut verknüpfen** auf der Seite **Form Library Settings** . 
    
## <a name="signature-verification-failure"></a>Fehler bei signaturüberprüfung

Eine signierte Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, deren Signatur aber nicht authentifiziert werden kann, wird nicht geöffnet. Die Signaturüberprüfung kann augrund der folgenden Ursachen fehlschlagen:
  
- Das Stammzertifikat befindet sich nicht im Speicher für vertrauenswürdige Stammzertifikate.
    
- Das zum Signieren der Formularvorlage verwendete Zertifikat ist abgelaufen.
    
- Das zum Signieren der Formularvorlage verwendete Zertifikat wurde widerrufen.
    
- Die Signatur in der Formularvorlage ist fehlerhaft (ein Hinweis darauf, dass die Formularvorlage nach dem Signieren geändert wurde).
    
Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, wird die Signatur von InfoPath nicht überprüft. Es wird lediglich festgestellt, ob die Vorlage automatisch aktualisiert werden kann.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Infrastrukturregistrierungsschlüssel für die Migration Formular das Verhalten beim Öffnen

Wenn ein Benutzer versucht, ein Formular zu öffnen, und das Formular mit einer Formularvorlage, der Formular-ID verglichen wird, zeigt InfoPath eine Fehlermeldung, wenn die Formularvorlage eine Vertrauensebene Domäne wurde und die Domäne nicht des *Href* -Attributs des Formulars entspricht. Dies verhindert, dass Formulare geöffnet werden, die mithilfe der Formularvorlage nicht explizit erstellt wurden. 
  
In InfoPath ist die Koexistenz von Formularvorlagen mit der gleichen Formular-ID nicht zulässig. Mithilfe von vier zusätzlichen Registrierungsschlüsseln bieten Systemadministratoren den Benutzern die Möglichkeit, das Öffnen der XML-Datei für eine Formularvorlage zuzulassen. Hiermit können die Administratoren für Formulare auch das gewünschte Verhalten beim Öffnen festlegen.
  
In der folgenden Tabelle werden die Standardeinstellungen für die Registrierungsschlüssel beschrieben. Falls diese Registrierungsschlüssel fehlen, wird der in der Tabelle angegebene Standardwert verwendet.
  
Die Namenswerte entsprechen den Domäneneinstellungen von Internet Explorer. Dieser Werte bestimmen das Verhalten beim Öffnen eines Formulars in diesen Sicherheitszonen, indem das Öffnen des Formulars zugelassen bzw. blockiert wird oder indem die Benutzer die Möglichkeit erhalten, das Formular zu öffnen.
  
|**Name-Wert**|**Blockieren**|**User Interface**|**Zulassen**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Clientcomputer** <br/> |||X  <br/> |
|**Vertrauenswürdige Site** <br/> |||X  <br/> |
   
Der Registrierungsschlüsselpfad lautet `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors`.

Das Verhalten beim Öffnen eines Formulars wird wie folgt definiert:
  
- `Block [REG_DWORD = 0]`-Ein Fehlerdialogfeld mit der Hilfeschaltfläche wird angezeigt. InfoPath kann nicht ansetzt, die XML-Datei zu öffnen, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und die Vorlagendomäne stimmt nicht überein. 
    
- `User Interface [REG_DWORD = 1]`-Ja/kein Dialogfeld wird angezeigt. InfoPath fordert den Benutzer, die XML-Datei mit der Formularvorlage öffnen, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und die Vorlagendomäne stimmt nicht überein. 
    
- `Allow [REG_DWORD = 2]`-Die XML-Datei wird ohne Fehler oder Warndialogfeld geöffnet. InfoPath ansetzt, kann die XML-Datei zu öffnen, wenn das Formular in der angegebenen Sicherheitszone ausgeführt wird und die Vorlagendomäne stimmt nicht überein. 
    
Wenn ein Formular geöffnet wird, mit einer Formularvorlage mit der Sicherheitsstufe Domäne ausgeführt, und die Sicherheitsdomäne, der der Vorlage "aus" Speicherort zwischengespeichert (d. h., in dem das Formular zwischengespeichert wird) und das Formular **Href** -Attribut nicht übereinstimmen, InfoPath überprüft, ob die Registrierung, um das Formular öffnen Verhalten zu definieren. Zulässige Verhalten basiert auf der Sicherheitszone in die Vorlage ist (den Wert *CachedFromLocation* ) befinden. 
  
Wenn z. B. ein Formular mit einer Formularvorlage bezüglich der Formular-ID, aber nicht bezüglich des Zugriffspfads übereinstimmt, und die Formularvorlage aus einem Internetspeicherort zwischengespeichert wird, zeigt InfoPath ein Fehlerdialogfeld mit einer Schaltfläche Hilfe an.
  
> [!NOTE]
> InfoPath-Formulare werden nicht geöffnet, wenn es sich bei der Domäne um eine eingeschränkte Internet Explorer-Domäne handelt. Deshalb gibt es keinen Registrierungsschlüssel für eingeschränkte Sites in Internet Explorer. 
  

