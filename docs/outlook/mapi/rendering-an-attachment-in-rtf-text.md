---
title: Rendern einer Anlage in RTF-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280360"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Rendern einer Anlage in RTF-Text

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rich Text Format (RTF)-fähige Clients können Informationen zur Renderingposition aus RTF-Nachrichten Text abrufen, indem Sie in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht nach der folgenden Escapesequenz suchen:
  
 `\objattph`
  
 **So suchen Sie Informationen zur Darstellung in formatiertem Text**
  
1. Rufen Sie **IMessage::** getattachmentable auf die Anlage Tabelle der Nachricht zugreifen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Erstellen Sie eine Eigenschaftseinschränkung, die die Tabelle auf Zeilen beschränkt, die **PR_RENDERING_POSITION** ungleich-1 aufweisen. Weitere Informationen finden Sie unter **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md)).
    
3. Rufen Sie **IMAPITable:: Restrict** auf, um die Einschränkung zu erzwingen. Weitere Informationen finden Sie unter [IMAPITable:: Restrict](imapitable-restrict.md).
    
4. Rufen Sie **IMAPITable:: sortable** auf, um die Anlagen zu sortieren. Weitere Informationen finden Sie unter [IMAPITable:: sortable](imapitable-sorttable.md).
    
5. Rufen Sie **IMAPITable:: QueryRows** auf, um die entsprechenden Zeilen abzurufen. Weitere Informationen finden Sie unter [IMAPITable:: QueryRows](imapitable-queryrows.md).
    
6. Rufen Sie die **IMAPIProp:: OpenProperty** -Methode der Nachricht auf, um **PR_RTF_COMPRESSED** mit der **IStream** -Schnittstelle abzurufen. Weitere Informationen finden Sie unter [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
    
7. Überprüfen Sie den Stream, und suchen Sie nach `\objattph`dem Render-Platzhalter. Das Zeichen nach diesem Platzhalter ist die Stelle für die nächste Anlage in der sortierten Tabelle.
    

