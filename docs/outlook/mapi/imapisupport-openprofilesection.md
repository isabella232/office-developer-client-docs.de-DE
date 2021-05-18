---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411386"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parameter

 _lpUid_
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den zu öffnenden Profilabschnitt identifiziert. Wenn Sie NULL für den  _lpUid-Parameter übergeben,_ wird der Profilabschnitt des Anrufers geöffnet. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Profilabschnitt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openProfileSection,** erfolgreich zurückzukehren, möglicherweise bevor der Profilabschnitt vollständig für den Aufrufer zugänglich ist. Wenn auf den Profilabschnitt nicht zugegriffen werden kann, kann ein nachfolgender Objektaufruf zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lppProfileObj_
  
> [out] Ein Zeiger auf einen Zeiger auf den geöffneten Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profilabschnitt zu ändern oder auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der in  _lpEntryID_ übergebenen Eintrags-ID ist kein Profilabschnitt zugeordnet.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Reservierte oder nicht unterstützte Flags wurden verwendet, und daher wurde der Vorgang nicht abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenProfileSection-Methode** wird für alle Supportobjekte implementiert. Dienstanbieter und Nachrichtendienste rufen **OpenProfileSection auf,** um einen Profilabschnitt zu öffnen und einen Zeiger auf die **IProfSect-Schnittstellenimplementierung** abzurufen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenProfileSection** öffnet Profilabschnitte als schreibgeschützt, es sei denn, Sie legen das MAPI_MODIFY im  _ulFlags-Parameter_ ein, und Ihre Berechtigung ist ausreichend. Das Festlegen dieses Kennzeichens garantiert keine Lese-/Schreibberechtigung. Die Ihnen erteilten Berechtigungen hängen von Ihrer Zugriffsebene und dem Objekt ab. 
  
Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt als schreibgeschützt zu öffnen, wird MAPI_E_NOT_FOUND. Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt als Lese-/Schreibzugriff zu öffnen, wird der Profilabschnitt erstellt und der **IProfSect-Zeiger** zurückgegeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

