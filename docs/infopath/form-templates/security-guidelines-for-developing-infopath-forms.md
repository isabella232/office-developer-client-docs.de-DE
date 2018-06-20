---
title: Sicherheitsrichtlinien für die Entwicklung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Bevor Sie dieses Thema lesen, finden Sie unter Allgemeine Kenntnisse über das Sicherheitsmodell für InfoPath zusätzliche Sicherheitskonzepte für InfoPath-Formular.
ms.openlocfilehash: 3a72421882e655f34abd1eda30fe7e4fb42c45c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790851"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Sicherheitsrichtlinien für die Entwicklung von InfoPath-Formularen

Bevor Sie dieses Thema lesen, finden Sie unter Allgemeine Kenntnisse über das Sicherheitsmodell für InfoPath [Zusätzliche Sicherheitskonzepte für InfoPath-Formular](additional-infopath-form-security-concepts.md) . 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Sicherheitsaspekte für Benutzer von InfoPath-Formularen

Die wichtigsten Sicherheitsbedenken für Benutzer von Microsoft InfoPath ähneln jenen für Webanwendungen, die in Internet Explorer ausgeführt. Beachten Sie jedoch, dass die Sicherheitsebene eines Formulars nur davon, wo sich die Formularvorlage befindet abhängt und nicht auf, an dem Benutzer speichern, oder öffnen Sie die resultierende XML-Dokumente, die sie erstellen. Benutzer können den Speicherort der Formularvorlage bestimmen, mit der Sie arbeiten Sie anhand der Statusleiste in InfoPath.
  
InfoPath schützt die Benutzer vor den folgenden potenziellen Bedrohungen durch von böswilligen Benutzern erstellte Formularvorlagen:
  
- Dem Potenzial für die Weitergabe vertraulicher Informationen vom lokalen Computer oder von Remotedatenquellen.
    
- Der Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten.
    
- Der Verwendung von Eigenschaften und Methoden aus dem InfoPath-Objektmodell mit böswilligen Absichten.
    
## <a name="disclosure-of-sensitive-information"></a>Weitergabe vertraulicher Informationen

Das häufigste Szenario für die Offenlegung von vertraulichen Informationen kann auftreten, wenn ein Autor böswilligen Formulars ein Formular erstellt, die Anmeldeinformationen des aktuellen Benutzers verwendet, um eine Datenquelle in einer anderen als der Domäne zugreifen, auf dem das Formular selbst bereitgestellt wurde. Beispielsweise konnte ein böswilliger Benutzer ein Formular durch e-Mail-Nachricht oder mithilfe einer URL zu einem Formular auf einem privaten Freigabe oder Webserver senden. Das Formular konnte Skript enthalten, die eine Anforderung zum Zugriff von Daten mithilfe der Anmeldeinformationen des aktuellen Benutzers zum Abrufen von Daten aus einer Datenquelle in einer anderen Domäne, dass der böswillige Benutzer zugreifen kann, wie etwa eine Datenbank zu Lohn und Gehalt oder andere vertrauliche andernfalls nicht vorhanden wäre durchführt Informationen. Diese Klasse Sicherheitsrisiko wird als domänenübergreifender Datenzugriff bezeichnet.
  
Das Sicherheitsmodell für Internet Explorer, dem InfoPath basiert, bietet die eine Einstellung **auf Datenquellen über Domänengrenzen hinweg zugreifen** , die standardmäßig deaktiviert domänenübergreifenden Zugriff für InfoPath-Formulare, die sich im **Internet** und **eingeschränkt befinden Websites** Sicherheitszonen. Diese Einstellung auch fordert den Benutzer zulassen oder Verweigern des domänenübergreifenden Zugriffs für InfoPath-Formulare, die sich in der **lokalen** Intranetzone befinden und ermöglicht domänenübergreifenden Zugriff für InfoPath-Formulare, die sich in der **vertrauenswürdigen Sites** oder **lokalen befinden Computer** Zonen. 
  
## <a name="malicious-use-of-activex-controls"></a>Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten

Das gängigste Szenario für die Verwendung von ActiveX-Steuerelementen mit böswilligen Absichten ist denkbar, wenn ein böswilliger Formularautor Code für ein ActiveX-Steuerelement schreibt, der auf das Dateisystem zugreift, um persönliche Dateien und Kennwortlisten abzurufen, Dateien zu löschen oder das System des Benutzers zu deaktivieren. Ein InfoPath-Formular kann Code für ActiveX-Steuerelemente nur in Geschäftslogik oder in einem Skript in einem Aufgabenbereich ausführen. In InfoPath dürfen mit einem Skript in InfoPath-Ansichten keine ActiveX-Steuerelemente ausgeführt werden.
  
