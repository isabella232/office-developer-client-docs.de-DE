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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422761"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger zurück, der Zugriff auf ein Anbieterverwaltungsobjekt bietet.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu verwaltenden Nachrichtendienst enthält. 
    
 _ulFlags_
  
> [in] Immer NULL. 
    
 _lppProviderAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Anbieterverwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt für die Anbieterverwaltung wurde erfolgreich zurückgegeben.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die  _von lpUID_ verwiesen wird, ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::AdminProviders-Methode** bietet Zugriff auf ein Anbieterverwaltungsobjekt. Eine Anbieterverwaltung ist ein Objekt, das die [IProviderAdmin-Schnittstelle](iprovideradminiunknown.md) unterstützt und Clients folgendes ermöglicht: 
  
- Hinzufügen von Dienstanbietern zu einem Nachrichtendienst.
    
- Löschen von Dienstanbietern aus einem Nachrichtendienst.
    
- Öffnen Sie Profilabschnitte.
    
- Greifen Sie auf die Tabelle des Nachrichtendienstanbieters zu.
    
Die Arten von Änderungen, die tatsächlich an einem Nachrichtendienst vorgenommen werden können, während das Profil verwendet wird, hängen vom Nachrichtendienst ab. Die meisten Nachrichtendienste unterstützen jedoch keine Änderungen, z. B. das Hinzufügen und Löschen von Anbietern, während das Profil verwendet wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die **MAPIUID-Struktur** für den zu verwaltenden Nachrichtendienst abzurufen, rufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaftsspalte aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab. Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode beschriebenen](imsgserviceadmin-createmsgservice.md) Prozedur. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::AdminProviders-Methode,** um ein Anbieterverwaltungsobjekt für einen Dienst zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

