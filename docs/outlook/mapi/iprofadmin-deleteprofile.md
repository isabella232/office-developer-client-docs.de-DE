---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792767"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Betrifft**: Outlook 
  
Löscht ein Profil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des Profils, das gelöscht werden.
    
 _ulFlags_
  
> [in] Immer NULL. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Profil wurde gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Das angegebene Profil ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin::DeleteProfile** -Methode löscht ein Profil. Wenn das zu löschende Profil verwendet wird, wenn **DeleteProfile** aufgerufen wird, **DeleteProfile** gibt S_OK zurück, jedoch wird das Profil nicht sofort gelöscht. Stattdessen **DeleteProfile** das Profil zum Löschen markiert und, nachdem es nicht mehr verwendet wird, wenn alle seine aktiven Sitzungen beendet haben, wird gelöscht. 
  
Die Funktion Eintrag für jeden Nachrichtendienst im Profil wird mit den im Parameter _UlContext_ festgelegten MSG_SERVICE_DELETE Wert aufgerufen. Zunächst die Funktion löscht den Dienst, und löscht dann den Dienst Profilabschnitt. Die Nachricht Service Eintrag-Funktion wird nicht erneut aufgerufen, nachdem der Dienst gelöscht wurde. 
  
Zum Löschen eines Profils ist kein Kennwort erforderlich.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI (engl.) wird die **IProfAdmin::DeleteProfile** -Methode verwendet, um das ausgewählte Profil zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

