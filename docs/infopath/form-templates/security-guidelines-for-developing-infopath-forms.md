---
title: Sicherheitsrichtlinien für die Entwicklung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Bevor Sie dieses Thema lesen, finden Sie unter "Zusätzliche InfoPath-Formularsicherheitskonzepte" ein allgemeines Verständnis des InfoPath-Sicherheitsmodells.
ms.openlocfilehash: 4e1d42fcc47d58b540bff752e183830dcd4f022d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557400"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Sicherheitsrichtlinien für die Entwicklung von InfoPath-Formularen

Bevor Sie dieses Thema lesen, finden Sie [unter "Zusätzliche InfoPath-Formularsicherheitskonzepte"](additional-infopath-form-security-concepts.md) ein allgemeines Verständnis des InfoPath-Sicherheitsmodells. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Sicherheitsaspekte für Benutzer von InfoPath-Formularen

Die wichtigsten Sicherheitsbedenken für Benutzer von Microsoft InfoPath ähneln denen für Webanwendungen, die in Internet Explorer ausgeführt werden. Sie sollten jedoch beachten, dass die Sicherheitsstufe für eine Formular nur vom Speicherort der Formularvorlage abhängt, und nicht davon, wo Benutzer die resultierenden erstellten XML-Dokumente speichern oder öffnen. Die Benutzer können den Speicherort der verwendeten Formularvorlage mithilfe der Statusleiste in InfoPath bestimmen.
  
InfoPath schützt die Benutzer vor den folgenden potenziellen Bedrohungen durch von böswilligen Benutzern erstellte Formularvorlagen:
  
- Dem Potenzial für die Weitergabe vertraulicher Informationen vom lokalen Computer oder von Remotedatenquellen.
    
- Der Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten.
    
- Der Verwendung von Eigenschaften und Methoden aus dem InfoPath-Objektmodell mit böswilligen Absichten.
    
## <a name="disclosure-of-sensitive-information"></a>Weitergabe vertraulicher Informationen

Das gängigste Szenario für die Weitergabe vertraulicher Informationen ist denkbar, wenn ein Formularautor mit böswilligen Absichten ein Formular erstellt, das mithilfe der Sicherheitsanmeldeinformationen des aktuellen Benutzers auf eine Datenquelle in einer anderen als der Domäne zugreift, in der das Formular selbst bereitgestellt wurde. Beispielsweise könnte ein böswilliger Benutzer ein Formular per E-Mail oder mithilfe einer URL zu einem Formular auf einer privaten Freigabe oder einem Webserver senden. Das Formular könnte ein Skript enthalten, das mithilfe der Anmeldeinformationen des aktuellen Benutzers eine Datenzugriffsanforderung ausführt, um Daten von einer Datenquelle in einer anderen Domäne abzurufen, auf die der böswillige Benutzer andernfalls keinen Zugriff hätte (z. B. eine Datenbank mit Lohnbuchhaltungsinformationen oder anderen vertraulichen Informationen). Diese Arte von Sicherheitsrisiko wird als domänenübergreifender Datenzugriff bezeichnet.
  
Das Sicherheitsmodell von Internet Explorer, auf dem InfoPath basiert, enthält die Einstellung **Auf Datenquellen über Domänengrenzen hinweg zugreifen**. Standardmäßig wird mit dieser Einstellung der domänenübergreifende Zugriff für InfoPath-Formulare in den Sicherheitszonen **Internet** und **Eingeschränkte Sites** deaktiviert. Der Benutzer wird außerdem gefragt, ob der domänenübergreifende Zugriff für InfoPath-Formulare in der Sicherheitszone **Lokales Intranet** zugelassen werden soll, und der domänenübergreifende Zugriff für InfoPath-Formulare in den Zonen **Vertrauenswürdige Sites** oder **Lokaler Computer** wird aktiviert. 
  
## <a name="malicious-use-of-activex-controls"></a>Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten

Das gängigste Szenario für die Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten ist denkbar, wenn ein böswilliger Formularautor Code für ein ActiveX-Steuerelement schreibt, der auf das Dateisystem zugreift, um persönliche Dateien und Kennwortlisten abzurufen, Dateien zu löschen oder das System des Benutzers zu deaktivieren. Ein InfoPath-Formular kann Code für ActiveX-Steuerelemente nur in Geschäftslogik oder in einem Skript in einem Aufgabenbereich ausführen. In InfoPath dürfen mit einem Skript in InfoPath-Ansichten keine ActiveX-Steuerelemente ausgeführt werden.
  
