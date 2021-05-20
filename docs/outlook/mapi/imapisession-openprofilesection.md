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
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439919"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück. 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Profilabschnitt identifiziert. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Durch Übergeben von NULL gibt  _der lppProfSect-Parameter_ einen Zeiger auf die Standardschnittstelle des Profilabschnitts zurück, **IProfSect**.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt vollständig für den aufrufenden Client verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf einen Profilabschnitt, der nicht zum Anbieter gehört.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Profilabschnitt zu zugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profilabschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::OpenProfileSection-Methode** öffnet einen Profilabschnitt oder ein Objekt, das die **IProfSect-Schnittstelle** unterstützt. Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet. 
  
Sie können **OpenProfileSection** nicht zum Öffnen von Profilabschnitten verwenden, die einzelne Dienstanbieter besitzen, es sei denn, Sie geben MAPI_FORCE_ACCESS  _ulFlags-Parameter_ an. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen. Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flagsatz aufrufen, wird beim Aufruf ein Fehler ausgeführt, und MAPI_E_NO_ACCESS. 
  
Ein schreibgeschützter offener Vorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, indem **Sie OpenProfileSection** mit dem flag MAPI_MODIFY und einer nicht vorhandenen **MAPIUID-Struktur** im  _lpUID-Parameter_ aufrufen. Stellen Sie sicher, dass Sie MAPI_MODIFY. Wenn Sie  _lpUID_ so festlegen, dass sie auf eine nicht vorhandene **MAPIUID** zeigt und **OpenProfileSection** auf den Standardzugriffsmodus schreibgeschützt festgelegt ist, wird beim Aufruf ein Fehler MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

