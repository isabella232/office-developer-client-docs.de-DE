---
title: MAPI-Berichtnachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: addf93cadae418017a40ba448328d2e1fc1decf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793061"
---
# <a name="mapi-report-messages"></a>MAPI-Berichtnachrichten

  
  
**Betrifft**: Outlook 
  
Melden von Nachrichten vorhanden Statusinformationen über eine Nachricht an den Absender.
  
Es gibt zwei allgemeine Arten von Nachrichten melden:
  
- Lesen Sie Statusberichte.
    
- Übermittlung Statusberichte.
    
## <a name="read-status-reports"></a>Lesen von Statusberichten

Lesen von Statusberichten werden Zeichenfolgeneigenschaften Nachricht durch einen Aufruf an die [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) -Methode initiiert und an den Empfänger, dargestellt durch die Eintrags-ID in der **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) gesendet werden -Eigenschaft. Statusberichte lesen werden nicht automatisch erstellt. Clientanwendungen, die sie erhalten möchten, müssen sie explizit anfordern.
  
Lese-Bericht gibt an, dass das Flag Lesen einer Nachricht die kann auftreten, wenn die Nachricht geöffnet, gedruckt, kopiert oder verschoben wird, festgelegt wurde. Unabhängig davon, ob eine Nachricht Speicheranbieter generiert einen lesen Bericht als Antwort auf eine Verschiebung oder Kopiervorgang, hängt davon ab, in dem die Nachricht gesendet wird. Wenn es ist, die verschoben oder kopiert an einen anderen Nachrichtenspeicher eine Lese-Bericht wird sehr wahrscheinlich immer gesendet. Wenn es gerade verschoben oder kopiert haben, in der aktuellen Nachrichtenspeicher Lese-Bericht möglicherweise oder möglicherweise nicht gesendet werden. 
  
Ein Bericht nonread gibt an, dass das Flag Lesen einer Nachricht nicht festgelegt ist und dass die Nachricht nicht entweder vor in den Ordner Gelöschte Objekte gespeichert wird, oder vor dem Ablauf eines Zeitlimits geöffnet wurde. Clients können die [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) -Methode, um festzulegen, oder eine Nachricht lesen Kennzeichnung löschen aufrufen. 
  
## <a name="delivery-status-reports"></a>Übermittlungsberichte Status

Zustellungsstatus wiedergegeben wird, in einen Übermittlungsbericht, die gesendet wird, wenn eine Nachricht den Empfänger erreicht hat, und ein Unzustellbarkeitsbericht, die gesendet wird, wenn eine Nachricht einen Empfänger nicht erreichen konnte. Übermittlungsberichte Status werden an den Empfänger, dargestellt durch die Eintrags-ID in der Eigenschaft **PR_REPORT_ENTRYID** oder an den Absender gesendet, wenn diese Eigenschaft nicht vorhanden ist. 
  
Übermittlungsberichte werden nur auf Anforderung gesendet und die ursprüngliche Nachricht nicht einschließen. Unzustellbarkeitsberichten werden automatisch gesendet, es sei denn, sie unterdrückt eine Anforderung gestellt wird. Unzustellbarkeitsberichten enthalten die ursprüngliche Nachricht als Anlage so aktivieren Sie den Bericht Empfänger die Nachricht erneut zu senden, für den Fall, dass Sie den Inhalt die Lieferung blockiert nicht mehr ein Problem darstellt. Die Nachricht angefügte ähnelt den ursprünglichen vorhanden war die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wurde, zunächst zu senden. 
  
Mindestens einen Status Übermittlungsberichte werden von Transportanbieter generiert, wenn sie die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode aufrufen. Transportanbieter Verfassenmodus eine Liste der Empfänger einer Nachricht. Unabhängig davon, ob ein Empfänger empfängt, ein Bericht und den Typ des Berichts, die generiert wird, hängt von folgenden Faktoren ab: 
  
- Übermittlungsberichte wechseln Sie zu Empfänger, die die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))-Eigenschaft auf TRUE festgelegt, bevor die Nachricht im Nachrichtenspeicher getätigt wurde.
    
- Unzustellbarkeitsberichten wechseln Sie zu Empfänger an, die nicht die **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md))-Eigenschaft auf FALSE festgelegt. 
    
Fast alle erforderlichen Informationen von einem Unzustellbarkeitsbericht anzeigen in der Tabelle Empfänger der Nachricht angefügte enthalten ist. Einige Eigenschaften sind aus dem Bericht selbst. Für Übermittlungsberichte ist die erforderliche Informationen in der Tabelle Empfänger des Berichts und einige Eigenschaften des Berichts enthalten. 
  
Berichte werden Nachrichten mit unterschiedlichen Nachrichtenklassen, basierend auf der Klasse die gesendete Nachricht. Die meisten Dienstanbieter verwenden eine Namenskonvention fest, bei dem die Nachrichtenklasse aus mehreren Teilen durch Punkte getrennt ist. Der erste Teil ist "Report" und der letzte Teil ist eine Konstante, die den Typ des Berichts darstellt. Im mittleren Bereich ist für die Klasse der gesendeten Nachricht reserviert. Beispielsweise, da die Konstante DR ein Unzustellbarkeitsberichts verwendet werden, die Nachrichtenklasse für eine Übermittlung Berichten zu einer IPM. Hinweis Nachricht wäre **Report.IPM.Note.DR**.
  
Die folgende Tabelle enthält die Konstanten, mit die die Typen von Berichten darstellen.
  
|**Berichtstyp**|**Konstante in der Nachrichtenklasse**|
|:-----|:-----|
|Lesen  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|Übermittlung  <br/> |DR  <br/> |
|NonDelivery  <br/> |NDR  <br/> |
   
Interactive-Clients können Nachrichten melden anzeigen, mithilfe von MAPI bereitgestellten Standardformulare oder benutzerdefinierte Formulare, die mit dem Formular-Manager für den Bericht Nachrichtenklasse registriert wurden. Clients, die einen für ein IPM Unzustellbarkeitsbericht. Hinweis Nachricht, kann beispielsweise das MAPI-Standardformular anzeigen, das eine Liste der fehlerhaften Empfänger und einer vorgeschlagenen Grund für den Fehler anzeigt. Das Formular ermöglicht dem Benutzer erneuten Senden die Nachricht auch, falls gewünscht. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

