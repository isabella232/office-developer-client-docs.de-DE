---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0ffa10ee6939ca46a5c6cab2c2d41e1facca5375
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625518"
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
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Wenn NULL übergeben wird, gibt der  _Parameter "lppProfSect"_ einen Zeiger auf die Standardschnittstelle des Profilabschnitts, **IProfSect,** zurück.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt für den aufrufenden Client vollständig verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf einen Profilabschnitt, der nicht zum Anbieter gehört.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wurde. 
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Profilabschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profilabschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::OpenProfileSection-Methode** öffnet einen Profilabschnitt oder ein Objekt, das die **IProfSect-Schnittstelle** unterstützt. Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet. 
  
Sie können **OpenProfileSection** nicht verwenden, um Profilabschnitte zu öffnen, die einzelne Dienstanbieter besitzen, es sei denn, Sie geben MAPI_FORCE_ACCESS im  _ulFlags-Parameter_ an. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen. Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY Flag aufrufen, schlägt der Aufruf fehl und gibt MAPI_E_NO_ACCESS zurück. 
  
Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY Flag und einer nicht vorhandenen **MAPIUID-Struktur** im  _lpUID-Parameter_ aufrufen. Achten Sie darauf, dass Sie MAPI_MODIFY angeben. Wenn Sie  _lpUID_ so festlegen, dass es auf eine nicht vorhandene **MAPIUID** verweist und **OpenProfileSection** so festgelegt ist, dass der Standardzugriffsmodus schreibgeschützt verwendet wird, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

