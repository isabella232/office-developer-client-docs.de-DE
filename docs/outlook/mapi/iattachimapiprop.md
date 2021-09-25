---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c67ce8be8cd1389a985f8762759a0136c5f81c1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580041"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet und bietet Zugriff auf die Eigenschaften von Anlagen in Nachrichten. Die **IAttach-Schnittstelle** verfügt über keine eigenen eindeutigen Methoden. Weitere Informationen zur Verwendung von Anlagen finden Sie unter [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Attachment-Objekte  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicheranbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAttachment  <br/> |
|Zeigertyp:  <br/> |LPATTACH  <br/> |
|Transaktionsmodell:  <br/> |Transaktiven  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

