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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405660"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Profilabschnitt aus dem aktuellen Profil und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück. 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu öffnenden Profilabschnitt enthält. Clients dürfen null nicht für den  _lpUID-Parameter_ übergeben. Dienstanbieter können NULL übergeben, um **die MAPIUID abzurufen,** wenn sie von ihren Nachrichtendienst-Einstiegspunktfunktionen aufrufen. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle (**IProfSect**) des Profilabschnitts zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Profilabschnitt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProfileSection,** erfolgreich zurückzukehren, möglicherweise bevor der Profilabschnitt vollständig für den Aufrufer verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler zur Folge haben. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden. Clients sind für Anbieterabschnitte des Profils keine Lese-/Schreibberechtigungen zulässig.
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch die, die im Besitz einzelner Dienstanbieter sind.
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profilabschnitt zu ändern oder auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profilabschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::OpenProfileSection-Methode** öffnet einen Profilabschnitt, mit dem der Aufrufer Informationen aus dem aktiven Profil lesen und möglicherweise in das aktive Profil schreiben kann. 
  
Clients können keine Profilabschnitte öffnen, die zu Anbietern gehören, indem sie die **OpenProfileSection-Methode** verwenden. 
  
Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen. Wenn ein Profilabschnitt jedoch mit Lese-/Schreibberechtigung geöffnet ist, können keine weiteren Aufrufe zum Öffnen des Abschnitts vorgenommen werden, unabhängig von der Art des Zugriffs. Wenn ein Profilabschnitt mit schreibgeschützter Berechtigung geöffnet ist, wird bei einem nachfolgenden Aufruf der Lese-/Schreibberechtigung ein Fehler MAPI_E_NO_ACCESS. Wenn ein Abschnitt mit Lese-/Schreibberechtigung geöffnet ist, kann auch ein nachfolgender Aufruf zum Anfordern von schreibgeschützter Berechtigung fehlschlagen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie anfordern, dass **OpenProfileSection** einen nicht vorhandenen Profilabschnitt öffnet, indem MAPI_MODIFY in  _ulFlags_ und eine unbekannte **MAPIUID** in  _lpUID_ übergeben wird, wird der Profilabschnitt erstellt. 
  
Wenn Sie anfordern, **dass OpenProfileSection** einen nicht vorhandenen Abschnitt mit schreibgeschützter Berechtigung öffnet, wird MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI verwendet die **IProviderAdmin::OpenProfileSection-Methode,** um einen Profilabschnitt aus dem aktuellen Profil zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

