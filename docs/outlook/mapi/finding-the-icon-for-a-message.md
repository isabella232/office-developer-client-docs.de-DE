---
title: Suchen des Symbols für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409153"
---
# <a name="finding-the-icon-for-a-message"></a>Suchen des Symbols für eine Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So suchen Sie das Symbol, das einer Nachricht zugeordnet ist**
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) der Nachricht auf, um die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) abzurufen.
    
2. Rufen [Sie MAPIOpenFormMgr auf,](mapiopenformmgr.md) um einen **IMAPIFormMgr-Schnittstellenzeiger** abzurufen. Übergeben Sie den **IMAPISession-Zeiger** im _pSession-Parameter._ 
    
3. Rufen [Sie IMAPIFormMgr::ResolveMessageClass auf,](imapiformmgr-resolvemessageclass.md) um einen **IMAPIFormInfo-Schnittstellenzeiger** abzurufen. 
    
4. Verwenden Sie den **IMAPIFormInfo-Zeiger,** um [IMAPIProp::GetProps](imapiprop-getprops.md) aufrufen und die **Eigenschaften PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) abzurufen. 
    

