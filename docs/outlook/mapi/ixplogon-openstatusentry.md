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
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587019"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Öffnet die Adressbuchhierarchie Status-Objekt.
  
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
  
> [in] Ein Zeiger auf eine Schnittstellenbezeichner (IID) für die Anmeldung Transportobjekt. Übergeben von NULL gibt die [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle zurück. Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Die Standard-Schnittstelle ist schreibgeschützt. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppEntry_
  
> [out] Ein Zeiger auf den Zeiger auf das Statusobjekt geöffnet.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Warteschlange Ruft die **IXPLogon::OpenStatusEntry** -Methode auf, wenn eine Clientanwendung für die Eintrags-ID in der Adressbuchhierarchie Status Tabellenzeile eine **OpenEntry** -Methode aufruft. **OpenStatusEntry** öffnet ein Objekt mit der **IMAPIStatus** -Schnittstelle in bestimmten Transport Anbieter Anmeldung zugeordnet. Dieses Objekt wird dann verwendet, um die Clientanwendungen zum Aufrufen von Methoden (z. B. so konfigurieren Sie die Sitzung neu mithilfe [der SettingsDialog](imapistatus-settingsdialog.md) oder Überprüfen Sie den Status der die Sitzung mithilfe der [ **IMAPIStatus** aktivieren IMAPIStatus::ValidateState](imapistatus-validatestate.md) Methode). 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

