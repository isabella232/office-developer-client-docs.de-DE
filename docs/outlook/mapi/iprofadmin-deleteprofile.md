---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83bae85596603dc5ef2700cd008b2b44e2fde08a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587881"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht ein Profil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des zu löschenden Profils.
    
 _ulFlags_
  
> [in] Immer NULL. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Profil wurde erfolgreich gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProfAdmin::D eleteProfile-Methode** löscht ein Profil. Wenn das zu löschende Profil beim Aufrufen von **DeleteProfile** verwendet wird, gibt **DeleteProfile** S_OK zurück, löscht das Profil jedoch nicht sofort. Stattdessen markiert **DeleteProfile** das Profil zum Löschen und löscht es, nachdem es nicht mehr verwendet wird, wenn alle aktiven Sitzungen beendet wurden. 
  
Die Einstiegspunktfunktion für jeden Nachrichtendienst im Profil wird mit dem im  _ulContext-Parameter_ festgelegten MSG_SERVICE_DELETE Wert aufgerufen. Zuerst löscht die Funktion den Dienst und dann den Profilabschnitt des Diensts. Die Nachrichtendienst-Einstiegspunktfunktion wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde. 
  
Zum Löschen eines Profils ist kein Kennwort erforderlich.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI verwendet die **IProfAdmin::D eleteProfile-Methode,** um das ausgewählte Profil zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

