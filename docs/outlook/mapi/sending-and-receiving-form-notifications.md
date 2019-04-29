---
title: Senden und empfangen von Formular Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431855"
---
# <a name="sending-and-receiving-form-notifications"></a>Senden und empfangen von Formular Benachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formular Benachrichtigungen werden in MAPI verwendet, um die Kommunikation sowohl vom Formular zum Betrachter als auch von Ihrem Betrachter zum Formular zu erleichtern.
  
Formulare senden Benachrichtigungen an den Betrachter, wenn eines der folgenden Ereignisse eintritt:
  
- Das Formular ist geschlossen.
    
- Eine neue Nachricht wird in das Formular geladen.
    
- Ein Speichervorgang ist abgeschlossen.
    
- Eine Nachricht wird gesendet.
    
Jeder dieser Ereignistypen entspricht einer bestimmten Methode in [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), eine der Schnittstellen, die der Formular Betrachter implementieren muss. Wenn ein Ereignis auftritt, ruft das Formular die entsprechende **IMAPIViewAdviseSink** -Methode in der Advise-Senke des Viewers auf. Wenn beispielsweise eine neue Nachricht eingeht, die Ihr Viewer in die Anzeige aufnehmen soll, ruft das Formular die [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methode auf. 
  
Implementieren Sie Ihre Ansicht Advise-Senke auf eine Weise, die für Ihren Betrachter sinnvoll ist. Es gibt keine Standardimplementierung. In **OnNewMessage** können Sie beispielsweise die Ansicht der Inhaltstabelle des aktuellen Ordners aktualisieren, um die neu eingetroffene Nachricht einzuschließen. In [IMAPIViewAdviseSink:: onsubmitted](imapiviewadvisesink-onsubmitted.md), die Methode, die aufgerufen wird, wenn Sie ein gesendetes Nachrichtenereignis empfangen, können Sie die übermittelte Nachricht in einen Ordner "Gesendete Elemente" kopieren.
  
Formulare erhalten eine Benachrichtigung von Ihrem Betrachter, wenn eine Änderung auftritt, die sich auf das Formular auswirkt und wenn Sie eine neue Nachricht laden. Wenn Sie ein Formular benachrichtigen möchten, rufen Sie eine der Methoden von **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md)auf. Rufen **** Sie OnChange auf, um den Status zu kommunizieren. Wenn beispielsweise das Formular das letzte Element in einem Ordner anzeigt, wenn eine neue Nachricht eingeht, rufen **** Sie OnChange mit dem VCSTATUS_NEXT-Flag auf, um dem Formular mitzuteilen, dass es jetzt ein nächstes Element gibt. 
  
Rufen Sie **OnActivateNext** auf, um das Formular an den Eingang einer neuen Nachricht zu benachrichtigen, die möglicherweise nicht angezeigt werden kann oder nicht. Führen Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**. 
  
Benachrichtigungen durch ein Form-Objekt an die Clientanwendung werden von der **IMAPIViewAdviseSink** -Schnittstelle der Clientanwendung verarbeitet. Weitere Informationen finden Sie unter [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

