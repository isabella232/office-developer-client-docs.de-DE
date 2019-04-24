---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279549"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht einen Dienstanbieter aus dem Nachrichtendienst.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in, out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner enthält, der den zu löschenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde erfolgreich aus dem Nachrichtendienst gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** , auf die durch den _lpUID_ -Parameter verwiesen wurde, wurde nicht erkannt. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IProviderAdmin::D eleteprovider** -Methode wird ein Dienstanbieter aus dem Nachrichtendienst gelöscht. **DeleteProvider** bestimmt den zu löschenden Dienstanbieter, indem er der **MAPIUID** -Struktur entspricht, auf die durch _lpUID_ mit den von den aktiven Dienstanbietern registrierten Bezeichnern verwiesen wird. 
  
Bei den meisten Nachrichtendiensten können Anbieter nicht gelöscht werden, während das Profil verwendet wird. Wenn der zu löschende Anbieter verwendet wird, markiert **DeleteProvider** ihn zum Löschen, statt ihn sofort zu entfernen und S_OK zurückgeben. Wenn der Anbieter nicht mehr verwendet wird, wird er gelöscht. 
  
 **DeleteProvider** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, bevor der Anbieter aus dem Dienst entfernt wird. Der Parameter _ulContext_ ist auf MSG_SERVICE_PROVIDER_DELETE festgelegt. Die Nachrichtendienst-Einstiegspunktfunktion führt die folgenden Aufgaben aus: 
  
- Löscht den Dienstanbieter.
    
- Löscht den Profil Abschnitt des Dienstanbieters.
    
Die Nachrichtendienst-Einstiegspunktfunktion wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

