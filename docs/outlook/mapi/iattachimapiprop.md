---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409090"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet und bietet Zugriff auf die Eigenschaften von Anlagen in Nachrichten. Die **IAttach-Schnittstelle** verfügt über keine eigenen eindeutigen Methoden. Weitere Informationen zur Verwendung von Anlagen finden Sie unter [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Attachment-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Nachrichtenspeichern  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAttachment  <br/> |
|Zeigertyp:  <br/> |LPATTACH  <br/> |
|Transaktionsmodell:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

