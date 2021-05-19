---
title: Rendern einer Anlage in Nur-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410875"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Rendern einer Anlage in Nur-Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine Anlage in einer Nachricht mit Nur-Text zu rendern, rufen Sie die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft der Anlage ab, und wenden Sie sie auf die Daten in der **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))-Eigenschaft an. Es gibt zwei Möglichkeiten zum Abrufen **PR_RENDERING_POSITION:**
  
- Öffnen Sie die Anlage, indem Sie die **IMessage::OpenAttach-Methode** der Nachricht aufrufen und dann nach der **PR_RENDERING_POSITION-Eigenschaft** fragen, indem Sie die **IMAPIProp::GetProps-Methode** der Anlage aufrufen. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Rufen Sie die **IMessage::GetAttachmentTable-Methode** der Nachricht auf, um auf die Anlagentabelle zu zugreifen und die Spalte abzurufen, die die PR_RENDERING_POSITION **enthält.** Diese Methode ist immer vorzuziehen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Beachten Sie, dass viele #A0 erst  dann PR_RENDERING_POSITION berechnet werden, wenn ein Client die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft einer Nachricht anfordert. Bis zu diesem Zeitpunkt **stellt PR_RENDERING_POSITION** in der Regel einen ungefähren Wert dar. Anbieter von Nachrichtenspeichern dürfen Clients einen ungefähren Wert zur Verbesserung der Leistung zur Verfügung stellen. 
  
Das Rendering für eine Datei oder binäre Anlage wird in der PR_ATTACH_RENDERING **gespeichert.** Sie haben die Wahl, PR_ATTACH_RENDERING Wie Sie PR_RENDERING_POSITION **:** direkt aus der Anlage oder aus der Anlagentabelle abgerufen haben.  Für **PR_ATTACH_RENDERING** ist die erste Strategie zwar zeitaufwändiger, aber sicherer. Da einige Nachrichtenspeicheranbieter ihre Tabellenspalten auf 255 Byte oder in einigen Fällen auf 510 Byte kürzen, ist es schwierig sicherzustellen, dass die **spalte PR_ATTACH_RENDERING** das vollständige Rendering enthält. Wenn Sie die Eigenschaft direkt aus der Anlage abrufen, ist sie immer vollständig. 
  
Weder OLE noch Nachrichtenanlagen werden **PR_ATTACH_RENDERING.** Stattdessen werden Renderinginformationen für OLE 1-Anlagen im Nachrichtentextdatenstrom gespeichert. Für OLE 2-Anlagen wird sie in einem speziellen untergeordneten Datenstrom des Speicherobjekts gespeichert. Renderinginformationen für Nachrichtenanlagen sind über den Formular-Manager verfügbar. 
  
 **So rufen Sie das Rendering für eine Nachrichtenanlage ab**
  
1. Verwenden Sie die Nachrichtenklasse der Nachricht, um auf den Formular-Manager zu zugreifen.
    
2. Greifen Sie auf die PR_MINI_ICON des **Formular-Managers** zu. Weitere Informationen finden Sie unter **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

