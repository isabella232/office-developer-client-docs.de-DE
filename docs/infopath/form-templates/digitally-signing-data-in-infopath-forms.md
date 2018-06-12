---
title: Digitales Signieren von Daten in InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Bei einer digitalen Signatur handelt es sich um einen elektronischen, verschlüsselungsbasierten, sicheren Echtheitsstempel in einem Makro oder Dokument. Eine gültige digitale Signatur bestätigt, dass die Daten vom Signierer stammen und seit dem Signieren nicht geändert wurden. Wenn Dokumente oder bestimmte Daten in den Dokumenten signiert werden, wird die Signatur berechnet und dem Dokument hinzugefügt. Auf diese Weise werden die Signaturen immer zusammen mit den signierten Daten übertragen.
ms.openlocfilehash: dc839d0751d2e7aeb6f9eaccc3a86ce95e5228e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790717"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Digitales Signieren von Daten in InfoPath-Formularen

Bei einer digitalen Signatur handelt es sich um einen elektronischen, verschlüsselungsbasierten, sicheren Echtheitsstempel in einem Makro oder Dokument. Eine gültige digitale Signatur bestätigt, dass die Daten vom Signierer stammen und seit dem Signieren nicht geändert wurden. Wenn Dokumente oder bestimmte Daten in den Dokumenten signiert werden, wird die Signatur berechnet und dem Dokument hinzugefügt. Auf diese Weise werden die Signaturen immer zusammen mit den signierten Daten übertragen.
  
Zum Signieren von Daten müssen die Benutzer von einer Zertifizierungsstelle ein Zertifikat anfordern und damit dann digitale Signaturen erstellen. Die Zertifizierungsstelle verwaltet den Lebenszyklus der Zertifikate und Schlüssel (öffentlich oder privat), die zum Verschlüsseln von Daten und zum Erstellen der Signatur erforderlich sind.
  
Nachfolgende Benutzer des Dokuments müssen vorhandene Signaturen überprüfen und können in Abhängigkeit vom Ergebnis dieser Überprüfung einen eigenen Beitrag und ihre eigene Signatur hinzufügen. Für präzise Ergebnisse muss die überprüfende Person der Zertifizierungsstelle vertrauen, die das Zertifikat ausgestellt hat, mit dem das Dokument ursprünglich signiert wurde.
  
Digitale XML-Signaturen sind für Transaktionen vorgesehen, an denen XML-Dokumente und -Daten beteiligt sind. Digitale XML-Signaturen haben den Vorteil, dass damit nur bestimmte Daten in einem XML-Dokument signiert werden können.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Typen digitaler Signaturen in InfoPath-Formularen

Microsoft InfoPath implementiert digitale Signaturen, mit denen Daten in InfoPath-Formularen gesichert werden. In InfoPath werden zwei Arten von digitalen Signaturen Funktionsumfang:
  
- Digitale Signaturen, mit denen die Datenintegrität und Echtheit der Formularvorlage (XSN-Datei) sichergestellt werden.
    
- Digitale Signaturen, mit denen die Integrität, Echtheit und Unterstützung der Nichtabstreitbarkeit im Zusammenhang mit Daten in XML-Formularen sichergestellt werden.
    
Während die erste Kategorie von Signaturen, die Formularvorlage (XSN-Datei) abzielt, beruht die zweite Kategorie auf die aktuellen Benutzer eingegebenen Daten in InfoPath-Formulardateien (XML-Dateien), in dem der Formulardesigner Benutzer digitale Signaturen für das gesamte erstellen aktivieren können Formular oder für Abschnitte des Formulars. Es gibt grundlegende Unterschiede zwischen einer signierten Vorlage und einem signierten Formular. Obwohl einige Verweise auf signierte Vorlagen bestehen (als alternative Möglichkeit zum Erstellen eines Formulars, das ausgeführt wird, als voll vertrauenswürdige), werden keine Informationen zu dieser Art von Signieren bereitgestellt. Weitere Informationen zum Signieren von Formularvorlagen finden Sie unter [Bereitstellen signierter InfoPath Formularvorlagen](deploying-signed-infopath-form-templates.md) verwendet der Fokus in diesem Thema signierte InfoPath XML-Formulare. Digitale Signaturen von InfoPath zum Signieren von Daten in XML-Formularen erstellten erfüllen W3C XML digitale Signaturen Spezifikationen. 
  
