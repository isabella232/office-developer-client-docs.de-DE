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
ms.openlocfilehash: a5446ce30812b30b193e87484a7322d9ddf7d781
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572711"
---
# <a name="special-folders-in-message-stores"></a>Spezialordner im Nachrichtenspeicher

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [MAPI-Spezialordner](mapi-special-folders.md).
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeicher](implementing-folders-in-message-stores.md)

