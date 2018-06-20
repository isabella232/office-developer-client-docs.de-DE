---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792597"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Betrifft**: Outlook 
  
Gibt einen Zeiger, der Zugriff auf ein Anbieter Administration-Objekt bietet.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst zu verwaltenden enthält. 
    
 _ulFlags_
  
> [in] Immer NULL. 
    
 _lppProviderAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Anbieter Administration-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Anbieter Verwaltungsobjekt wurde erfolgreich zurückgegeben.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** auf den _LpUID_ ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::AdminProviders** -Methode ermöglicht den Zugriff auf ein Anbieter Administration-Objekt. Eine Anbieter Verwaltung ist ein Objekt, das die [IProviderAdmin](iprovideradminiunknown.md) -Schnittstelle unterstützt und ermöglicht es Clients, die folgenden Schritte aus: 
  
- Fügen Sie eine Message Service-Dienstanbieter hinzu.
    
- Dienstanbieter aus einem Nachrichtendienst zu löschen.
    
- Profil Abschnitte zu öffnen.
    
- Zugriff auf die Tabelle Nachricht-Dienstanbieter.
    
Die Arten von Änderungen, die mit einer Messagingdiensts tatsächlich hergestellt werden können, während das Profil verwendet wird, hängt von den Dienst. Die meisten Message Dienste unterstützen nicht jedoch Änderungen wie hinzufügen und Löschen von Anbietern, während das Profil verwendet wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Abrufen der **MAPIUID** -Struktur für den Dienst zu verwalten, Abrufen die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Nachrichtendienst Zeile in der Tabelle der Dienste. Weitere Informationen finden Sie unter dem Verfahren in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI (engl.) wird die **IMsgServiceAdmin::AdminProviders** -Methode verwendet, um einen Anbieter Administration-Objekt für einen Dienst zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IProviderAdmin: IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

