---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435901"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet das Statusobjekt des Transportanbieters.
  
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
  
> [in] Ein Zeiger auf eine Schnittstellen-ID (Interface Identifier, IID) für das Transportanmeldeobjekt. Durch Übergeben von NULL wird die [IMAPIStatus-Schnittstelle](imapistatusimapiprop.md) zurückgegeben. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Die Standardschnittstelle ist schreibgeschützt. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Statusobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::OpenStatusEntry-Methode** auf, wenn eine Clientanwendung eine **OpenEntry-Methode** für den Eintragsbezeichner in der Statustabelle des Transportanbieters aufruft. **OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus-Schnittstelle,** die dieser bestimmten Transportanbieteranmeldung zugeordnet ist. Dieses Objekt wird dann verwendet, um Clientanwendungen das Aufrufen von **IMAPIStatus-Methoden** zu ermöglichen (z. B. um die Anmeldesitzung mithilfe der [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) neu zu konfigurieren oder den Status der Anmeldesitzung mithilfe der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) zu überprüfen). 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

