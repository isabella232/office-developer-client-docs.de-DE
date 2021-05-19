---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338108"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet eine MAPI-Sitzung.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller anzuzeigenden Dialogfelder oder Fenster. Dieser Parameter wird ignoriert, wenn MAPI_LOGOFF_UI nicht festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Abmeldevorgang steuern. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_LOGOFF_SHARED 
  
> Wenn diese Sitzung freigegeben wird, sollten alle Clients, die sich über die freigegebene Sitzung angemeldet haben, über die derzeit ausgeführte Abmeldeung benachrichtigt werden. Die Clients sollten sich abmelden. Jeder Client, der die freigegebene Sitzung verwendet, kann dieses Flag festlegen. MAPI_LOGOFF_SHARED wird ignoriert, wenn die aktuelle Sitzung nicht freigegeben wird.
    
MAPI_LOGOFF_UI 
  
> **Beim Abmelden** kann während des Vorgangs ein Dialogfeld angezeigt werden, in dem der Benutzer möglicherweise zur Bestätigung aufgefordert wird. 
    
 _ulReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Abmeldevorgang war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::Logoff-Methode** beendet eine MAPI-Sitzung. Wenn **Logoff zurückgegeben** wird, kann keine der Methoden mit Ausnahme von [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **Logoff zurückgegeben** wird, lassen Sie das Sitzungsobjekt los, indem Sie die **IUnknown::Release-Methode** aufrufen. 
  
Weitere Informationen zum Beenden einer Sitzung finden Sie unter [Ending a MAPI Session](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI verwendet die **IMAPISession::Logoff-Methode,** um sich vor der Veröffentlichung von der Sitzung abmelden.  <br/> |
   
> [!NOTE]
> Aufgrund des schnellen Herunterfahrens, das in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 und Microsoft Outlook 2013 eingeführt wurde, sollten Clients den **parameter MAPI_LOGOFF_SHARED** niemals an [IMAPISession::Logoff](imapisession-logoff.md)übergeben. Durch **MAPI_LOGOFF_SHARED** werden alle MAPI-Clients mit dem Herunterfahren begonnen, und es tritt unerwartetes Verhalten auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)

