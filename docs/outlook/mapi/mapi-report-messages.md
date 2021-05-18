---
title: MAPI-Berichtsmeldungen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405765"
---
# <a name="mapi-report-messages"></a>MAPI-Berichtsmeldungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Berichtsmeldungen enthalten Statusinformationen zu einer Nachricht an den Absender.
  
Es gibt zwei allgemeine Typen von Berichtsmeldungen:
  
- Lesen von Statusberichten.
    
- Übermittlungsstatusberichte.
    
## <a name="read-status-reports"></a>Lesen von Statusberichten

Read status reports are initiated by message store providers through a call to the [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method and are sent to the recipient represented by the entry identifier in **the PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) property. Lesestatusberichte werden nicht automatisch generiert. Clientanwendungen, die sie empfangen möchten, müssen diese explizit anfordern.
  
Ein Lesebericht gibt an, dass das Leseflag einer Nachricht festgelegt wurde, was auftreten kann, wenn die Nachricht geöffnet, gedruckt, verschoben oder kopiert wird. Ob ein Nachrichtenspeicheranbieter als Reaktion auf einen Verschiebe- oder Kopiervorgang einen Lesebericht generiert, hängt davon ab, wo die Nachricht angezeigt wird. Wenn er verschoben oder in einen anderen Nachrichtenspeicher kopiert wird, wird höchstwahrscheinlich immer ein Lesebericht gesendet. Wenn er im aktuellen Nachrichtenspeicher verschoben oder kopiert wird, wird möglicherweise ein Lesebericht gesendet. 
  
Ein nicht gelesener Bericht gibt an, dass das Leseflag einer Nachricht nicht festgelegt ist und dass die Nachricht nicht geöffnet wurde, bevor sie im Ordner Gelöschte Elemente oder vor Ablauf eines Zeitlimits platziert wurde. Clients können die [IMessage::SetReadFlag-](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags-Methode](imapifolder-setreadflags.md) aufrufen, um das Leseflag einer Nachricht zu setzen oder zu löschen. 
  
## <a name="delivery-status-reports"></a>Übermittlungsstatusberichte

Der Zustellungsstatus spiegelt sich in einem Zustellungsbericht wider, der gesendet wird, wenn eine Nachricht den beabsichtigten Empfänger erreicht hat, und in einem Nicht-Zustellungsbericht, der gesendet wird, wenn eine Nachricht keinen Empfänger erreichen konnte. Übermittlungsstatusberichte werden an den Empfänger gesendet, der durch die Eintrags-ID in der **PR_REPORT_ENTRYID-Eigenschaft** dargestellt wird, oder an den Absender, wenn diese Eigenschaft nicht vorhanden ist. 
  
Übermittlungsberichte werden nur per Anforderung gesendet und enthalten nicht die ursprüngliche Nachricht. Unauslöschungsberichte werden automatisch gesendet, es sei denn, es wird eine Anforderung zur Unterdrückung gestellt. Nicht-Zustellungsberichte enthalten die ursprüngliche Nachricht als Anlage, damit der Empfänger des Berichts die Nachricht erneut senden kann, falls die Blockiertheit der Zustellung kein Problem mehr ist. Die angefügte Nachricht ähnelt dem Original, wie es beim ersten Senden der [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) vorhanden war. 
  
Mindestens ein Zustellungsstatusbericht wird von Transportanbietern generiert, wenn sie die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) aufrufen. Transportanbieter erstellen eine Liste der Empfänger für eine Nachricht. Ob ein Empfänger einen Bericht empfängt und welche Art von Bericht generiert wird, hängt von folgenden Kriterien ab: 
  
- Übermittlungsberichte gehen an Empfänger, die **die PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) -Eigenschaft auf TRUE festlegen, bevor die Nachricht im Nachrichtenspeicher platziert wurde.
    
- #A0 gehen an Empfänger, die die **eigenschaft PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) nicht auf FALSE festgelegt haben. 
    
Fast alle Informationen, die zum Anzeigen eines Nichtverstellberichts erforderlich sind, sind in der Empfängertabelle der angefügten Nachricht enthalten. Einige Eigenschaften sind aus dem Bericht selbst. Für Übermittlungsberichte sind die erforderlichen Informationen in der Empfängertabelle des Berichts und in einigen Berichtseigenschaften enthalten. 
  
Berichte sind Nachrichten mit unterschiedlichen Nachrichtenklassen, die auf der Klasse der gesendeten Nachricht basieren. Die meisten Dienstanbieter verwenden eine Benennungskonvention, bei der die Nachrichtenklasse aus mehreren Teilen besteht, die durch Punkte getrennt sind. Der erste Teil ist "Bericht", und der letzte Teil ist eine Konstante, die den Berichtstyp darstellt. Der mittlere Teil ist für die Klasse der gesendeten Nachricht reserviert. Da ein Zustellungsbericht beispielsweise die Konstante DR verwendet, wird die Nachrichtenklasse für einen Übermittlungsbericht über ein IPM verwendet. Hinweisnachricht lautet **Report.IPM.Note.DR**.
  
In der folgenden Tabelle sind die Konstanten aufgeführt, die die Typen von Berichten darstellen.
  
|**Berichttyp**|**In der Nachrichtenklasse verwendete Konstante**|
|:-----|:-----|
|Lesen  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|Übermittlung  <br/> |DR  <br/> |
|Nondelivery  <br/> |NDR  <br/> |
   
Interaktive Clients können Berichtsnachrichten mithilfe von Standardformularen anzeigen, die von MAPI bereitgestellt werden, oder benutzerdefinierten Formularen, die beim Formular-Manager für die Nachrichtenklasse des Berichts registriert wurden. Clients, die einen Unauslöschungsbericht für ein IPM erhalten. Hinweismeldung kann z. B. das standardmäßige MAPI-Formular anzeigen, das eine Liste der fehlgeschlagenen Empfänger und einen vorgeschlagenen Grund für den Fehler enthält. Das Formular ermöglicht es dem Benutzer auch, die Nachricht bei Bedarf erneut zu senden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

