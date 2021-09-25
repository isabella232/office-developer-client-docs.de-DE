---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1082e3680ed9a53894c5fd810be91b42eac22cee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596456"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet das Statusobjekt des Anbieters.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Statusobjekt verwendet werden muss. Wenn NULL übergeben wird, wird die Standardschnittstelle des Objekts zurückgegeben, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschütztem Zugriff geöffnet, und Aufrufer sollten nicht davon ausgehen, dass die Lese-/Schreibberechtigung erteilt wurde.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und das Statusobjekt wurde geöffnet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Adressbuchanbieter implementieren die **OpenStatusEntry-Methode,** um Zugriff auf ihr Statusobjekt zu gewähren. Alle Adressbuchanbieter müssen ein Statusobjekt implementieren, das mindestens die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) unterstützt. Weitere Informationen finden Sie unter [Status Object Implementation](status-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

