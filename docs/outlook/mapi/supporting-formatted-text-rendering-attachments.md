---
title: Unterst�tzen formatierter Text Rendern von Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b6339d768ac476c24ce988ba761270a50d47464
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580313"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Unterst�tzen formatierter Text: Rendern von Anlagen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Clientanwendung, die interessiert, in dem in einer Nachricht ihre Anhänge gerendert werden, werden die **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft für diese Anlagen beim Verfassen festgelegt. Ein Client, der Rendering Platzierung nicht k�mmern bewirkt, dass diese Eigenschaft nicht festgelegt ist.
  
Wenn ein Client eine Nachricht mit Anlagen ge�ffnet wird, wird versucht, Abrufen aller Anlagen **PR_RENDERING_POSITION** -Eigenschaft, um zu bestimmen, in denen im Nachrichtentext die Anlage gerendert werden soll. Ein Client kann eine der folgenden Methoden zum Abrufen von **PR_RENDERING_POSITION**verwenden:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) on the open attachment to retrieve the **PR_RENDERING_POSITION** property. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) on the open message to retrieve its attachment table. **PR_RENDERING_POSITION** is a required column in all attachment tables. This is the preferred method because it results in better performance. 
    
RTF-f�higen Nachrichtenspeicher k�nnen ausw�hlen, ob einen genauen oder ungef�hren Wert f�r **PR_RENDERING_POSITION**zur�ck. Da Nachrichtenspeicher eine Anlage **PR_RENDERING_POSITION** Wert, wenn Sie aufgefordert werden f�r die Nachricht **PR_BODY** -Eigenschaft neu zu berechnen, speichert einige RTF-f�higen Nachricht nur Garantie die Genauigkeit von Rendering positioniert, wenn ein Client zun�chst f�r **PR_BODY**auffordert. RTF-f�higen Nachrichtenspeicher d�rfen Rendering ungef�hre Positionswerte zur Leistungssteigerung Clients bereitzustellen. Bietet eine ungef�hre, sondern eine genaue Renderingposition sparen Sie Zeit und ist in den meisten F�llen ausreichend. 
  
RTF-f�higen Nachrichtenspeicher sollte ihre Ann�herung der Werte, die durch den Client verantwortlich f�r die Erstellung der Anlage basieren soll. Obwohl alle Clients **PR_RENDERING_POSITION**festgelegt werden soll, sollten Nachricht-Anbieter f�r den Umgang mit der M�glichkeit, seine Abwesenheit vorbereitet sein. Wenn der Client nicht **PR_RENDERING_POSITION**festgelegt wird, kann ein Nachrichtenspeicher auf-1 festlegen um anzugeben, dass die Renderingposition nicht innerhalb des Nachrichtentexts befindet. Anlagen mit einer Renderingposition von-1 k�nnen an einer beliebigen Stelle innerhalb der Nachricht je nach dem Client angezeigt werden. Viele Clients positionieren Sie diese Typen von Anlagen am oberen Rand der Nachricht.
  
Der Grad der Genauigkeit für eine **PR_RENDERING_POSITION** -Eigenschaft hängt davon ab, unabhängig davon, ob ein Nachrichtenspeichers einer Nachricht **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und Eigenschaften **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) speichert oder nur **PR_RTF_COMPRESSED**. Wenn der Client **PR_BODY** generiert und der Nachrichtenspeicher ihn mit der formatierte Text speichert, werden die Endposition Rendering exakt sein. Wenn der Nachrichtenspeicher, da sie nur **PR_RTF_COMPRESSED**speichert eine eigene Version der **PR_BODY** generieren muss, ist es jedoch wahrscheinlich die Positionen Rendering etwas unrichtige ist. Dies ist aufgrund der auf unterschiedliche Weise, dass Clients und Anbieter Nachricht die **PR_BODY** -Eigenschaft generieren. 
  
To calculate an accurate **PR_RENDERING_POSITION** value, an RTF-aware store uses a tag embedded in the formatted text. The utility function **RTFSync** can be called to perform this calculation and update an attachment's rendering position. Depending on the amount of state information available, the message store can pass either RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED, or both values to [RTFSync](rtfsync.md).
  

