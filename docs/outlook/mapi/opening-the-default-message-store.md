---
title: Öffnen eines Standardnachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0b9a1fd73701c663d0477a2e2ebe1a445c5eb54e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555937"
---
# <a name="opening-the-default-message-store"></a>Öffnen eines Standardnachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einer bestimmten Sitzung fungiert ein Nachrichtenspeicher als Standardnachrichtenspeicher. Ein Standardnachrichtenspeicher weist die folgenden Merkmale auf:
  
- Die **eigenschaft PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) ist auf TRUE festgelegt.
    
- Das STATUS_DEFAULT_STORE Flag wird in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.
    
- MAPI erstellt automatisch die IPM-Unterstruktur und die Stammordner für Suchergebnisse, allgemeine Ansichten und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird. Weitere Informationen zu diesen Ordnern finden Sie unter [IPM-Unterstruktur](ipm-subtree.md) und [MAPI-Spezialordner.](mapi-special-folders.md) 
    
Um den Eintragsbezeichner für den Standardnachrichtenspeicher abzurufen, müssen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) aufrufen, um die Nachrichtenspeichertabelle zu öffnen und eine entsprechende Einschränkung in einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)anzuwenden. **HrQueryAllRows** gibt eine Zeile zurück, die mit der zeile festgelegt ist, die den Standardnachrichtenspeicher darstellt. Die Einschränkung, die Sie an **HrQueryAllRows** übergeben, kann eine der folgenden Formen annehmen: 
  
1. Eine **AND-Einschränkung,** die eine **SAndRestriction-Struktur** zum Kombinieren verwendet: 
    
   - Eine vorhandene Einschränkung, die eine **SExistRestriction-Struktur** verwendet, um das Vorhandensein der **PR_DEFAULT_STORE-Eigenschaft** zu testen. 
    
   - Eine Eigenschaftseinschränkung, die eine [SPropertyRestriction-Struktur](spropertyrestriction.md) verwendet, um den TRUE-Wert in der **PR_DEFAULT_STORE-Eigenschaft** zu überprüfen. 
    
2. Eine Bitmaskeneinschränkung, die eine [SBitMaskRestriction-Struktur](sbitmaskrestriction.md) zum Anwenden von STATUS_DEFAULT_STORE als Maske für die **PR_RESOURCE_FLAGS-Eigenschaft** verwendet. 
    
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

