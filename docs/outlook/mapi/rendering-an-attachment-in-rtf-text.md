---
title: Darstellen einer Anlage als RTF-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795365"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Darstellen einer Anlage als RTF-Text

  
  
**Betrifft**: Outlook 
  
Rich-Text-Format (RTF)-Clients unterstützen können Positionsinformationen Rendering von RTF des Nachrichtentexts anhand der folgenden Escapezeichen in der Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft abrufen:
  
 `\objattph`
  
 **Zum Suchen von Rendering-Informationen in formatierten text**
  
1. Rufen Sie **IMessage::GetAttachmentTable** Zugriff auf die Nachricht Anlage-Tabelle. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Erstellen Sie eine eigenschaftseinschränkung, die die Tabelle, um Zeilen beschränkt, die nicht gleich-1 **PR_RENDERING_POSITION** aufweisen. Weitere Informationen finden Sie unter **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Rufen Sie die **Methode IMAPITable:: Restrict** , um die Einschränkung zu erzwingen. Weitere Informationen finden Sie unter [Methode IMAPITable:: Restrict](imapitable-restrict.md).
    
4. Rufen Sie **SortTable** , um die Anlagen zu sortieren. Weitere Informationen finden Sie unter [SortTable](imapitable-sorttable.md).
    
5. Rufen Sie **IMAPITable::QueryRows** zum Abrufen der entsprechenden Zeilen. Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Rufen Sie die Nachricht **IMAPIProp::OpenProperty** -Methode zum Abrufen von **PR_RTF_COMPRESSED** mit der **IStream** -Schnittstelle. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.
    
7. Überprüfung den Stream, suchen Sie nach der Platzhalter Rendering `\objattph`. Das Zeichen nach dieser Platzhalter ist der Ort für die neue Anlage in der sortierten Tabelle.
    

