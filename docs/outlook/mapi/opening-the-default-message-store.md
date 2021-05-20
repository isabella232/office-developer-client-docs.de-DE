---
title: Öffnen eines Standardnachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436027"
---
# <a name="opening-the-default-message-store"></a>Öffnen eines Standardnachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einer bestimmten Sitzung fungiert ein Nachrichtenspeicher als Standardnachrichtenspeicher. Ein Standardnachrichtenspeicher hat die folgenden Merkmale:
  
- Die **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) -Eigenschaft ist auf TRUE festgelegt.
    
- Das STATUS_DEFAULT_STORE wird in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.
    
- MAPI erstellt automatisch die IPM-Unterstruktur und die Stammordner für Suchergebnisse, allgemeine Ansichten und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird. Weitere Informationen zu diesen Ordnern finden Sie unter [IPM Subtree](ipm-subtree.md) und [MAPI Special Folders](mapi-special-folders.md). 
    
Zum Abrufen der Eintrags-ID für den Standardnachrichtenspeicher müssen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) aufrufen, um die Nachrichtenspeichertabelle zu öffnen und eine entsprechende Einschränkung in einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)anzuwenden. **HrQueryAllRows** gibt einen Zeilensatz mit der zeile zurück, die den Standardnachrichtenspeicher darstellt. Die Einschränkung, die Sie an **HrQueryAllRows übergeben,** kann in einem der folgenden Formen bestehen: 
  
1. Eine **AND-Einschränkung,** die eine **SAndRestriction-Struktur** verwendet, um zu kombinieren: 
    
   - Es gibt eine Einschränkung, die eine **SExistRestriction-Struktur** verwendet, um das Vorhandensein der PR_DEFAULT_STORE **zu** testen. 
    
   - Eine Eigenschaftseinschränkung, die eine [SPropertyRestriction-Struktur](spropertyrestriction.md) verwendet, um den TRUE-Wert in der PR_DEFAULT_STORE **zu** überprüfen. 
    
2. Eine Bitmaskeneinschränkung, die eine [SBitMaskRestriction-Struktur](sbitmaskrestriction.md) zum Anwenden von STATUS_DEFAULT_STORE als Maske auf die PR_RESOURCE_FLAGS **verwendet.** 
    
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

