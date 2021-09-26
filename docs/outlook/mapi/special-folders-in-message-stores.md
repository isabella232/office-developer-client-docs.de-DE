---
title: Spezialordner im Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 453aaa842b9b69d5eaf502f85cd5b3c2b655b673
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591073"
---
# <a name="special-folders-in-message-stores"></a>Spezialordner im Nachrichtenspeicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [MAPI-Spezialordner](mapi-special-folders.md).
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Ordnern in Nachrichtenspeichern](implementing-folders-in-message-stores.md)

