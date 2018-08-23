---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571199"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) für die Statusobjekt zu öffnen. Übergeben von NULL gibt an, dass der standard-Benutzeroberfläche für das Objekt (in diesem Fall die Schnittstelle [IMAPIStatus](imapistatusimapiprop.md) ) zurückgegeben wird. Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit Leseberechtigung erstellt und Clientanwendungen sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Objekts geöffnet.
    
 _lppEntry_
  
> [out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachricht-Anbieter implementiert die **IMSLogon::OpenStatusEntry** -Methode, um ein Statusobjekt zu öffnen. Dieser Statusobjekt wird dann verwendet, damit Clients [IMAPIStatus](imapistatusimapiprop.md) Methoden aufrufen können. Beispielsweise können Clients [die SettingsDialog](imapistatus-settingsdialog.md) verwenden, konfigurieren Sie die Nachricht Store-Sitzung oder die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode, um den Status der Nachricht Store Anmeldung Sitzung zu überprüfen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

