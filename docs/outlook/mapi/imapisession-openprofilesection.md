---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568189"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die im Profilabschnitt identifiziert. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden. Übergeben von NULL bewirkt, dass den Parameter _LppProfSect_ auf einen Zeiger auf das Profilabschnitt Standardschnittstelle, **IProfSect**zurückzugeben.
    
 _ulFlags_
  
> [in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Benutzerprofildienst-Abschnitt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt an den aufrufenden Client vollständig verfügbar. Wenn der Profilabschnitt nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf ein Profilabschnitt, der nicht an den Anbieter gehört.
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. In der Standardeinstellung Profil Abschnitte mit Leseberechtigung geöffnet sind, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, Zugriff auf einen Profil für den Anrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Abschnitt angeforderten Profile ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::OpenProfileSection** -Methode öffnet eine Benutzerprofilabschnitt oder ein Objekt, das die **IProfSect** -Schnittstelle unterstützt. Profil Abschnitte dienen zum Lesen von Informationen aus und Schreiben von Informationen in das Sitzungsprofil. 
  
Sie können **"OpenProfileSection"** Profil Abschnitte öffnen, einzelne eigenen Dienstanbieter, es sei denn, Sie MAPI_FORCE_ACCESS im _UlFlags_ -Parameter angeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können mit Leseberechtigung Profile-Abschnitt öffnen, jedoch nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung geöffnet werden. Wenn ein anderer Client einen Profilabschnitt öffnen hat, dass Sie versuchen, die durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY öffnen, schlägt der Aufruf fehl MAPI_E_NO_ACCESS zurückgeben. 
  
Ein Vorgang zum schreibgeschützt öffnen schlägt fehl, wenn im Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY und eine nicht vorhandene **MAPIUID** Struktur im _LpUID_ -Parameter. Stellen Sie sicher, dass Sie MAPI_MODIFY angeben. Wenn Sie die _LpUID_ So zeigen Sie auf eine nicht vorhandene **MAPIUID** festgelegt, und Verwenden der Standardzugriffsmodus schreibgeschützten **"OpenProfileSection"** festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

