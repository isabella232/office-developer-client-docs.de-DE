---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f20f891df60495407609653831e2442c9167dec2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592466"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013 Lösungen herauszufinden, ob eine Anlage als unsicher eingestuft und für die Anzeige und Indizierung blockiert wird.
  
|||
|:-----|:-----|
|Schnittstellenbezeichner:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Überprüft, ob eine angegebene Anlage von Outlook 2010 oder Outlook 2013 zum Anzeigen und Indizieren blockiert wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Outlook 2010- und Outlook 2013-Lösungen können diese Schnittstelle abfragen, um festzustellen, ob eine Anlage blockiert ist. Die Anlagen, die von Outlook 2010 oder Outlook 2013 blockiert werden, variieren je nachdem, wie Outlook 2010 oder Outlook 2013 konfiguriert wurde und welche Richtlinien ein Administrator angewendet hat.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)
  
[Überprüfen, ob eine Anlage blockiert ist](how-to-verify-an-attachment-is-blocked.md)

