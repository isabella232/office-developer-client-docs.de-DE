---
title: Öffnen die Standard-Informationsspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0366e889f1c63e5fe40760ca80cec701cd6b3713
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573537"
---
# <a name="opening-the-default-message-store"></a>Öffnen die Standard-Informationsspeicher

**Betrifft**: Outlook 2013 | Outlook 2016 
  
In einer bestimmten Sitzung verhält sich eine Nachrichtenspeicher als Standard-Informationsspeicher. Ein Standardnachrichtenspeicher weist folgende Merkmale auf:
  
- Die **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))-Eigenschaft ist auf TRUE festgelegt.
    
- Das Flag STATUS_DEFAULT_STORE ist in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.
    
- MAPI erstellt automatisch IPM-Unterstruktur und den Stammordner für Suchergebnisse, allgemeine und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird. Weitere Informationen zu diesen Ordnern finden Sie unter [IPM-Unterstruktur](ipm-subtree.md) und [MAPI-Spezialordner](mapi-special-folders.md). 
    
Um die Eintrags-ID für den standardmäßigen Nachrichtenspeicher abzurufen, müssen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) zum Öffnen Sie die Nachricht Store Tabelle und anwenden eine angemessene Einschränkung in einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)aufrufen. **HrQueryAllRows** gibt ein Rowset mit der eine Zeile, die Standard-Informationsspeicher darstellt, zurück. Die Einschränkung, die an **HrQueryAllRows** übergeben kann eine der folgenden Formen annehmen: 
  
1. Eine **AND** -Einschränkung, die eine **SAndRestriction** Struktur verwendet, um zu kombinieren: 
    
   - Eine Einschränkung, die eine **SExistRestriction** -Struktur So testen Sie das Vorhandensein der **PR_DEFAULT_STORE** -Eigenschaft verwendet vorhanden. 
    
   - Eine eigenschaftseinschränkung, die eine [SPropertyRestriction](spropertyrestriction.md) -Struktur zum Überprüfen der Wert "TRUE" in der **PR_DEFAULT_STORE** -Eigenschaft verwendet. 
    
2. Eine Bitmaske Einschränkung, die eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur für die Anwendung STATUS_DEFAULT_STORE als Maske gegen die **PR_RESOURCE_FLAGS** -Eigenschaft verwendet. 
    
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

