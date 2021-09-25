---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 053ead29442c847a0b5a786263845a1dc8a6c6ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556427"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht einen Nachrichtendienst aus einem Profil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parameter

 _lpuid_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu löschenden Nachrichtendienst enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die von  _lpuid_ verwiesen wird, stimmt nicht mit einem vorhandenen Nachrichtendienst überein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::D eleteMsgService-Methode** löscht einen Nachrichtendienst aus einem Profil. **DeleteMsgService** entfernt alle Profilabschnitte im Zusammenhang mit dem Nachrichtendienst. 
  
 **DeleteMsgService** führt die folgenden Schritte aus, um den Nachrichtendienst zu löschen: 
  
1. Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_DELETE festgelegt ist, bevor die Profilabschnitte entfernt werden. Dadurch kann der Dienst alle dienstspezifischen Aufgaben ausführen. 
    
2. Löscht den Nachrichtendienst.
    
3. Löscht den Profilabschnitt des Nachrichtendiensts.
    
Die Einstiegspunktfunktion des Nachrichtendiensts wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die **MAPIUID-Struktur** für den zu löschenden Nachrichtendienst abzurufen, rufen Sie die Eigenschaftsspalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab. Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode](imsgserviceadmin-createmsgservice.md) beschriebenen Prozedur. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::D eleteMsgService-Methode,** um den ausgewählten Dienst zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