Das Sicherheitsmodell für Internet Explorer, dem InfoPath basiert bietet die Einstellung **als nicht sicher markiert ActiveX-Steuerelemente initialisieren und Ausführen**. Diese Einstellung wird standardmäßig deaktiviert, Initialisierung und scripting von ActiveX-Steuerelemente als unsicher für InfoPath-Formulare, die sich in den Sicherheitszonen **Lokales Intranet**, **Internet**und **Eingeschränkte Sites** befinden. Es fordert den Benutzer zulassen oder verweigern scripting von ActiveX-Steuerelemente als unsicher für InfoPath-Formulare, die sich in die **Vertrauenswürdige Sites** oder dem **Lokalen Computer** Sicherheitszonen befinden, und dadurch können ActiveX-Steuerelemente als unsicher für Skripts InfoPath-Formulare, die vollständig vertrauenswürdig sind. 
  
Darüber hinaus können Sie im Designmodus kein ActiveX-Steuerelement, das zum Initialisieren und Ausführen als nicht sicher markiert ist, im Aufgabenbereich Steuerelemente hinzufügen, unabhängig von der aktiven Sicherheitszone oder der Vertrauensebene des Formulars.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Verwendung von InfoPath-Objektmodellcode mit böswilligen Absichten

In ähnlicher Weise können InfoPath-Methoden und Eigenschaften, die aus Code aufgerufen verschiedene Risiko darstellen. Beispielsweise kann die [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) -Methode der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zum Schreiben von Daten an einer beliebigen Stelle im Dateisystem verwendet werden. Zum Schutz gegen die Verwendung dieser Objektmodellmitglieder implementiert das InfoPath-Objektmodell drei Sicherheitsstufen, die bestimmen, wie und wo ein bestimmtes Objektmodellelement verwendet werden kann. Weitere Informationen zu diesem Feature finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Bewährte Methoden für Entwickler von InfoPath-Formularen

Entwickler, die InfoPath-Formulare erstellen, sollten mit der Implementierung der folgenden bewährten Sicherheitsmethoden vertraut sein:
  
- Wie potenzielle Sicherheitsrisiken in der XML-Datei, die einem Formular zugeordnet ist, erkannt werden.
    
- Wie für Benutzer von Formularen die Anzeige verwirrender oder lästiger Fehlermeldungen vermieden wird.
    
- Wie die CAB-Dateien von ActiveX-Steuerelementen signiert werden.
    
- Wie als Anlage einer e-Mail-Nachricht gesendete Formularvorlagen signiert werden.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Bewährte Methoden für einem Formular zugeordnete XML-Daten

Beachten Sie, dass InfoPath-Formularen können XML-Daten aus einer Datenquelle verwendet werden, einschließlich derjenigen, die der Benutzer nicht notwendigerweise vertraut oder eines Steuerelements. Beispielsweise kann InfoPath XML-Daten über einen Link zu einer Webseite oder aus XML-Anlage an den Benutzer in e-Mail-Nachricht gesendet erhalten. Um diesen Risiken zu verringern, beachten Sie sollten die folgenden bewährten Methoden:
  
- Übergeben Sie nicht nicht vertrauenswürdige Daten, die an **die Eval()-Funktion Microsoft JScript** oder der **InnerHTML** -Eigenschaft des Aufgabenbereichs aus der XML-Code gelesen werden. Beide Aufrufe können verwendet werden, bösartige Skript ausgeführt. Verwenden Sie die **InnerText** -Eigenschaft in einem Aufgabenbereich als Alternative. Beachten Sie, dass das Skript nicht InfoPath-Ansichten ausgeführt werden können. 
    
- Aus einer XML-Datei an eine Datenbank gesendete Daten können Sicherheitsrisiken für die Datenbank darstellen, falls die Daten vor dem Senden nicht überprüft werden.
    
Daten, die vor dem Senden an eine Datenquelle nicht überprüft werden, können die Datenintegrität der Datenquelle beschädigen oder in extremeren Fällen Pufferüberläufe verursachen. Außerdem kann eine Skripteinschleusung oder eine Einschleusung von SQL-Befehlen ausgelöst werden, falls Sie versuchen, nicht vertrauenswürdige Daten direkt auf dem Server zu verwenden.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Bewährte Methoden zur Vermeidung der Anzeige verwirrender Fehlermeldungen

 **Bereitstellen von Formularen und deren Datenquellen in derselben Domäne**
  
