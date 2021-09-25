---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e808f573608a8ba822f0fa8942b2cbfab82b421b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592417"
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die angezeigt werden sollen. Dieser Parameter wird ignoriert, wenn das MAPI_LOGOFF_UI-Flag nicht festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Abmeldevorgang steuern. Die folgenden Flags können festgelegt werden:
    
MAPI_LOGOFF_SHARED 
  
> Wenn diese Sitzung freigegeben ist, sollten alle Clients, die sich mithilfe der freigegebenen Sitzung angemeldet haben, über die anmeldung benachrichtigt werden. Die Clients sollten sich abmelden. Jeder Client, der die freigegebene Sitzung verwendet, kann dieses Flag festlegen. MAPI_LOGOFF_SHARED wird ignoriert, wenn die aktuelle Sitzung nicht freigegeben ist.
    
MAPI_LOGOFF_UI 
  
> **Beim Abmelden** kann während des Vorgangs ein Dialogfeld angezeigt werden, in dem der Benutzer möglicherweise zur Bestätigung aufgefordert wird. 
    
 _ulReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Abmeldevorgang war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::Logoff-Methode** beendet eine MAPI-Sitzung. Wenn **Logoff** zurückgegeben wird, kann keine der Methoden außer [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **Logoff** zurückgegeben wird, geben Sie das Sitzungsobjekt frei, indem Sie seine **IUnknown::Release-Methode** aufrufen. 
  
Weitere Informationen zum Beenden einer Sitzung finden Sie unter [Beenden einer MAPI-Sitzung.](ending-a-mapi-session.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI verwendet die **IMAPISession::Logoff-Methode,** um sich vor der Freigabe von der Sitzung abzumelden.  <br/> |
   
> [!NOTE]
> Aufgrund des in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 und Microsoft Outlook 2013 eingeführten Schnellen Herunterfahrens sollten Clients den **Parameter MAPI_LOGOFF_SHARED** niemals an [IMAPISession::Logoff](imapisession-logoff.md)übergeben. Wenn **MAPI_LOGOFF_SHARED** übergeben wird, beginnen alle MAPI-Clients mit dem Herunterfahren, und es tritt unerwartetes Verhalten auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)

