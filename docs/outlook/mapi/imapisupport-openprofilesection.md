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
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parameter

 _lpUid_
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den zu öffnenden Profil Abschnitt identifiziert. Durch das Übergeben von NULL für den Parameter _lpUid_ wird der Profil Abschnitt des Anrufers geöffnet. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Art des Öffnens des Profil Abschnitts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht es **OpenProfileSection** , erfolgreich zurückzugeben, möglicherweise bevor der Profil Abschnitt vollständig für den Aufrufer zugänglich ist. Wenn der Profil Abschnitt nicht zugänglich ist, kann durch einen nachfolgenden Objektaufruf zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde. 
    
 _lppProfileObj_
  
> Out Ein Zeiger auf einen Zeiger auf den geöffneten Profil Abschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profil Abschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profil Abschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der Eintrags-ID, die in _lpEntryID_übergeben wurde, ist kein Profil Abschnitt zugeordnet.
    
MAPI_E_UNKNOWN_FLAGS 
  
> ReServierte oder nicht unterstützte Flags wurden verwendet, daher wurde der Vorgang nicht abgeschlossen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: OpenProfileSection** -Methode wird für alle Support-Objekte implementiert. Dienstanbieter und Nachrichtendienste rufen **OpenProfileSection** auf, um einen Profil Abschnitt zu öffnen und einen Zeiger auf die **IProfSect** -Schnittstellenimplementierung abzurufen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenProfileSection** öffnet Profilabschnitte als schreibgeschützt, es sei denn, Sie legen das MAPI_MODIFY-Flag im _ulFlags_ -Parameter fest, und ihre Berechtigung genügt. Das Festlegen dieses Kennzeichens garantiert keine Lese-/Schreibzugriff; die Berechtigungen, die Ihnen erteilt werden, hängen von ihrer Zugriffsebene und dem Objekt ab. 
  
Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profil Abschnitt als schreibgeschützt zu öffnen, wird MAPI_E_NOT_FOUND zurückgegeben. Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profil Abschnitt als Lese-/Schreibzugriff zu öffnen, erstellt er den profile-Abschnitt und gibt den **IProfSect** -Zeiger zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

