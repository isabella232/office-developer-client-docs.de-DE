---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419989"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nimmt Änderungen an einem Nachrichtenspeicherprofilabschnitt dauerhaft vor.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ des Nachrichtenspeichers angibt. Das folgende Flag kann festgelegt werden:
    
MDB_TEMPORARY 
  
> Der Nachrichtenspeicher ist temporär und sollte nicht der Nachrichtenspeichertabelle hinzugefügt werden. Wenn MDB_TEMPORARY festgelegt ist, gibt **ModifyProfile** S_OK zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Änderungen am Profilabschnitt waren erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::ModifyProfile-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ModifyProfile auf,** um MAPI zum Ändern ihrer Profilinformationen aufforderen. 
  
 **ModifyProfile** fügt den Profilabschnitt, der dem aufrufenden Anbieter zugeordnet ist, zur Liste der installierten Ressourcen des Nachrichtenspeicheranbieters hinzu. Dies bewirkt, dass der Nachrichtenspeicher in der Nachrichtenspeichertabelle aufgeführt wird, die Clients über die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) zur Verfügung steht, und ohne die Anzeige eines Dialogfelds geöffnet wird. 
  
Wenn das MDB_TEMPORARY festgelegt ist, führt MAPI nichts aus, und die Methode gibt sofort mit S_OK.
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

