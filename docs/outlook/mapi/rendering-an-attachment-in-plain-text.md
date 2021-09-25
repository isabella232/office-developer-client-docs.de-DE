---
title: Rendern einer Anlage in Nur-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 959716e6067f0eb4fd808c4ccacbd4ffb11db025
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591304"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Rendern einer Anlage in Nur-Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rufen Sie zum Rendern einer Anlage in einer Nachricht mit Nur-Text die **Eigenschaft PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) der Anlage ab, und wenden Sie sie auf die Daten in der **eigenschaft PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) an. Es gibt zwei Möglichkeiten, **PR_RENDERING_POSITION** abzurufen:
  
- Öffnen Sie die Anlage, indem Sie die **IMessage::OpenAttach-Methode** der Nachricht aufrufen, und fragen Sie dann nach der **PR_RENDERING_POSITION-Eigenschaft,** indem Sie die **IMAPIProp::GetProps-Methode** der Anlage aufrufen. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Rufen Sie die **IMessage::GetAttachmentTable-Methode** der Nachricht auf, um auf die Anlagentabelle zuzugreifen und die Spalte abzurufen, die die **PR_RENDERING_POSITION-Eigenschaft** enthält. Auf diese Weise ist immer vorzuziehen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Beachten Sie, dass viele RTF-fähige Nachrichtenspeicher **PR_RENDERING_POSITION** erst berechnen, wenn ein Client die **eigenschaft PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) einer Nachricht anfordert. Bis zu diesem Zeitpunkt stellt **PR_RENDERING_POSITION** in der Regel einen ungefähren Wert dar. Nachrichtenspeicheranbieter dürfen Clients einen ungefähren Wert bereitstellen, um die Leistung zu verbessern. 
  
Das Rendering für eine Datei oder binäre Anlage wird in ihrer **PR_ATTACH_RENDERING-Eigenschaft** gespeichert. Sie haben die Möglichkeit, **PR_ATTACH_RENDERING** auf die gleiche Weise abzurufen, wie Sie **PR_RENDERING_POSITION** abgerufen haben: direkt aus der Anlage oder aus der Anlagentabelle. Für **PR_ATTACH_RENDERING** ist die erste Strategie zwar zeitaufwändig, aber sicherer. Da einige Nachrichtenspeicheranbieter ihre Tabellenspalten auf 255 Byte oder in einigen Fällen auf 510 Bytes abschneiden, ist es schwierig, sicherzustellen, dass die **PR_ATTACH_RENDERING** Spalte das vollständige Rendering enthält. Wenn Sie die Eigenschaft direkt aus der Anlage abrufen, ist sie immer abgeschlossen. 
  
Weder OLE noch Nachrichtenanlagen **sind PR_ATTACH_RENDERING** festgelegt. Stattdessen werden Renderinginformationen für OLE 1-Anlagen im Nachrichtentextstream gespeichert. Für OLE 2-Anlagen wird sie in einem speziellen untergeordneten Datenstrom des Speicherobjekts gespeichert. Das Rendern von Informationen für Nachrichtenanlagen ist über den Formular-Manager verfügbar. 
  
 **So rufen Sie das Rendering für eine Nachrichtenanlage ab**
  
1. Verwenden Sie die Nachrichtenklasse der Nachricht, um auf den Formular-Manager zuzugreifen.
    
2. Greifen Sie auf die **PR_MINI_ICON-Eigenschaft** des Formularmanagers zu. Weitere Informationen finden Sie unter **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

