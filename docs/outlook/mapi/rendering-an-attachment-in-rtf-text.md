---
title: Rendern einer Anlage in RTF-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90e8c40833570927f488a053c7682af19bde9480
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609648"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Rendern einer Anlage in RTF-Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
RTF-fähige Clients (Rich Text Format) können Renderingpositionsinformationen aus RTF-Nachrichtentext abrufen, indem sie in der **Eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) der Nachricht nach der folgenden Escapesequenz suchen:
  
 `\objattph`
  
 **So suchen Sie Renderinginformationen in formatiertem Text**
  
1. Rufen Sie **IMessage::GetAttachmentTable** auf, um auf die Anlagentabelle der Nachricht zuzugreifen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Erstellen Sie eine Eigenschaftseinschränkung, die die Tabelle auf Zeilen beschränkt, deren **PR_RENDERING_POSITION** nicht gleich -1 ist. Weitere Informationen finden Sie unter **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Rufen Sie **IMAPITable::Restrict** auf, um die Einschränkung zu erzwingen. Weitere Informationen finden Sie unter [IMAPITable::Restrict](imapitable-restrict.md).
    
4. Rufen Sie **IMAPITable::SortTable** auf, um die Anlagen zu sortieren. Weitere Informationen finden Sie unter [IMAPITable::SortTable](imapitable-sorttable.md).
    
5. Rufen Sie **IMAPITable::QueryRows** auf, um die entsprechenden Zeilen abzurufen. Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Rufen Sie die **IMAPIProp::OpenProperty-Methode** der Nachricht auf, um **PR_RTF_COMPRESSED** mit der **IStream-Schnittstelle** abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
    
7. Scannen Sie den Datenstrom, und suchen Sie nach dem  `\objattph` Renderingplatzhalter. Das Zeichen, das auf diesen Platzhalter folgt, ist die Stelle für die nächste Anlage in der sortierten Tabelle.
    

