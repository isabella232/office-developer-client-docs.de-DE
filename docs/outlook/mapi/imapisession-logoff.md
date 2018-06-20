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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792305"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Betrifft**: Outlook 
  
MAPI-Sitzung beendet.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, angezeigt werden soll. Dieser Parameter wird ignoriert, wenn das Flag MAPI_LOGOFF_UI nicht festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Vorgang zum Abmelden steuern. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_LOGOFF_SHARED 
  
> Wenn dieser Sitzung freigegeben ist, sollte die Abmeldung alle Clients, die mithilfe der freigegebenen Sitzung angemeldeten benachrichtigt werden. Die Clients sollten melden Sie sich ab. Jeder Client, der die freigegebene Sitzung verwendet wird, kann dieses Kennzeichen festgelegt. MAPI_LOGOFF_SHARED wird ignoriert, wenn die aktuelle Sitzung nicht freigegeben ist.
    
MAPI_LOGOFF_UI 
  
> **Abmelden** können während des Vorgangs ein Dialogfeld anzeigen möglicherweise der Benutzer zur Bestätigung aufgefordert wird. 
    
 _ulReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Vorgang zum Abmelden war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::Logoff** -Methode wird eine MAPI-Sitzung beendet. Wenn **Abmelden** zurückgegeben wird, kann keine der Methoden außer [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) aufgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **Abmelden** zurückgibt, release Session-Objekt durch die **IUnknown** -Methode aufrufen. 
  
Weitere Informationen zum Beenden einer Sitzung finden Sie unter [Beenden einer MAPI-Sitzung](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::Logoff** -Methode aus der Sitzung vor einer Freigabe abmelden.  <br/> |
   
> [!NOTE]
> Aufgrund der Verhalten für Schnelles Herunterfahren in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 und Microsoft Outlook 2013 eingeführt sollten Clients nie Parameters **MAPI_LOGOFF_SHARED** [IMAPISession::Logoff](imapisession-logoff.md)übergeben. Übergeben von **MAPI_LOGOFF_SHARED** bewirkt, dass alle MAPI-Clients zum Herunterfahren beginnen und unerwartetes Verhalten tritt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)

