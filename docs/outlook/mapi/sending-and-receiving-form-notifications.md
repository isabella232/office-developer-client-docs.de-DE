---
title: Senden und Empfangen von Formularbenachrichtigungen
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
# <a name="sending-and-receiving-form-notifications"></a>Senden und Empfangen von Formularbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularbenachrichtigungen werden in MAPI verwendet, um die Kommunikation sowohl vom Formular zum Viewer als auch vom Viewer zum Formular zu erleichtern.
  
Formulare senden Benachrichtigungen an Ihren Viewer, wenn eines der folgenden Ereignisse auftritt:
  
- Das Formular wird geschlossen.
    
- Im Formular wird eine neue Nachricht geladen.
    
- Ein Speichervorgang ist abgeschlossen.
    
- Es wird eine Nachricht gesendet.
    
Jeder dieser Ereignistypen entspricht einer bestimmten Methode in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), einer der Schnittstellen, die die Formularanzeige implementieren muss. Wenn ein Ereignis auftritt, ruft das Formular die entsprechende **IMAPIViewAdviseSink-Methode** in der Anzeigesenke auf. Wenn z. B. eine neue Nachricht eintrifft, die ihr Viewer in die Anzeige einbezahlen soll, ruft das Formular Ihre [IMAPIViewAdviseSink::OnNewMessage-Methode](imapiviewadvisesink-onnewmessage.md) auf. 
  
Implementieren Sie Ihre Ansichts-Ratensenke auf eine Weise, die für Ihren Betrachter sinnvoll ist. es gibt keine Standardimplementierung. Beispielsweise können Sie in **OnNewMessage** die Ansicht der Inhaltstabelle des aktuellen Ordners so aktualisieren, dass sie die neu eingetroffene Nachricht enthält. In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), der Methode, die aufgerufen wird, wenn Sie ein gesendetes Nachrichtenereignis empfangen, können Sie die übermittelte Nachricht in einen Ordner "Gesendete Elemente" kopieren.
  
Formulare erhalten eine Benachrichtigung von Ihrem Viewer, wenn eine Änderung auftritt, die sich auf das Formular auswirkt, und wenn Sie eine neue Nachricht laden. Rufen Sie zum Benachrichtigen eines Formulars eine der Methoden von **IMAPIFormAdviseSink** auf: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Rufen **Sie OnChange auf,** um den Status zu kommunizieren. Wenn das Formular z. B. das letzte Element in einem Ordner zeigt, wenn eine neue Nachricht eintrifft, rufen Sie **OnChange** mit dem VCSTATUS_NEXT-Flag auf, um dem Formular zu sagen, dass es jetzt ein nächstes Element gibt. 
  
Rufen **Sie OnActivateNext auf,** um das Formular vor dem Eintreffen einer neuen Nachricht zu warnen, die möglicherweise angezeigt werden kann oder nicht. Übergeben Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**. 
  
Benachrichtigungen eines Formularobjekts an die Clientanwendung werden von der **IMAPIViewAdviseSink-Schnittstelle** der Clientanwendung verarbeitet. Weitere Informationen finden Sie unter [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

