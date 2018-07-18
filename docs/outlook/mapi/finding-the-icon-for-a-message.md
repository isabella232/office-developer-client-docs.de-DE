---
title: Suchen nach dem Symbol für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791672"
---
# <a name="finding-the-icon-for-a-message"></a>Suchen nach dem Symbol für eine Nachricht

  
  
**Betrifft**: Outlook 
  
 **Nach dem Symbol einer Nachricht**
  
1. Rufen Sie die Nachricht [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Rufen Sie [MAPIOpenFormMgr](mapiopenformmgr.md) zum Abrufen eines **IMAPIFormMgr** Schnittstelle Zeigers. Der Parameter _pSession_ übergeben Sie Zeigerposition **IMAPISession** . 
    
3. Rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) zum Abrufen eines **IMAPIFormInfo** Schnittstelle Zeigers. 
    
4. Verwenden Sie den Zeiger **IMAPIFormInfo** [IMAPIProp::GetProps](imapiprop-getprops.md) aufrufen und Abrufen der **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaften. 
    

