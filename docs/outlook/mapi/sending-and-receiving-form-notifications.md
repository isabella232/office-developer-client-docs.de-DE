---
title: Senden und Empfangen von Formularbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 57a4e4d1a39130e666b786f51c0ea48c7966c656
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550064"
---
# <a name="sending-and-receiving-form-notifications"></a>Senden und Empfangen von Formularbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularbenachrichtigungen werden in DER MAPI verwendet, um die Kommunikation sowohl vom Formular an den Betrachter als auch vom Betrachter zum Formular zu vereinfachen.
  
Formulare senden Benachrichtigungen an den Betrachter, wenn eines der folgenden Ereignisse auftritt:
  
- Das Formular ist geschlossen.
    
- Eine neue Nachricht wird im Formular geladen.
    
- Ein Speichervorgang ist abgeschlossen.
    
- Eine Nachricht wird gesendet.
    
Jeder dieser Ereignistypen entspricht einer bestimmten Methode in [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), einer der Schnittstellen, die der Formularviewer implementieren muss. Wenn ein Ereignis auftritt, ruft das Formular die entsprechende **IMAPIViewAdviseSink-Methode** in der Empfehlungssenke Ihres Betrachters auf. Wenn beispielsweise eine neue Nachricht eingeht, die der Betrachter in die Anzeige aufnehmen soll, ruft das Formular die [IMAPIViewAdviseSink::OnNewMessage-Methode auf.](imapiviewadvisesink-onnewmessage.md) 
  
Implementieren Sie ihre Ansichts-Empfehlungssenke so, dass sie für Ihren Betrachter sinnvoll ist. es gibt keine Standardimplementierungen. In **OnNewMessage** können Sie beispielsweise die Ansicht des Inhaltsverzeichnisses des aktuellen Ordners aktualisieren, um die neu empfangene Nachricht einzuschließen. In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), der Methode, die aufgerufen wird, wenn Sie ein gesendetes Nachrichtenereignis erhalten, können Sie die gesendete Nachricht in einen Ordner "Gesendete Elemente" kopieren.
  
Formulare erhalten eine Benachrichtigung von Ihrem Viewer, wenn eine Änderung auftritt, die sich auf das Formular auswirkt, und wenn Sie eine neue Nachricht laden. Um ein Formular zu benachrichtigen, rufen Sie eine der Methoden von **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink::OnActivateNext auf.](imapiformadvisesink-onactivatenext.md) Rufen Sie **OnChange auf,** um den Status zu kommunizieren. Wenn das Formular beispielsweise das letzte Element in einem Ordner anzeigt, wenn eine neue Nachricht eingeht, rufen Sie **OnChange auf,** wobei das VCSTATUS_NEXT-Flag festgelegt ist, um dem Formular mitzuteilen, dass jetzt ein nächstes Element vorhanden ist. 
  
Rufen Sie **OnActivateNext auf,** um das Formular vor dem Eintreffen einer neuen Nachricht zu benachrichtigen, die möglicherweise angezeigt werden kann. Übergeben Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**. 
  
Benachrichtigungen von einem Formularobjekt an die Clientanwendung werden von der **IMAPIViewAdviseSink-Schnittstelle** der Clientanwendung verarbeitet. Weitere Informationen finden Sie unter [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

