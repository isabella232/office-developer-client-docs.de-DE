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
ms.openlocfilehash: 7148383c92b59adb9d3783e079e7c5f28c038eac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588993"
---
# <a name="sending-and-receiving-form-notifications"></a>Senden und Empfangen von Formularbenachrichtigungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Formular Benachrichtigungen werden in MAPI verwendet, um Kommunikation sowohl aus dem Formular an die Anzeige sowie aus Ihrer Viewer auf das Formular zu vereinfachen.
  
Formulare senden Benachrichtigungen für Ihre Betrachter, wenn eines der folgenden Ereignisse auftreten:
  
- Das Formular geschlossen wird.
    
- Eine neue Nachricht wird in das Formular geladen.
    
- Ein Speichervorgang abgeschlossen ist.
    
- Eine Nachricht wird gesendet.
    
Jede dieser Ereignistypen in eine bestimmte Methode entspricht [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), eine der Schnittstellen, die Ihr Formular Viewer implementiert werden muss. Bei Auftreten eines Ereignisses, das Formular Anrufe in der Warteschlangenanzeige die entsprechende **IMAPIViewAdviseSink** -Methode des advise-Empfänger. Beispielsweise beim Eintreffen einer neuen Nachricht, dass Ihre Viewer in seiner Darstellung aufgenommen werden sollen, ruft das Formular zu Ihrer [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methode. 
  
Implementieren Sie Ihre Ansicht advise-Empfänger in eine Möglichkeit, dass Ihre Viewer sinnvoll; Es ist keine standard-Implementierung. Beispielsweise können Sie die Ansicht im aktuellen Ordner Inhaltstabelle Einbeziehung die neu empfangene Meldung in **OnNewMessage** aktualisieren. In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), die Methode, die aufgerufen wird, wenn Sie ein Ereignis gesendete Nachricht erhalten, können Sie die gesendete Nachricht in einen Ordner Gesendete Objekte kopieren.
  
Formulare erhalten eine Benachrichtigung über den Viewer eine Änderung auftritt, der das Formular wirkt sich auf, wenn Sie eine neue Nachricht geladen werden. Um ein Formular zu benachrichtigen, rufen Sie eine der Methoden des **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Rufen Sie die **OnChange** Status für die Kommunikation. Wenn das Formular in einem Ordner das letzte Element angezeigt wird, wenn eine neue Nachricht eingeht, rufen Sie **OnChange** beispielsweise mit VCSTATUS_NEXT Flag des Formulars mitgeteilt wird, dass nun eine nächsten Element vorhanden ist. 
  
Rufen Sie **OnActivateNext** , um das Formular über den Eingang einer neuen Nachricht informiert, dass es eventuell oder auch nicht angezeigt werden. Übergeben Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**. 
  
Benachrichtigungen durch ein Form-Objekt an die Clientanwendung werden von der Clientanwendung **IMAPIViewAdviseSink** Schnittstelle behandelt. Weitere Informationen finden Sie unter [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

