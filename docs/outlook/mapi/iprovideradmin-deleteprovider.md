---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de399f12e95c94560ad5bd65cdd0a111871f0766
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592256"
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
  
> [in, out] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner enthält, der den zu löschenden Anbieter darstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Anbieter wurde erfolgreich aus dem Nachrichtendienst gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die der  _parameter lpUID_ verweist, wurde nicht erkannt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProviderAdmin::D eleteProvider-Methode** löscht einen Dienstanbieter aus dem Nachrichtendienst. **DeleteProvider** bestimmt den zu löschenden Dienstanbieter, indem die **MAPIUID-Struktur,** auf die von  _lpUID_ verwiesen wird, mit dem Satz von Bezeichnern übereinstimmt, die von den aktiven Dienstanbietern registriert wurden. 
  
Die meisten Nachrichtendienste lassen nicht zu, dass Anbieter gelöscht werden, während das Profil verwendet wird. Wenn der zu löschende Anbieter verwendet wird, markiert **DeleteProvider** ihn für den Löschvorgang, anstatt ihn sofort zu entfernen, und gibt S_OK zurück. Wenn der Anbieter nicht mehr verwendet wird, wird er gelöscht. 
  
 **DeleteProvider** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, bevor der Anbieter aus dem Dienst entfernt wird. Der  _ulContext-Parameter_ wird auf MSG_SERVICE_PROVIDER_DELETE festgelegt. Die Einstiegspunktfunktion für den Nachrichtendienst führt die folgenden Aufgaben aus: 
  
- Löscht den Dienstanbieter.
    
- Löscht den Profilabschnitt des Dienstanbieters.
    
Die Nachrichtendienst-Einstiegspunktfunktion wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

