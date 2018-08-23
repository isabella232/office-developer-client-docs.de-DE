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
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570912"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verwaltet und bietet Zugriff auf die Eigenschaften von Nachrichtenanlagen. Die **IAttach** -Schnittstelle hat keine eindeutigen Methoden. Weitere Informationen zur Verwendung von Anlagen finden Sie unter [MAPI-Anlagen](mapi-attachments.md) und [Anlagentabellen](attachment-tables.md). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Attachment-Objekte  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAttachment  <br/> |
|Zeigertyp:  <br/> |LPATTACH  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle hat keinen eindeutigen Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

