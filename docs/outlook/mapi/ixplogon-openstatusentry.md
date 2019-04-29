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
  
Öffnet das Status-Objekt des Transportanbieters.
  
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
  
> in Ein Zeiger auf einen Schnittstellenbezeichner (IID) für das Transport Anmeldeobjekt. Durch das Übergeben von NULL wird die [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle zurückgegeben. Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Die Standardschnittstelle ist schreibgeschützt. 
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> Out Ein Zeiger auf den Zeiger auf das geöffnete Status-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange ruft die **IXPLogon:: OpenStatusEntry** -Methode auf, wenn eine **** Clientanwendung eine OpenEntry-Methode für die Eintrags-ID in der Statustabellen Zeile des Transportanbieters aufruft. **OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus** -Schnittstelle, die dieser bestimmten Transportanbieter Anmeldung zugeordnet ist. Dieses Objekt wird dann verwendet, um Clientanwendungen das Aufrufen von **IMAPIStatus** -Methoden (beispielsweise zum erneuten Konfigurieren der Anmeldesitzung mithilfe der [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode oder zum Überprüfen des Status der Anmeldesitzung mithilfe der [ IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode). 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

