---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97383721fd1c9c2d8481f8c9b6fde37768555af6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630677"
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
  
> [in] Eine Bitmaske mit Flags, die den Typ des Nachrichtenspeichers angibt. Das folgende Kennzeichen kann festgelegt werden:
    
MDB_TEMPORARY 
  
> Der Nachrichtenspeicher ist temporär und sollte nicht der Nachrichtenspeichertabelle hinzugefügt werden. Wenn MDB_TEMPORARY festgelegt ist, gibt **ModifyProfile** sofort S_OK zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Änderungen am Profilabschnitt waren erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::ModifyProfile-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ModifyProfile** auf, um die MAPI aufzufordern, ihre Profilinformationen zu ändern. 
  
 **ModifyProfile** fügt den Profilabschnitt, der dem aufrufenden Anbieter zugeordnet ist, zur Liste der installierten Nachrichtenspeicheranbieterressourcen hinzu. Dadurch wird der Nachrichtenspeicher in der Nachrichtenspeichertabelle aufgeführt, die Clients über die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) zur Verfügung steht, und ohne Anzeige eines Dialogfelds geöffnet werden. 
  
Wenn das MDB_TEMPORARY-Flag festgelegt ist, führt MAPI keine Aktion aus, und die Methode wird sofort mit S_OK zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

