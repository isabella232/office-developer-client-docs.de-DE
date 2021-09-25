---
title: MAPI-Berichtsnachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 383c673a7313bb3a91e35f109399be92f98e215f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575680"
---
# <a name="mapi-report-messages"></a>MAPI-Berichtsnachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Melden Sie Nachrichten, die Statusinformationen zu einer Nachricht an den Absender senden.
  
Es gibt zwei allgemeine Typen von Berichtsnachrichten:
  
- Lesen von Statusberichten.
    
- Übermittlungsstatusberichte.
    
## <a name="read-status-reports"></a>Statusberichte lesen

Lesestatusberichte werden von Nachrichtenspeicheranbietern durch einen Aufruf der [IMAPISupport::ReadReceipt-Methode](imapisupport-readreceipt.md) initiiert und an den Empfänger gesendet, der durch den Eintragsbezeichner in der **Eigenschaft PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) dargestellt wird. Lesestatusberichte werden nicht automatisch generiert. Clientanwendungen, die sie empfangen möchten, müssen sie explizit anfordern.
  
Ein Lesebericht gibt an, dass das Lesekennzeichen einer Nachricht festgelegt wurde, das auftreten kann, wenn die Nachricht geöffnet, gedruckt, verschoben oder kopiert wird. Ob ein Nachrichtenspeicheranbieter als Reaktion auf einen Verschiebungs- oder Kopiervorgang einen Lesebericht generiert, hängt davon ab, wohin die Nachricht geht. Wenn sie in einen anderen Nachrichtenspeicher verschoben oder kopiert wird, wird höchstwahrscheinlich immer ein Lesebericht gesendet. Wenn sie im aktuellen Nachrichtenspeicher verschoben oder kopiert wird, wird möglicherweise ein Lesebericht gesendet. 
  
Ein nicht gelesener Bericht gibt an, dass das Lesekennzeichen einer Nachricht nicht festgelegt ist und dass die Nachricht weder vor dem Ablegen im Ordner "Gelöschte Elemente" noch vor Ablauf eines Zeitlimits geöffnet wurde. Clients können die [IMessage::SetReadFlag-](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags-Methode](imapifolder-setreadflags.md) aufrufen, um das Leseflag einer Nachricht festzulegen oder zu löschen. 
  
## <a name="delivery-status-reports"></a>Übermittlungsstatusberichte

Der Zustellungsstatus wird in einem Übermittlungsbericht widergespiegelt, der gesendet wird, wenn eine Nachricht den gewünschten Empfänger erreicht hat, und in einem Nichtzustellbarkeitsbericht, der gesendet wird, wenn eine Nachricht einen Empfänger nicht erreichen konnte. Übermittlungsstatusberichte werden an den Empfänger gesendet, der durch den Eintragsbezeichner in der **PR_REPORT_ENTRYID-Eigenschaft** dargestellt wird, oder an den Absender, wenn diese Eigenschaft nicht vorhanden ist. 
  
Übermittlungsberichte werden nur nach Anforderung gesendet und enthalten nicht die ursprüngliche Nachricht. Unzustellbarkeitsberichte werden automatisch gesendet, es sei denn, sie werden unterdrückt. Nichtzustellbarkeitsberichte enthalten die ursprüngliche Nachricht als Anlage, damit der Empfänger des Berichts die Nachricht erneut senden kann, falls die blockierte Zustellung kein Problem mehr ist. Die angefügte Nachricht ähnelt dem Original, wie sie vorhanden war, als die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen wurde, um sie zu senden. 
  
Ein oder mehrere Übermittlungsstatusberichte werden von Transportanbietern generiert, wenn sie die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) aufrufen. Transportanbieter erstellen eine Liste der Empfänger für eine Nachricht. Ob ein Empfänger einen Bericht empfängt und welche Art von Bericht generiert wird, hängt von Folgendem ab: 
  
- Übermittlungsberichte werden an Empfänger weitergeleitet, die die **Eigenschaft PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) auf TRUE festlegen, bevor die Nachricht im Nachrichtenspeicher platziert wurde.
    
- Nicht-Absenderberichte gehen an Empfänger, die die **eigenschaft PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) nicht auf FALSE festgelegt haben. 
    
Fast alle Informationen, die zum Anzeigen eines Nichtzustellbarkeitsberichts erforderlich sind, sind in der Empfängertabelle der angefügten Nachricht enthalten. Einige Eigenschaften stammen aus dem Bericht selbst. Für Übermittlungsberichte sind die erforderlichen Informationen in der Empfängertabelle des Berichts und in einigen Berichtseigenschaften enthalten. 
  
Berichte sind Nachrichten mit unterschiedlichen Nachrichtenklassen, basierend auf der Klasse der gesendeten Nachricht. Die meisten Dienstanbieter verwenden eine Benennungskonvention, bei der die Nachrichtenklasse aus mehreren Teilen besteht, die durch Punkte getrennt sind. Der erste Teil ist "Bericht", und der letzte Teil ist eine Konstante, die den Berichtstyp darstellt. Der mittlere Teil ist für die Klasse der gesendeten Nachricht reserviert. Beispielsweise, da ein Übermittlungsbericht die Konstante DR verwendet, die Nachrichtenklasse für einen Übermittlungsbericht zu einem IPM. Hinweismeldung wäre **Report.IPM.Note.DR**.
  
In der folgenden Tabelle sind die Konstanten aufgeführt, die die Typen von Berichten darstellen.
  
|**Berichttyp**|**Konstante, die in der Nachrichtenklasse verwendet wird**|
|:-----|:-----|
|Lesen  <br/> |IPNRN  <br/> |
|Nicht gelesen  <br/> |IPNNRN  <br/> |
|Übermittlung  <br/> |DR  <br/> |
|Nondelivery  <br/> |UNZUSTELLBARKEITSBERICHT  <br/> |
   
Interaktive Clients können Berichtsnachrichten mithilfe von Standardformularen anzeigen, die von mapi bereitgestellt werden, oder mit benutzerdefinierten Formularen, die beim Formular-Manager für die Nachrichtenklasse des Berichts registriert wurden. Clients, die einen Nicht-Bericht für ein IPM erhalten. Eine Notiznachricht kann z. B. das standardmäßige MAPI-Formular anzeigen, das eine Liste der fehlgeschlagenen Empfänger und einen vorgeschlagenen Grund für den Fehler enthält. Das Formular ermöglicht es dem Benutzer auch, die Nachricht bei Bedarf erneut zu senden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

