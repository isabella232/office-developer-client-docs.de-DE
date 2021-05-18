---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411414"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013-Lösungen herauszufinden, ob eine Anlage als unsicher gilt und zum Anzeigen und Indizierung gesperrt ist.
  
|||
|:-----|:-----|
|Schnittstellenbezeichner:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Überprüft, ob eine angegebene Anlage von Outlook 2010 oder Outlook 2013 zur Anzeige und Indizierung blockiert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Outlook 2010- und Outlook 2013-Lösungen können diese Schnittstelle abfragen, um zu sehen, ob eine Anlage blockiert ist. Die von Outlook 2010 oder Outlook 2013 blockierten Anlagen hängen davon ab, wie Outlook 2010 oder Outlook 2013 konfiguriert wurde und welche Richtlinien ein Administrator angewendet hat.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)
  
[Überprüfen, ob eine Anlage blockiert ist](how-to-verify-an-attachment-is-blocked.md)

