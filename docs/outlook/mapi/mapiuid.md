---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587166"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Byte-Reihenfolge unabhängige Version einer [GUID](guid.md) -Struktur, die verwendet wird, um einem Dienstanbieter eindeutig zu identifizieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Elemente

 **ab**
  
> Ein Array, das einen 16-Byte-Bezeichner enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **MAPIUID** -Struktur ist eine **GUID** -Struktur in Intel® Prozessor-Byte-Reihenfolge zu platzieren. 
  
MAPI erstellt **MAPIUID** Strukturen in eine Möglichkeit, mit dem zwei verschiedene Elemente, die dieselbe ID äußerst selten kann. **MAPIUID** Strukturen können gespeichert werden, als binäre Eigenschaften oder als Dateien, ohne dabei die Anordnung der Bytes des Computers speichern oder den Zugriff auf die Informationen zu berücksichtigen. 
  
 **MAPIUID** Strukturen verwendet werden: 
  
- Um einen Profilabschnitt zu identifizieren.
    
- In den Eintrag Bezeichner der Nachricht speichern und address Book-Objekten, um den verantwortlich Dienstanbieter zu ermitteln.
    
- In der Eigenschaft **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) von Nachrichten.
    
Um einen **MAPIUID** Bezeichner für eine Suche Schlüssel generiert werden soll, rufen Sie Dienstanbieter [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Wenn ein Client über ein Netzwerk eine Nachricht sendet, sollte ein Protokoll oder Übertragung Format verwendet werden, die nicht die Bytereihenfolge **MAPIUID** Daten geändert wird. 
  
Weitere Informationen dazu, wie **MAPIUID** Strukturen verwendet werden finden Sie unter den folgenden Themen: 
  
[Registrieren der eindeutigen Dienstanbieterbezeichner](registering-service-provider-unique-identifiers.md)
  
[Festlegen der Transportreihenfolge](setting-transport-order.md)
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI-Strukturen](mapi-structures.md)

