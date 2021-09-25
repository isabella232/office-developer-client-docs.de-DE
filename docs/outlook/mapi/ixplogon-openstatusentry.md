---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a471b66709d2109bfd3894eed80168ea1b8d5140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571556"
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
  
> [in] Ein Zeiger auf einen Schnittstellenbezeichner (INTERFACE Identifier, IID) für das Transportanmeldeobjekt. Wenn NULL übergeben wird, wird die [IMAPIStatus-Schnittstelle zurückgegeben.](imapistatusimapiprop.md) Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Die Standardschnittstelle ist schreibgeschützt. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Statusobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPLogon::OpenStatusEntry-Methode** auf, wenn eine Clientanwendung eine **OpenEntry-Methode** für den Eintragsbezeichner in der Statustabellenzeile des Transportanbieters aufruft. **OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus-Schnittstelle,** die dieser bestimmten Transportanbieteranmeldung zugeordnet ist. Dieses Objekt wird dann verwendet, um Clientanwendungen das Aufrufen von **IMAPIStatus-Methoden** zu ermöglichen (z. B. zum Neukonfigurieren der Anmeldesitzung mithilfe der [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) oder zum Überprüfen des Status der Anmeldesitzung mithilfe der [IMAPIStatus::ValidateState-Methode).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

