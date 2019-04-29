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
  
Öffnet das Status-Objekt des Anbieters.
  
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
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Status-Objekt verwendet werden muss. Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)zurückgegeben.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz geöffnet, und Aufrufer sollten nicht davon ausgehen, dass Lese-/Schreibzugriff erteilt wurde.
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und das Status-Objekt wurde geöffnet.
    
## <a name="remarks"></a>Bemerkungen

Adressbuchanbieter implementieren die **OpenStatusEntry** -Methode, um Zugriff auf Ihr Status-Objekt zu gewähren. Alle Adressbuchanbieter müssen ein Status-Objekt implementieren, das mindestens die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode unterstützt. Weitere Informationen finden Sie unter [Implementierung von Status Objekten](status-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

