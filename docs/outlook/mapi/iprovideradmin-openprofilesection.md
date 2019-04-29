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
  
Öffnet einen Profil Abschnitt aus dem aktuellen Profil und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für weiteren Zugriff zurück. 
  
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
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu öffnenden Profil Abschnitt enthält. Clients dürfen keinen NULL-Wert für den _lpUID_ -Parameter übergeben. Dienstanbieter können NULL zum Abrufen der **MAPIUID** -Funktion, wenn Sie über Ihre Message-Dienst-Einstiegspunkt-Funktionen aufrufen. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll. Übergeben von NULL Ergebnisse in der Profil Abschnitt Standardschnittstelle (**IProfSect**) wird zurückgegeben. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Art des Öffnens des Profil Abschnitts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht es **OpenProfileSection** , erfolgreich zurückzugeben, möglicherweise, bevor der Profil Abschnitt vollständig für den Aufrufer verfügbar ist. Wenn der profile-Abschnitt nicht verfügbar ist, kann durch einen nachfolgenden Aufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde. Clients dürfen keine Lese-/Schreibzugriff auf Anbieter Abschnitte des Profils haben.
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch im Besitz einzelner Dienstanbieter.
    
 _lppProfSect_
  
> Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profil Abschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profil Abschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profil Abschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IProviderAdmin:: OpenProfileSection** -Methode wird ein Profil Abschnitt geöffnet, in dem der Aufrufer Informationen lesen und möglicherweise Informationen in das aktive Profil schreiben kann. 
  
Clients können Profilabschnitte, die zu Anbietern gehören, nicht mithilfe der **OpenProfileSection** -Methode öffnen. 
  
Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profil Abschnitt mit Leseberechtigung öffnen. Wenn jedoch ein Profil Abschnitt mit Lese-/Schreibzugriff geöffnet ist, können keine weiteren Aufrufe zum Öffnen des Abschnitts ausgeführt werden, unabhängig von der Art des Zugriffs. Wenn ein Profil Abschnitt mit schreibgeschützter Berechtigung geöffnet ist, schlägt ein nachfolgendes Aufrufen der Berechtigung Lese-/Schreibzugriff mit MAPI_E_NO_ACCESS fehl. Wenn ein Abschnitt mit Lese-/Schreibzugriff-Berechtigung geöffnet ist, tritt ebenfalls ein Fehler bei einem nachfolgenden Aufruf der Berechtigung Read-Only auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie anfordern, dass **OpenProfileSection** einen nicht vorhandenen Profil Abschnitt öffnet, indem Sie MAPI_MODIFY in _ulFlags_ und eine unbekannte **MAPIUID** in _lpUID_übergeben, wird der profile-Abschnitt erstellt. 
  
Wenn Sie **OpenProfileSection** einen nicht vorhandenen Abschnitt mit Schreibschutz Berechtigung öffnen möchten, wird MAPI_E_NOT_FOUND zurückgegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI verwendet die **IProviderAdmin:: OpenProfileSection** -Methode, um einen Profil Abschnitt aus dem aktuellen Profil zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

