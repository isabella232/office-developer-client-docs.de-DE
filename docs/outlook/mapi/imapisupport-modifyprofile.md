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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792373"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Betrifft**: Outlook 
  
Ändert eine Nachricht Profilabschnitt permanent gespeichert.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Nachricht gibt an, speichern. Das folgende Flag kann festgelegt werden:
    
MDB_TEMPORARY 
  
> Der Nachrichtenspeicher ist vorübergehend und sollten nicht auf die Nachricht Store-Tabelle hinzugefügt werden. Wenn MDB_TEMPORARY festgelegt ist, gibt **ModifyProfile** sofort S_OK zurück. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Änderungen in den Profilabschnitt waren erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::ModifyProfile** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. E-Mail-Speicher-Anbieter Aufruf **ModifyProfile** auffordern, MAPI, um ihre Profilinformationen zu ändern. 
  
 **ModifyProfile** fügt Abschnitts Profile, die der aufrufende Anbieter zur Liste der installierten Nachricht Store Anbieter Ressourcen zugeordnet ist. Daraufhin wird den Nachrichtenspeicher in der Nachricht Store-Tabelle aufgelistet werden die Clients durch die [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode zur Verfügung steht, und ohne die Anzeige von einem Dialogfeld geöffnet werden soll. 
  
Wenn das Flag MDB_TEMPORARY festgelegt ist, MAPI hat keine Auswirkung, und die Methode gibt sofort mit S_OK zurück.
  
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

