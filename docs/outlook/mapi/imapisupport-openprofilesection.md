---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cf4f3954b529dd40fe3b273f0bc469766645da33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592389"
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) der den zu öffnenden Profilabschnitt identifiziert. Wird NULL für den  _Parameter lpUid übergeben,_ wird der Profilabschnitt des Aufrufers geöffnet. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Profilabschnitt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Aufrufer vollständig auf den Profilabschnitt zugegriffen werden kann. Wenn auf den Profilabschnitt nicht zugegriffen werden kann, kann ein nachfolgender Objektaufruf zu einem Fehler führen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte schreibgeschützt geöffnet, und Aufrufer sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibberechtigung erteilt wurde. 
    
 _lppProfileObj_
  
> [out] Ein Zeiger auf einen Zeiger auf den geöffneten Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen schreibgeschützten Profilabschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Dem in  _lpEntryID übergebenen_ Eintragsbezeichner ist kein Profilabschnitt zugeordnet.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Reservierte oder nicht unterstützte Flags wurden verwendet, weshalb der Vorgang nicht abgeschlossen wurde.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::OpenProfileSection-Methode** wird für alle Unterstützungsobjekte implementiert. Dienstanbieter und Nachrichtendienste rufen **OpenProfileSection** auf, um einen Profilabschnitt zu öffnen und einen Zeiger auf die **IProfSect-Schnittstellenimplementierung** abzurufen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **OpenProfileSection** öffnet Profilabschnitte schreibgeschützt, es sei denn, Sie legen das flag MAPI_MODIFY im  _UlFlags-Parameter_ fest, und Ihre Berechtigung ist ausreichend. Das Festlegen dieses Flags garantiert nicht die Lese-/Schreibberechtigung. Welche Berechtigungen Ihnen erteilt werden, hängt von Ihrer Zugriffsebene und dem Objekt ab. 
  
Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt schreibgeschützt zu öffnen, wird MAPI_E_NOT_FOUND zurückgegeben. Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt mit Lese-/Schreibzugriff zu öffnen, wird der Profilabschnitt erstellt und der **IProfSect-Zeiger** zurückgegeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