Das Sicherheitsmodell von Internet Explorer, auf dem Microsoft InfoPath basiert, enthält die Einstellung **ActiveX-Steuerelemente initialisieren und ausführen, die nicht sicher sind**. Mit dieser Einstellung wird standardmäßig das Initialisieren und Ausführen von ActiveX-Steuerelementen, die als nicht sicher markiert sind, für InfoPath-Formulare in den Sicherheitszonen **Lokales Intranet**, **Internet** und **Eingeschränkte Sites** deaktiviert. Der Benutzer wird gefragt, ob das Ausführen von ActiveX-Steuerelementen, die als nicht sicher markiert sind, für InfoPath-Formulare in den Sicherheitszonen **Vertrauenswürdige Sites** oder **Lokaler Computer** zulässig sein soll. Außerdem wird das Ausführen von ActiveX-Steuerelementen, die als nicht sicher markiert sind, für voll vertrauenswürdige InfoPath-Formulare aktiviert. 
  
Darüber hinaus können Sie im Designmodus kein ActiveX-Steuerelement, das zum Initialisieren und Ausführen als nicht sicher markiert ist, im Aufgabenbereich Steuerelemente hinzufügen, unabhängig von der aktiven Sicherheitszone oder der Vertrauensebene des Formulars.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Verwendung von InfoPath-Objektmodellcode mit böswilligen Absichten

