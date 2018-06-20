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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792765"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Betrifft**: Outlook 
  
Löscht einen Dienstanbieter aus der Nachrichtendienst.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in, out] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner, der den enthält zu löschenden-Anbieter darstellt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Anbieter wurde aus dem Nachrichtendienst gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** auf den durch den Parameter _LpUID_ verwiesen wurde nicht erkannt. 
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::DeleteProvider** -Methode löscht einen Dienstanbieter aus den Dienst. **DeleteProvider** bestimmt den Dienstanbieter zu löschen, indem Sie die **MAPIUID** -Struktur, die auf den _LpUID_ mit den IDs durch die aktiv-Dienstanbieter registriert. 
  
Die meisten Message-Dienste können nicht Anbieter gelöscht werden, während das Profil verwendet wird. Wenn der Anbieter löschen verwendet wird, **DeleteProvider** es zum Löschen, anstatt sie zu entfernen sofort markiert und gibt S_OK zurück. Wenn der Anbieter nicht mehr verwendet wird, wird es gelöscht. 
  
 **DeleteProvider** Ruft die Messagingdiensts Eintrag Point-Funktion, bevor der Anbieter aus dem Dienst entfernt wird. Der Parameter _UlContext_ wird auf MSG_SERVICE_PROVIDER_DELETE festgelegt. Die Nachricht Service Eintrag-Funktion werden die folgenden Aufgaben ausgeführt: 
  
- Löscht den Dienstanbieter.
    
- Löscht den Dienstanbieter Profilabschnitt.
    
Die Nachricht Service Eintrag-Funktion wird nicht erneut aufgerufen, nachdem der Anbieter gelöscht wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin: IUnknown](iprovideradminiunknown.md)

