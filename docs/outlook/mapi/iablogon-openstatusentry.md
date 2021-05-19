---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410784"
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Statusobjekt verwendet werden muss. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützten Zugriffen geöffnet, und Anrufer sollten nicht davon ausgehen, dass Lese-/Schreibberechtigungen erteilt wurden.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf ist erfolgreich, und das Statusobjekt wurde geöffnet.
    
## <a name="remarks"></a>Hinweise

Adressbuchanbieter implementieren die **OpenStatusEntry-Methode,** um Zugriff auf ihr Statusobjekt zu gewähren. Alle Adressbuchanbieter müssen ein Statusobjekt implementieren, das mindestens die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) unterstützt. Weitere Informationen finden Sie unter [Status Object Implementation](status-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