Auf ähnliche Weise können in Code aufgerufene InfoPath-Methoden und -Eigenschaften unterschiedliche Risikostufen darstellen. Beispielsweise kann die [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)-Methode der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)-Klasse zum Schreiben von Daten an einer beliebigen Stelle im Dateisystem verwendet werden. Für den Schutz vor der Verwendung dieser Objektmodellmember mit böswilligen Absichten implementiert das InfoPath-Objektmodell drei Sicherheitsstufen, die bestimmen, wie und wo ein bestimmtes Objektmodellmember verwendet werden kann. Weitere Informationen zu diesem Feature finden Sie unter ["Informationen zum Sicherheitsmodell für Formularvorlagen mit Code".](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Bewährte Methoden für Entwickler von InfoPath-Formularen

Entwickler, die InfoPath-Formulare erstellen, sollten mit der Implementierung der folgenden bewährten Sicherheitsmethoden vertraut sein:
  
- Wie potenzielle Sicherheitsrisiken in der XML-Datei, die einem Formular zugeordnet ist, erkannt werden.
    
- Wie für Benutzer von Formularen die Anzeige verwirrender oder lästiger Fehlermeldungen vermieden wird.
    
- Wie die CAB-Dateien von ActiveX-Steuerelementen signiert werden.
    
- Signieren von Formularvorlagen, die als Anlage an eine E-Mail-Nachricht gesendet werden.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Bewährte Methoden für einem Formular zugeordnete XML-Daten

Beachten Sie, dass InfoPath-Formulare mit XML-Daten aus einer beliebigen Quelle aufgefüllt werden können, einschließlich Quellen, denen der Benutzer nicht notwendigerweise vertraut oder die er nicht notwendigerweise kontrolliert. Beispielsweise kann InfoPath XML-Daten aus einem Link zu einer Webseite oder aus einer XML-Anlage abrufen, die in einer E-Mail-Nachricht an den Benutzer gesendet wird. Beachten Sie die folgenden bewährten Methoden, um diese Risiken zu reduzieren:
  
- Übergeben Sie keine nicht vertrauenswürdigen Daten, die aus der XML-Datei gelesen wird, an die **eval()**-Funktion von Microsoft JScript oder an die **innerHTML**-Eigenschaft des Aufgabenbereichs. Mithilfe beider Aufrufe könnte ein böswilliges Skript ausgeführt werden. Verwenden Sie in einem Aufgabenbereich alternativ die **innerText**-Eigenschaft. Beachten Sie, dass in InfoPath-Ansichten kein Skript ausgeführt werden kann. 
    
- Aus einer XML-Datei an eine Datenbank gesendete Daten können Sicherheitsrisiken für die Datenbank darstellen, falls die Daten vor dem Senden nicht überprüft werden.
    
Daten, die vor dem Senden an eine Datenquelle nicht überprüft werden, können die Datenintegrität der Datenquelle beschädigen oder in extremeren Fällen Pufferüberläufe verursachen. Außerdem kann eine Skripteinschleusung oder eine Einschleusung von SQL-Befehlen ausgelöst werden, falls Sie versuchen, nicht vertrauenswürdige Daten direkt auf dem Server zu verwenden.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Bewährte Methoden zur Vermeidung der Anzeige verwirrender Fehlermeldungen

 **Stellen Sie Formulare und deren Datenquellen in derselben Domäne bereit**
  
Die meisten Benutzer verstehen das Sicherheitsrisiko des domänenübergreifenden Datenzugriffs nicht richtig. Die Bereitstellung von Formularen, mit denen die Benutzer ständig vor dem Zulassen des domänenübergreifenden Datenzugriffs gewarnt und aufgefordert werden, hat zur Folge, dass viele Benutzer alle domänenübergreifenden Zugriffsanforderungen genehmigen oder dass sie die Ausgangsdomäne der Liste **Vertrauenswürdige Sites** hinzufügen, ohne die damit verbundenen Sicherheitsrisiken ernst zu nehmen. Um diese Situation zu vermeiden, sollten Sie InfoPath-Formulare auf demselben Server wie die Datenquellen, von denen sie abhängen, bereitstellen. 
  
 **Vermeiden Sie die Verwendung von ActiveX-Steuerelementen, die als nicht sicher markiert sind**
  
Durch ActiveX-Steuerelemente können potenziell Eigenschaften und Methoden verfügbar gemacht werden, mit denen man sich den Zugang zum System eines Benutzers verschaffen kann, wie z. B. Methoden für den Zugriff auf das Dateisystem eines Computers. Sie sollten nach Möglichkeit nur ActiveX-Steuerelemente verwenden, die als sicher markiert sind. Hierbei handelt es sich um getestete Steuerelemente, die garantieren, dass das System eines Benutzers nicht beschädigt oder die Sicherheit des Benutzers nicht gefährdet wird, unabhängig davon, wie die Methoden und Eigenschaften des Steuerelements durch das Skript einer Webseite manipuliert werden. Beim Erstellen von ActiveX-Steuerelementen für die Verwendung mit InfoPath sollten Sie entsprechend den Code überprüfen und das ActiveX-Steuerelement gründlich testen, bevor Sie es als für die Ausführung sicher markieren.
  
InfoPath verwendet ein Sicherheitsmodell, das auf den Sicherheitszonen von Internet Explorer basiert. Deshalb verwendet ein InfoPath-Formular die gleichen Berechtigungen wie Internet Explorer, wodurch standardmäßig Skriptaufrufe für ActiveX-Steuerelemente, die als sicher markiert sind, ermöglicht werden, ohne dass die Benutzer aufgefordert werden.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Bewährte Methoden für die Verwaltung der CAB-Dateien von ActiveX-Steuerelementen

ActiveX-Steuerelemente können in Formularvorlagen gehostet werden, die für den InfoPath-Editor entworfen wurden. CAB-Dateien für diese Steuerelemente, die nicht bereits auf dem Computer des Benutzers vorhanden sind, müssen in der Formularvorlagendatei (XSN) enthalten sein. In Formularvorlagen enthaltene CAB-Dateien müssen digital signiert sein, damit die CAB-Dateien installiert werden. Eine nicht signierte CAB-Datei wird von InfoPath nicht installiert, und zwar unabhängig von der Vertrauensebene oder der Sicherheitszone.
  
Um sicherzustellen, dass die digitale Signatur in der CAB-Datei überprüft werden kann, sollte die Datei mit einem Zertifikat signiert werden, das eine Vertrauenskette zu einem bereits vertrauenswürdigen Stammzertifikat aufweist. Andernfalls kann die Signatur nicht authentifiziert werden, die Signaturüberprüfung schlägt fehl, und die CAB-Datei wird nicht installiert.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Bewährte Methoden für Formularvorlagen, die als Anlage an eine E-Mail-Nachricht gesendet werden

InfoPath unterstützt die Bereitstellung von Formularvorlagen als Anlage zu einer E-Mail-Nachricht und das Verschieben von Formularvorlagen von einem Speicherort an einen anderen. Es empfiehlt sich, eine Formularvorlage digital zu signieren, die Sie entwerfen und als Anlage an eine E-Mail-Nachricht bereitstellen möchten. Eine digitale Signatur in einer Formularvorlage, die per E-Mail bereitgestellt wird, stellt nicht nur die Authentizität der Vorlage sicher. Dies hat zusätzlich den Vorteil, dass die Formularvorlage automatisch aktualisiert werden kann.
  
Die Formularvorlage sollte mit einem Zertifikat signiert werden, das eine Vertrauenskette zu einem bereits vertrauenswürdigen Stammzertifikat aufweist. Andernfalls schlägt die Signaturüberprüfung fehl, da die Signatur nicht authentifiziert werden kann.
  
> [!NOTE]
> Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, wird die Signatur von InfoPath nicht überprüft. Es wird lediglich festgestellt, ob die Vorlage von InfoPath automatisch aktualisiert werden kann. 
  
Weitere Informationen zur E-Mail-Bereitstellung finden Sie unter ["Sicherheitsstufen", "E-Mail-Bereitstellung" und "Remoteformularvorlagen".](security-levels-email-deployment-and-remote-form-templates.md)
  

