---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: acb42aa4fedf0cdd006553cbeb9a5a5be96f61b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620674"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Statusobjekt.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), damit das Statusobjekt geöffnet wird. Wenn NULL übergeben wird, wird die Standardschnittstelle für das Objekt zurückgegeben (in diesem Fall die [IMAPIStatus-Schnittstelle).](imapistatusimapiprop.md) Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung erstellt, und Clientanwendungen sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicheranbieter implementieren die **IMSLogon::OpenStatusEntry-Methode,** um ein Statusobjekt zu öffnen. Dieses Statusobjekt wird dann verwendet, um Clients das Aufrufen von [IMAPIStatus-Methoden](imapistatusimapiprop.md) zu ermöglichen. Clients können beispielsweise die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) verwenden, um die Anmeldesitzung des Nachrichtenspeichers neu zu konfigurieren, oder die [IMAPIStatus::ValidateState-Methode,](imapistatus-validatestate.md) um den Status der Anmeldesitzung des Nachrichtenspeichers zu überprüfen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

