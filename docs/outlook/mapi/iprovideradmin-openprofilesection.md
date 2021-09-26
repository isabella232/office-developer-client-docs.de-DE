---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21cfb68a187743dc8db14c198eff03ca9bba5618
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620548"
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu öffnenden Profilabschnitt enthält. Clients dürfen für den  _lpUID-Parameter_ keinen NULL-Wert übergeben. Dienstanbieter können NULL übergeben, um die **MAPIUID** abzurufen, wenn sie von ihren Nachrichtendienst-Einstiegspunktfunktionen aufrufen. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle des Profilabschnitts (**IProfSect**) zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Profilabschnitt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt für den Aufrufer vollständig verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschützter Berechtigung geöffnet, und Aufrufer sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibberechtigung erteilt wurde. Clients ist die Lese-/Schreibberechtigung für Anbieterabschnitte des Profils nicht zulässig.
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch diejenigen, die im Besitz einzelner Dienstanbieter sind.
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profilabschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profilabschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IProviderAdmin::OpenProfileSection-Methode** öffnet einen Profilabschnitt, in dem der Aufrufer Informationen aus dem aktiven Profil lesen und möglicherweise in dieses schreiben kann. 
  
Clients können profilabschnitte, die zu Anbietern gehören, nicht mithilfe der **OpenProfileSection-Methode** öffnen. 
  
Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen. Wenn ein Profilabschnitt jedoch mit Lese-/Schreibberechtigung geöffnet ist, können keine weiteren Aufrufe zum Öffnen des Abschnitts ausgeführt werden, unabhängig vom Zugriffstyp. Wenn ein Profilabschnitt mit schreibgeschützter Berechtigung geöffnet ist, schlägt ein nachfolgender Aufruf der Lese-/Schreibberechtigung mit MAPI_E_NO_ACCESS fehl. Wenn ein Abschnitt mit Lese-/Schreibberechtigung geöffnet ist, schlägt auch ein nachfolgender Aufruf zum Anfordern der schreibgeschützten Berechtigung fehl. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie anfordern, dass **OpenProfileSection** einen nicht vorhandenen Profilabschnitt öffnet, indem Sie MAPI_MODIFY in  _ulFlags_ und eine unbekannte **MAPIUID** in  _lpUID_ übergeben, wird der Profilabschnitt erstellt. 
  
Wenn Sie anfordern, dass **OpenProfileSection** einen nicht vorhandenen Abschnitt mit schreibgeschützter Berechtigung öffnet, wird MAPI_E_NOT_FOUND zurückgegeben. 
  
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

