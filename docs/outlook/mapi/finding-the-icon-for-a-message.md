---
title: Suchen des Symbols für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2016332f5347aeda46d65b03e87cc69f9f359867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614199"
---
# <a name="finding-the-icon-for-a-message"></a>Suchen des Symbols für eine Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So suchen Sie das symbol, das einer Nachricht zugeordnet ist**
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) der Nachricht auf, um die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft abzurufen.
    
2. Rufen Sie [MAPIOpenFormMgr](mapiopenformmgr.md) auf, um einen **IMAPIFormMgr-Schnittstellenzeiger** abzurufen. Übergeben Sie den **IMAPISession-Zeiger** im _Parameter "pSession"._ 
    
3. Rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) auf, um einen **IMAPIFormInfo-Schnittstellenzeiger** abzurufen. 
    
4. Verwenden Sie den **IMAPIFormInfo-Zeiger,** um [IMAPIProp::GetProps](imapiprop-getprops.md) aufzurufen und die **Eigenschaften PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) abzurufen. 
    

