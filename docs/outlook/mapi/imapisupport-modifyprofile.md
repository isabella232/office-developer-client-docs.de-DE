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
  
Änderungen an einem Abschnitt des Nachrichtenspeicher Profils bleiben permanent.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ des Nachrichtenspeichers angibt. Das folgende Flag kann festgelegt werden:
    
MDB_TEMPORARY 
  
> Der Nachrichtenspeicher ist temporär und sollte nicht der Nachrichtenspeichertabelle hinzugefügt werden. Wenn MDB_TEMPORARY festgelegt ist, gibt **MODIFYPROFILE** S_OK sofort zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Änderungen am Profil Abschnitt waren erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: ModifyProfile** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter rufen **ModifyProfile** auf, um MAPI aufzufordern, Ihre Profilinformationen zu ändern. 
  
 **ModifyProfile** fügt den dem anrufenden Anbieter zugeordneten Profil Abschnitt der Liste der installierten Ressourcen des Nachrichtenspeicher Anbieters hinzu. Dies führt dazu, dass der Nachrichtenspeicher in der Nachrichtenspeichertabelle aufgeführt wird, die Clients über die [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zur Verfügung steht, und die geöffnet werden soll, ohne dass ein Dialogfeld angezeigt wird. 
  
Wenn das MDB_TEMPORARY-Flag festgelegt ist, bewirkt MAPI nichts, und die Methode gibt sofort mit S_OK zurück.
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

