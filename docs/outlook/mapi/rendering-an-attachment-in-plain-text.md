---
title: Rendern einer Anlage im nur-Text-Format
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
# <a name="rendering-an-attachment-in-plain-text"></a>Rendern einer Anlage im nur-Text-Format

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie eine Anlage in einer Nachricht mit nur-Text rendern möchten, rufen Sie die **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft der Anlage ab, und wenden Sie Sie auf die Daten im **PR_ATTACH_RENDERING** ([pidtagattachrendering (](pidtagattachrendering-canonical-property.md)) an. Eigenschaft. Es gibt zwei Möglichkeiten zum Abrufen von **PR_RENDERING_POSITION**:
  
- Öffnen Sie die Anlage durch Aufrufen der **IMessage:: openattach** -Methode der Nachricht, und Fragen Sie dann nach der **PR_RENDERING_POSITION** -Eigenschaft, indem Sie die **IMAPIProp::** GetProps-Methode der Anlage aufrufen. Weitere Informationen finden Sie unter [IMessage:: openattach](imessage-openattach.md) und [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
- Rufen Sie die **IMessage:: GetAttachment** Table-Methode der Nachricht auf, und rufen Sie die Spalte ab, die die **PR_RENDERING_POSITION** -Eigenschaft enthält. Diese Methode ist immer vorzuziehen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Beachten Sie, dass viele RTF-fähige Nachrichtenspeicher **PR_RENDERING_POSITION** erst berechnen, wenn ein Client die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft einer Nachricht anfordert. Bis zu diesem Zeitpunkt stellt **PR_RENDERING_POSITION** in der Regel einen Näherungswert dar. Nachrichtenspeicher Anbieter können Clients einen Näherungswert liefern, um die Leistung zu verbessern. 
  
Das Rendering für eine Datei oder eine binäre Anlage wird in der **PR_ATTACH_RENDERING** -Eigenschaft gespeichert. Sie können **PR_ATTACH_RENDERING** auf die gleiche Weise abrufen wie **PR_RENDERING_POSITION**: direkt aus der Anlage oder aus der Attachment-Tabelle. Für **PR_ATTACH_RENDERING**ist die erste Strategie, wenngleich zeitaufwändiger, sicherer. Da einige Nachrichtenspeicher Anbieter ihre Tabellenspalten auf 255 Byte oder in einigen Fällen 510 Byte abschneiden, ist es schwierig, sicherzustellen, dass die **PR_ATTACH_RENDERING** -Spalte das vollständige RENDERING enthält. Wenn Sie die Eigenschaft direkt aus der Anlage abrufen, ist Sie immer vollständig. 
  
Weder OLE noch Nachrichtenanlagen legen **PR_ATTACH_RENDERING**fest. Stattdessen werden Informationen zum Rendern von OLE 1-Anlagen im Nachrichtentextdaten Strom gespeichert. Bei OLE 2-Anlagen wird es in einem speziellen untergeordneten Stream des Storage-Objekts gespeichert. Renderinginformationen für Nachrichtenanlagen stehen über den Formular-Manager zur Verfügung. 
  
 **So rufen Sie das Rendering für eine Nachrichtenanlage ab**
  
1. Verwenden Sie die Nachrichtenklasse der Nachricht, um auf den Formular-Manager zuzugreifen.
    
2. Zugreifen auf die **PR_MINI_ICON** -Eigenschaft des Formular-Managers. Weitere Informationen finden Sie unter **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md)).
    

