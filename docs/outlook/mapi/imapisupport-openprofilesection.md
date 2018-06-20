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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792395"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Betrifft**: Outlook 
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parameter

 _lpUid_
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die identifiziert den Profilabschnitt geöffnet werden soll. Übergeben NULL für den Parameter _LpUid_ wird des Anrufers Profilabschnitt geöffnet. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie im Profilabschnitt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt vollständig mit dem Anrufer zugegriffen werden. Wenn der Profilabschnitt nicht möglich ist, kann nachfolgende Objekt Anrufen ein Laufzeitfehler. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. In der Standardeinstellung Objekte werden als schreibgeschützt geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lppProfileObj_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt geöffnete.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, einen Profilabschnitt schreibgeschützt ändern oder auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Profilabschnitt _LpEntryID_übergebenen Eintrags-ID zugeordnet.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Reservierte oder nicht unterstützte Flags verwendet wurden und daher der Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenProfileSection** -Methode wird für alle Unterstützungsobjekte implementiert. Rufen **"OpenProfileSection"** zum Öffnen eines Abschnitts Profil und Abrufen eines Zeigers auf seine Implementierung **IProfSect** Dienstanbieter und Message-Dienste. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **"OpenProfileSection"** öffnet Profil Abschnitte mit Schreibschutz, es sei denn, Sie die Kennzeichen MAPI_MODIFY im _UlFlags_ -Parameter festgelegt und die Berechtigung ausreichend ist. Wenn Sie dieses Flag garantiert nicht Lese-/Schreibberechtigung. die Berechtigungen, die Sie erteilt werden, hängt von Ihrer Zugriffsebene und das Objekt ab. 
  
Wenn **"OpenProfileSection"** versucht, einen nicht vorhandenen Profilabschnitt im schreibgeschützten Modus zu öffnen, wird die MAPI_E_NOT_FOUND zurückgegeben. Wenn **"OpenProfileSection"** versucht, einen nicht vorhandenen Profilabschnitt mit Lese-/Schreibzugriff zu öffnen, Profilabschnitt erstellt und gibt den **IProfSect** Zeiger zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp: IUnknown](imapipropiunknown.md)
  
[IProfSect: IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

