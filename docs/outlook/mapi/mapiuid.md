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
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432205"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine unabhängige Bytereihenfolge einer [GUID-Struktur,](guid.md) die zum eindeutigen Identifizieren eines Dienstanbieters verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Elemente

 **ab**
  
> Ein Array, das einen 16-Byte-Bezeichner enthält.
    
## <a name="remarks"></a>Hinweise

Eine **MAPIUID-Struktur** ist eine **GUID-Struktur,** die in intel® Prozessor-Bytereihenfolge geordnet ist. 
  
MAPI erstellt **MAPIUID-Strukturen** so, dass es sehr selten ist, dass zwei unterschiedliche Elemente denselben Bezeichner haben. **MAPIUID-Strukturen** können als binäre Eigenschaften oder als Dateien gespeichert werden, unabhängig von der Bytereihenfolge des Computers, der die Informationen speichert oder auf diese zu zugegriffen hat. 
  
 **Es werden MAPIUID-Strukturen** verwendet: 
  
- So identifizieren Sie einen Profilabschnitt.
    
- In den Eintragsbezeichnern von Nachrichtenspeicher- und Adressbuchobjekten, um den zuständigen Dienstanbieter zu identifizieren.
    
- In der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft von Nachrichten.
    
Zum Generieren eines **MAPIUID-Bezeichners** für einen Suchschlüssel rufen Dienstanbieter [IMAPISupport::NewUID auf.](imapisupport-newuid.md)
  
Wenn ein Client eine Nachricht über ein Netzwerk überträgt, sollte er ein Protokoll- oder Übertragungsformat verwenden, das die Bytereihenfolge von **MAPIUID-Daten nicht** ändert. 
  
Weitere Informationen zur Verwendung von **MAPIUID-Strukturen** finden Sie in den folgenden Themen: 
  
[Registrieren eindeutiger Bezeichner des Dienstanbieters](registering-service-provider-unique-identifiers.md)
  
[Festlegen der Transportreihenfolge](setting-transport-order.md)
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI-Strukturen](mapi-structures.md)

