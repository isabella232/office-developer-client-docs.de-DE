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
ms.openlocfilehash: cb9a2ba72ee9fd9c45aefe9d0797930a4871404a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579284"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Von adressbuchanbietern implementierte implementieren Sie die **OpenStatusEntry** -Methode zum Erteilen des Zugriffs auf ihre Statusobjekt. Alle von adressbuchanbietern implementierte sind erforderlich, um einem Statusobjekt implementiert werden, die mindestens die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode unterstützt. Weitere Informationen finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

