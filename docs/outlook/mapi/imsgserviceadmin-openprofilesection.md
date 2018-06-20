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
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792601"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**Betrifft**: Outlook 
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff. 
  
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
  
> Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die im Profilabschnitt identifiziert. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden. Bei Übergabe von NULL erzeugt einen Zeiger auf die standard-Schnittstelle im Parameter _LppProfSect_ zurückgegeben wird. Die standard-Schnittstelle für einen Profilabschnitt ist **IProfSect**.
    
 _ulFlags_
  
> [in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Benutzerprofildienst-Abschnitt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt an den aufrufenden Client vollständig verfügbar. Wenn im Profilabschnitt nicht verfügbar ist, kann die nachfolgenden Aufrufen es ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. In der Standardeinstellung Profil Abschnitte mit Leseberechtigung geöffnet sind, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Abschnitte Profil, auch die einzelnen Dienstanbieter Besitz.
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, Zugriff auf einen Profil für den Anrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Abschnitt angeforderten Profile ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::OpenProfileSection** -Methode öffnet einen Profilabschnitt, ein Objekt, das die [IProfSect](iprofsectimapiprop.md) -Schnittstelle unterstützt. Profil Abschnitte dienen zum Lesen von Informationen aus und Schreiben von Informationen in das Sitzungsprofil. 
  
 **"OpenProfileSection"** kann nicht verwendet werden, öffnen Sie Profil Abschnitte Besitz einzelne-Dienstanbieter, es sei denn, MAPI_FORCE_ACCESS verwendet wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können mit Leseberechtigung Profile-Abschnitt öffnen, jedoch nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung geöffnet werden. Wenn ein anderer Client einen Profilabschnitt öffnen hat, dass Sie versuchen, die durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY öffnen, schlägt der Aufruf fehl MAPI_E_NO_ACCESS zurückgeben. 
  
Ein Vorgang zum schreibgeschützt öffnen schlägt fehl, wenn im Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY und eine nicht vorhandene [MAPIUID](mapiuid.md) Struktur im _LpUID_ -Parameter. Stellen Sie sicher, dass Sie MAPI_MODIFY angeben. Wenn Sie die _LpUID_ So zeigen Sie auf eine nicht vorhandene **MAPIUID** festgelegt, und Verwenden der Standardzugriffsmodus schreibgeschützten **"OpenProfileSection"** festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |"OpenProfileSection"  <br/> |MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::OpenProfileSection** -Methode, um einen Profilabschnitt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp: IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect: IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

