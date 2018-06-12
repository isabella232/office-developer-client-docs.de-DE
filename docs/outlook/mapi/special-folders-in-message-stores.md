---
title: Spezialordner im Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 013e62e06e100296a5fc702b68348bb74eb718e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795596"
---
# <a name="special-folders-in-message-stores"></a>Spezialordner im Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [MAPI-Spezialordner](mapi-special-folders.md).
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeicher](implementing-folders-in-message-stores.md)

