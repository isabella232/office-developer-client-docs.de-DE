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
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413178"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Status-Objekt.
  
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
  
> in Ein Zeiger auf den Schnittstellenbezeichner (IID) für das zu öffnende Status-Objekt. Übergeben von NULL gibt an, dass die Standardschnittstelle für das Objekt zurückgegeben wird (in diesem Fall die [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle). Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Statusobjekt geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz Berechtigung erstellt, und Clientanwendungen sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde. 
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppEntry_
  
> Out Ein Zeiger auf den Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher Anbieter implementieren die **IMSLogon:: OpenStatusEntry** -Methode, um ein Status-Objekt zu öffnen. Dieses Status-Objekt wird dann verwendet, um Clients das Aufrufen von [IMAPIStatus](imapistatusimapiprop.md) -Methoden zu ermöglichen. Clients können beispielsweise die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode verwenden, um die Anmeldesitzung des Nachrichtenspeichers oder die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode neu zu konfigurieren, um den Status der Nachrichtenspeicher-Anmeldesitzung zu überprüfen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

