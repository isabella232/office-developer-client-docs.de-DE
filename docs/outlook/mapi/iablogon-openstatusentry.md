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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791970"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Betrifft**: Outlook 
  
Öffnet den Anbieter Status-Objekt.
  
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
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle darstellt, die den Zugriff auf die Statusobjekt verwendet werden muss. Übergeben NULL zurückgegeben Standardschnittstelle für das Objekt, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet und Anrufer sollte nicht davon ausgehen, dass die Lese-Schreib-Berechtigung gewährt wurde.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und das Statusobjekt geöffnet wurde.
    
## <a name="remarks"></a>Bemerkungen

Von adressbuchanbietern implementierte implementieren Sie die **OpenStatusEntry** -Methode zum Erteilen des Zugriffs auf ihre Statusobjekt. Alle von adressbuchanbietern implementierte sind erforderlich, um einem Statusobjekt implementiert werden, die mindestens die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode unterstützt. Weitere Informationen finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

