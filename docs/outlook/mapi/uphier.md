---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414921"
---
# <a name="uphier"></a>UPHIER
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren einer Ordnerhierarchie während des [Uploadhierarchiestatus](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
> [in] Flags zum Ändern des Verhaltens beim Synchronisieren der Ordnerhierarchie.
    
  - UPH_OK
    
    - [in] Hochladen war erfolgreich. Der Client legt dies nach dem erfolgreichen Hochladen von Informationen auf den Server fest. Wenn dieses Flag angezeigt wird, Outlook alle internen Buchhaltungsinformationen, die angegeben haben, dass die Ordnerhierarchie aktualisiert werden muss. 
    
    - Der Client übergibt das HRESULT, wenn der Upload nicht erfolgreich war.
    
_pstmReserved_
  
> [out] Dieses Mitglied ist für die Outlook reserviert und wird nicht unterstützt.
    
_iEnt_
  
> [out] Index zum Nachverfolgen der Synchronisierung der durch *cEnt angegebenen Ordneranzahl.* 
    
_cEnt_
  
> [out] Die Anzahl der Ordner, die nicht synchronisiert sind.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

