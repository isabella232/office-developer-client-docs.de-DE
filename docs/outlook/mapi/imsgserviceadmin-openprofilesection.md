---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317394"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Profil Abschnitt identifiziert. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll. Das übergeben von NULL führt zu einem Zeiger auf die Standardschnittstelle, die im _lppProfSect_ -Parameter zurückgegeben wird. Die Standardschnittstelle für einen Profil Abschnitt ist **IProfSect**.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Zugriff auf den Profil Abschnitt steuern. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe von **OpenProfileSection** , möglicherweise bevor der Profil Abschnitt vollständig für den aufrufenden Client verfügbar ist. Wenn der profile-Abschnitt nicht verfügbar ist, kann durch einen nachfolgenden Aufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Profilabschnitte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch im Besitz einzelner Dienstanbieter.
    
 _lppProfSect_
  
> Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profil Abschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Profil Abschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profil Abschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: OpenProfileSection** -Methode öffnet einen Profil Abschnitt, ein Objekt, das die [IProfSect](iprofsectimapiprop.md) -Schnittstelle unterstützt. Profilabschnitte dienen zum Lesen von Informationen und zum Schreiben von Informationen in das Sitzungsprofil. 
  
 **OpenProfileSection** kann nicht zum Öffnen von Profil Abschnitten verwendet werden, die einzelnen Dienstanbietern gehören, es sei denn, MAPI_FORCE_ACCESS wird verwendet. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profil Abschnitt mit Schreibschutz Berechtigung Öffnen, aber nur ein Client kann einen Profil Abschnitt mit Berechtigung zum Lesen/Schreiben öffnen. Wenn ein anderer Client einen Profil Abschnitt geöffnet hat, den Sie durch Aufrufen von **OpenProfileSection** mit dem MAPI_MODIFY-Flag-Satz öffnen, schlägt der Aufruf fehl, und es wird MAPI_E_NO_ACCESS zurückgegeben. 
  
Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profil Abschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flag und einer nicht vorhandenen [MAPIUID](mapiuid.md) -Struktur im _lpUID_ -Parameter aufrufen. Stellen Sie sicher, dass Sie MAPI_MODIFY angeben. Wenn Sie _lpUID_ so festlegen, dass auf ein nicht vorhandenes **MAPIUID** und **OpenProfileSection** auf den Standardzugriffs Modus schreibgeschützt festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin:: OpenProfileSection** -Methode, um einen Profil Abschnitt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