Das Sicherheitsrisiko domänenübergreifenden Datenzugriff wird von den meisten Benutzern nicht klar verstanden. Bereitstellen von Formularen, die ständig warnen und Benutzer zu ermöglichen, dass domänenübergreifenden Datenzugriff Schulung viele Benutzer alle domänenübergreifenden zugriffsanforderungen genehmigen oder die ursprüngliche Domäne ihrer Liste **vertrauenswürdiger Websites** ohne Nachrichtenempfang hinzufügen, hat auffordern die Sicherheitsrisiken ernsthaft. Um dies zu vermeiden, Bereitstellen von InfoPath-Formularen auf demselben Server wie sämtliche, den Datenquellen, auf dem sie abhängig sind. 
  
 **Vermeiden der Verwendung von ActiveX-Steuerelemente, die nicht gekennzeichnet sind als sicher für Skripting**
  
Durch ActiveX-Steuerelemente können potenziell Eigenschaften und Methoden verfügbar gemacht werden, mit denen man sich den Zugang zum System eines Benutzers verschaffen kann, wie z. B. Methoden für den Zugriff auf das Dateisystem eines Computers. Sie sollten nach Möglichkeit nur ActiveX-Steuerelemente verwenden, die als sicher markiert sind. Hierbei handelt es sich um getestete Steuerelemente, die garantieren, dass das System eines Benutzers nicht beschädigt oder die Sicherheit des Benutzers nicht gefährdet wird, unabhängig davon, wie die Methoden und Eigenschaften des Steuerelements durch das Skript einer Webseite manipuliert werden. Beim Erstellen von ActiveX-Steuerelementen für die Verwendung mit InfoPath sollten Sie entsprechend den Code überprüfen und das ActiveX-Steuerelement gründlich testen, bevor Sie es als für die Ausführung sicher markieren.
  
InfoPath verwendet ein Sicherheitsmodell, das auf den Sicherheitszonen von Internet Explorer basiert. Deshalb verwendet ein InfoPath-Formular die gleichen Berechtigungen wie Internet Explorer, wodurch standardmäßig Skriptaufrufe für ActiveX-Steuerelemente, die als sicher markiert sind, ermöglicht werden, ohne dass die Benutzer aufgefordert werden.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Bewährte Methoden für die Verwaltung der CAB-Dateien von ActiveX-Steuerelementen

ActiveX-Steuerelemente können in Formularvorlagen für InfoPath-Editor für gehostet werden. CAB-Dateien für diese Steuerelemente, die nicht bereits auf dem Computer des Benutzers vorhanden sind, müssen in der Formularvorlagendatei (XSN) enthalten sein. CAB-Dateien in Formularvorlagen müssen digital signiert werden, in der Reihenfolge für die CAB-Datei installiert werden soll. InfoPath wird eine CAB-Datei, die nicht, unabhängig von der Vertrauensstellung oder der Sicherheitszone angemeldet ist, nicht installiert.
  
Um sicherzustellen, dass die digitale Signatur in der CAB-Datei überprüft werden kann, sollte die Datei mit einem Zertifikat signiert werden, das eine Vertrauenskette zu einem bereits vertrauenswürdigen Stammzertifikat aufweist. Andernfalls kann die Signatur nicht authentifiziert werden, die Signaturüberprüfung schlägt fehl, und die CAB-Datei wird nicht installiert.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Bewährte Methoden für als Anlage einer E-Mail-Nachricht gesendete Formularvorlagen

InfoPath unterstützt das Bereitstellen von Formularvorlagen als Anlage einer e-Mail-Nachricht und das Verschieben von Formularvorlagen von einem Speicherort in einen anderen. Es ist eine gute Sicherheitsmethode zum digitalen Signieren eine Formularvorlage, die Sie beim Entwerfen und als Anlage einer e-Mail-Nachricht bereitstellen möchten. Eine digitale Signatur auf einer Formularvorlage von e-Mail-Nachricht bereitgestellt wird nicht nur die Echtheit der Vorlage sichergestellt. Es hat auch den Vorteil, dass die Formularvorlage automatisch aktualisiert werden.
  
Die Formularvorlage sollte mit einem Zertifikat signiert werden, das eine Vertrauenskette zu einem bereits vertrauenswürdigen Stammzertifikat aufweist. Andernfalls schlägt die Signaturüberprüfung fehl, da die Signatur nicht authentifiziert werden kann.
  
> [!NOTE]
> Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, wird die Signatur von InfoPath nicht überprüft. Es wird lediglich festgestellt, ob die Vorlage von InfoPath automatisch aktualisiert werden kann. 
  
Weitere Informationen zur e-Mail-Bereitstellung finden in den [Sicherheitsstufen, Bereitstellung, per E-Mail und Remoteformularvorlagen](security-levels-email-deployment-and-remote-form-templates.md).
  

