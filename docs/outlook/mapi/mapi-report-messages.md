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
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329743"
---
# <a name="mapi-report-messages"></a>MAPI-Berichtnachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Berichtnachrichten geben dem Absender Statusinformationen zu einer Nachricht.
  
Es gibt zwei allgemeine Arten von Berichtnachrichten:
  
- Lesen Sie Statusberichte.
    
- ZuStellungsstatus Berichte.
    
## <a name="read-status-reports"></a>Lesen von Status Berichten

Lesestatus Berichte werden von Nachrichtenspeicher Anbietern durch einen Aufruf der [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) -Methode initiiert und an den Empfänger gesendet, der durch die Eintrags-ID im **PR_REPORT_ENTRYID** ([pidtagreportentryid (](pidtagreportentryid-canonical-property.md)) Eigenschaft. Lesestatus Berichte werden nicht automatisch generiert; Clientanwendungen, die Sie empfangen möchten, müssen Sie explizit anfordern.
  
Ein Lesebericht gibt an, dass die Read-Kennzeichnung einer Nachricht festgelegt wurde, die beim Öffnen, drucken, verschieben oder Kopieren der Nachricht auftreten kann. Ob ein Nachrichtenspeicher Anbieter als Reaktion auf einen Vorgang zum Verschieben oder kopieren einen Lesebericht generiert, hängt davon ab, wo die Nachricht gesendet wird. Wenn Sie in einen anderen Nachrichtenspeicher verschoben oder kopiert wird, wird wahrscheinlich immer ein Lesebericht gesendet. Wenn Sie im aktuellen Nachrichtenspeicher verschoben oder kopiert wird, wird möglicherweise ein Lesebericht gesendet. 
  
Ein nicht gelesener Bericht gibt an, dass die Read-Kennzeichnung einer Nachricht nicht festgelegt ist und dass die Nachricht nicht geöffnet wurde, bevor Sie im Ordner "Gelöschte Elemente" oder vor Ablauf eines Zeitlimits abgelegt wurde. Clients können die [IMessage:: SetReadFlag](imessage-setreadflag.md) -oder [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) -Methode aufrufen, um die Read-Kennzeichnung einer Nachricht festzulegen oder zu löschen. 
  
## <a name="delivery-status-reports"></a>Berichte über den zuStellungs Status

Der Übermittlungsstatus wird in einem Zustellungsbericht widergespiegelt, der gesendet wird, wenn eine Nachricht den beabsichtigten Empfänger erreicht hat, und in einem Unzustellbarkeitsbericht, der gesendet wird, wenn eine Nachricht keinen Empfänger erreichen konnte. ZuStellungsstatus Berichte werden an den Empfänger gesendet, der durch den Eintragsbezeichner in der **PR_REPORT_ENTRYID** -Eigenschaft oder an den Absender dargestellt wird, wenn diese Eigenschaft nicht vorhanden ist. 
  
Übermittlungsberichte werden nur auf Anforderung gesendet, und die ursprüngliche Nachricht wird nicht eingeschlossen. Unzustellbarkeitsberichte werden automatisch gesendet, es sei denn, Sie werden aufgefordert, Sie zu unterdrücken. Unzustellbarkeitsberichte schließen die ursprüngliche Nachricht als Anlage ein, damit der Empfänger des Berichts die Nachricht erneut senden kann, falls blockiert wird, dass die Übermittlung kein Problem mehr ist. Die angefügte Nachricht ähnelt der ursprünglichen, wenn Sie vorhanden war, als die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode zum anfänglichen senden aufgerufen wurde. 
  
Ein oder mehrere Übermittlungsstatusberichte werden von Transportanbietern generiert, wenn Sie die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode aufrufen. Transport Anbieter verfassen eine Liste von Empfängern für eine Nachricht. Hängt davon ab, ob ein Empfänger einen Bericht empfängt oder nicht, und wie der generierte Berichttyp generiert wird: 
  
- ZuStellungsberichte gehen an Empfänger, die die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))-Eigenschaft auf true festlegen, bevor die Nachricht im Nachrichtenspeicher abgelegt wurde.
    
- Unzustellbarkeitsberichte gehen an Empfänger, die die **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([pidtagoriginatornondeliveryreportrequested (](pidtagoriginatornondeliveryreportrequested-canonical-property.md))-Eigenschaft nicht auf false festgelegt haben. 
    
Fast alle erforderlichen Informationen, um einen Unzustellbarkeitsbericht anzuzeigen, sind in der Empfängertabelle der angefügten Nachricht enthalten. Einige Eigenschaften sind aus dem Bericht selbst. Für Zusteller-Berichte sind die erforderlichen Informationen in der Empfängertabelle des Berichts und in einigen Berichtseigenschaften enthalten. 
  
Berichte sind Nachrichten mit unterschiedlichen Nachrichtenklassen, basierend auf der Klasse der gesendeten Nachricht. Die meisten Dienstanbieter verwenden eine Benennungskonvention, wobei die Nachrichtenklasse aus mehreren Teilen besteht, die durch Punkte getrennt sind. Der erste Teil ist "Bericht", und der letzte Teil ist eine Konstante, die den Berichtstyp darstellt. Der mittlere Teil ist für die Klasse der gesendeten Nachricht reserviert. Da ein zugestellter Bericht beispielsweise die Konstante DR verwendet, wird die Nachrichtenklasse für einen Übermittlungsbericht zu einem IPM. Hinweis Nachricht wäre **Report. IPM. Note. Dr**.
  
In der folgenden Tabelle sind die Konstanten dargestellt, die die Berichtstypen darstellen.
  
|**Berichttyp**|**In der Nachrichtenklasse verwendete Konstante**|
|:-----|:-----|
|Lesen  <br/> |IPNRN  <br/> |
|Ungelesen  <br/> |IPNNRN  <br/> |
|Übermittlung  <br/> |DR  <br/> |
|Unzustellbarkeits  <br/> |NDR  <br/> |
   
Interaktive Clients können Berichtnachrichten mithilfe von MAPI bereitgestellten Standardformularen oder benutzerdefinierten Formularen anzeigen, die beim Formular-Manager für die Nachrichtenklasse des Berichts registriert wurden. Clients, die einen Unzustellbarkeitsbericht für eine IPM erhalten. Hinweis die Meldung kann beispielsweise das standardmäßige MAPI-Formular anzeigen, das eine Liste der fehlerhaften Empfänger und einen empfohlenen Grund für den Fehler enthält. Das Formular ermöglicht es dem Benutzer auch, die Nachricht erneut zu senden, falls gewünscht. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