## <a name="digital-signatures-features"></a>Features für digitale Signaturen

InfoPath enthält ein erweitertes Feature für digitale Signaturen, mit dem Vorlagenentwickler flexible Formulare entwerfen können, die digitale Signaturen für das gesamte Formular oder für bestimmte Daten im Formular ermöglichen. Während beim digitalen Signieren des gesamten Formulars stets Gegensignaturen für das Formular insgesamt erstellt werden, ermöglicht das Signieren von Teilen von InfoPath-Formularen mehr Flexibilität beim Auswählen der Beziehungsart zwischen Signaturen, die derselben Datengruppe hinzugefügt werden: gemeinsame Signaturen, Gegensignaturen oder nur eine einzige Signatur können zulässig sein.
  
Zusammen mit der Signatur werden von InfoPath außerdem standardmäßig Nichtabstreitbarkeitsinformationen hinzugefügt, um die Daten zu identifizieren, die den Benutzern in der aktuellen Ansicht angezeigt wurden, sowie die Uhrzeit und sonstige Umgebungseinstellungen, die beim Erstellen der Signatur festgelegt waren. Die Nichtabstreitbarkeitsinformationen können angepasst werden, aber nur die Daten in den standardmäßigen Nichtabstreitbarkeitsknoten werden im Nichtabstreitbarkeitsdialogfeld angezeigt.
  
Um eine Signatur hinzuzufügen, müssen die Benutzer die zu signierende Datengruppe auswählen. Die Datengruppe, die signiert werden kann, wird vom Formularvorlagendesigner definiert und zum Signieren der Daten beim Ausfüllen des Formulars verwendet. Für jede Signatur müssen die Benutzer einen Assistenten für digitale Signaturen ausführen, um die signierbare Datengruppe auszuwählen, ein Zertifikat auszuwählen, Kommentare hinzuzufügen sowie die Signatur für das Formular zu genehmigen und ein Commit dafür auszuführen.
  
Wenn ein Benutzer die Maus auf ein Steuerelement bewegt, das signierte Daten enthält, wird ein grafischer Indikator angezeigt, dass die Daten signiert sind und nicht geändert werden können. Formularvorlagendesigner können festlegen, dass die Signaturen in der Ansicht mit den signierten Daten angezeigt werden, damit die Benutzer auf einfache Weise auf die Nichtabstreitbarkeitsinformationen zugreifen können.
  
## <a name="programmatic-support-for-digital-signatures"></a>Programmgesteuerte Unterstützung digitaler Signaturen

Das InfoPath-Objektmodell umfasst Unterstützung für digitale Signaturen, wodurch Entwickler, die programmgesteuerten Zugriff auf den einzelnen signierbarer Daten in das Formular kann über die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Klasse für die zugewiesenen jeder Gruppe von Signaturen definiert sind signiert Daten über die [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Klasse, und klicken Sie auf das Zertifikat, das zum Erstellen einer Signatur über den [Zertifikat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) -Klasse verwendet wird. Darüber hinaus ist der [Anmelde](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignishandler in voll vertrauenswürdige Formulare, bietet Unterstützung für erweiterte Verarbeitung digitaler Signaturen in InfoPath-Formularen anpassbar. 
  
## <a name="interoperability"></a>Interoperabilität

Die Infrastruktur für digitale Signaturen in InfoPath wurde mithilfe der Unterstützung digitaler Signaturen in MSXML5 entwickelt, sodass digitale InfoPath-Signaturen vollständig mit digitalen MSXML5-Signaturen kompatibel sind.
  
Von InfoPath erstellte signierte InfoPath-Formulare und digitale Signaturen sind außerdem vollständig mit digitalen Signaturen kompatibel, die mit Microsoft .NET Framework (ab Version 1.1) erstellt wurden. Von InfoPath erstellte Signaturen können durch Anwendungen überprüft werden, die Signaturüberprüfungsklassen von .NET Framework verwenden. Signaturen, die für in InfoPath-Formularen gehostete Daten von Anwendungen erstellt wurden, die mithilfe der Klassen für digitale Signaturen von .NET Framework entwickelt wurden, werden vom Feature für digitale Signaturen von InfoPath erfolgreich überprüft.
  
## <a name="see-also"></a>Siehe auch



[Arbeiten mit digitalen Signaturen](how-to-work-with-digital-signatures.md)

