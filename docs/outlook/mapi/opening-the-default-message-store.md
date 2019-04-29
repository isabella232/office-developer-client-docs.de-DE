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
  
In einer bestimmten Sitzung fungiert ein Nachrichtenspeicher als Standardnachrichtenspeicher. Ein Standardnachrichtenspeicher weist die folgenden Merkmale auf:
  
- Die **PR_DEFAULT_STORE** ([pidtagdefaultstore (](pidtagdefaultstore-canonical-property.md))-Eigenschaft ist auf true festgelegt.
    
- Das STATUS_DEFAULT_STORE-Flag wird in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt.
    
- MAPI erstellt automatisch die IPM-Unterstruktur und die Stammordner für Suchergebnisse, allgemeine Ansichten und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird. Weitere Informationen zu diesen Ordnern finden Sie unter " [IPM subtree](ipm-subtree.md) " und " [MAPI Special Folders](mapi-special-folders.md)". 
    
Zum Abrufen der Eintrags-ID für den standardmäßigen Nachrichtenspeicher müssen Sie [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) aufrufen, um die Nachrichtenspeichertabelle zu öffnen und bei einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)eine entsprechende Einschränkung anzuwenden. **HrQueryAllRows** gibt einen Zeilensatz mit der eine Zeile zurück, die den Standardnachrichtenspeicher darstellt. Die an **HrQueryAllRows** übergebene Einschränkung kann eines der folgenden Formen annehmen: 
  
1. Eine **und-** Einschränkung, die eine **SAndRestriction** -Struktur kombiniert: 
    
   - Eine EXISTS-Einschränkung, die eine **SExistRestriction** -Struktur verwendet, um das vorhanden sein der **PR_DEFAULT_STORE** -Eigenschaft zu testen. 
    
   - Eine Eigenschaftseinschränkung, die eine [SPropertyRestriction](spropertyrestriction.md) -Struktur verwendet, um den true-Wert in der **PR_DEFAULT_STORE** -Eigenschaft zu überprüfen. 
    
2. Eine Bitmasken Einschränkung, die eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur zum Anwenden von STATUS_DEFAULT_STORE als Maske für die **PR_RESOURCE_FLAGS** -Eigenschaft verwendet. 
    
## <a name="see-also"></a>Siehe auch

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

