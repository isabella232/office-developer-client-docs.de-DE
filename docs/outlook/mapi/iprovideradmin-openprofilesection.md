---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 276a2bd84156e9b396df71f51130e6704ad7c7fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792784"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Betrifft**: Outlook 
  
Öffnet einen Profilabschnitt aus dem aktuellen Profil, und gibt einen [IProfSect](iprofsectimapiprop.md) Zeiger für den weiteren Zugriff. 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Profilabschnitt geöffnet werden enthält. Clients müssen nicht NULL für den _LpUID_ -Parameter übergeben. Dienstanbieter können NULL, um die **MAPIUID** abzurufen, beim Aufruf aus ihrer Nachricht Service Entry Point Funktionen übergeben. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden. Bei Übergabe von NULL erzeugt Profilabschnitt Standardschnittstelle (**IProfSect**) zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie im Profilabschnitt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **"OpenProfileSection"** erfolgreich, möglicherweise beendet, vor dem Profilabschnitt vollständig mit dem Anrufer verfügbar ist. Wenn im Profilabschnitt nicht verfügbar ist, kann die nachfolgenden Aufrufen es ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. Clients sind Lese-/Schreibberechtigung für Anbieter von Abschnitten des Profils nicht zulässig.
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Abschnitte Profil, auch die einzelnen Dienstanbieter Besitz.
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen Profilabschnitt schreibgeschützt ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Abschnitt angeforderten Profile ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::OpenProfileSection** -Methode öffnet einen Profilabschnitt, aktivieren den Anrufer zum Lesen von Informationen aus und Schreiben Sie möglicherweise Informationen in das aktive Profil. 
  
Clients können keine Profil Abschnitte öffnen, zu die Anbieter mithilfe der Methode **"OpenProfileSection"** gehören. 
  
Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profilabschnitt mit Leseberechtigung öffnen. Wenn ein Profilabschnitt mit Lese-/Schreibzugriff geöffnet ist, können jedoch keine anderen Aufrufe vorgenommen werden, den Abschnitt, unabhängig von der Art von Access zu öffnen. Wenn ein Profilabschnitt mit Leseberechtigung geöffnet ist, wird ein nachfolgender Aufruf von Lese-/Schreibberechtigung für anfordern mit MAPI_E_NO_ACCESS fehl. Wenn ein Abschnitt mit Lese-/Schreibzugriff geöffnet ist, wird ein nachfolgender Aufruf Leseberechtigung anfordern auch fehl. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie, die anfordern **"OpenProfileSection"** öffnen Sie einen nicht vorhandenen Profilabschnitt, indem Sie in _UlFlags_ MAPI_MODIFY übergeben, und eine unbekannte **MAPIUID** in _LpUID_, Profilabschnitt erstellt werden. 
  
Wenn Sie anfordern, dass **"OpenProfileSection"** einen nicht vorhandenen Abschnitt mit Lesezugriff zu öffnen, wird die MAPI_E_NOT_FOUND zurückgegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |"OpenProfileSection"  <br/> |MFCMAPI (engl.) verwendet die **IProviderAdmin::OpenProfileSection** -Methode, um einen Profilabschnitt aus dem aktuellen Profil zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp: IUnknown](imapipropiunknown.md)
  
[IProfSect: IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin: IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

