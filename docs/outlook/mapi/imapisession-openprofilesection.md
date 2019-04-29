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
  
Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück. 
  
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
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Profil Abschnitt identifiziert. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll. Durch das Übergeben von NULL wird der _lppProfSect_ -Parameter zum Zurückgeben eines Zeigers auf die Standardschnittstelle des Profil Abschnitts **IProfSect**.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Zugriff auf den Profil Abschnitt steuern. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe von **OpenProfileSection** , möglicherweise bevor der Profil Abschnitt vollständig für den aufrufenden Client verfügbar ist. Wenn der profile-Abschnitt nicht verfügbar ist, kann ein nachfolgendes aufrufen einen Fehler verursachen. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf einen Profil Abschnitt, der nicht zum Anbieter gehört.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Profilabschnitte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde. 
    
 _lppProfSect_
  
> Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profil Abschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Profil Abschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profil Abschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: OpenProfileSection** -Methode öffnet einen Profil Abschnitt oder ein Objekt, das die **IProfSect** -Schnittstelle unterstützt. Profilabschnitte dienen zum Lesen von Informationen und zum Schreiben von Informationen in das Sitzungsprofil. 
  
Sie können **OpenProfileSection** nicht verwenden, um Profilabschnitte zu öffnen, die einzelne Dienstanbieter besitzen, es sei denn, Sie geben MAPI_FORCE_ACCESS im _ulFlags_ -Parameter an. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profil Abschnitt mit Schreibschutz Berechtigung Öffnen, aber nur ein Client kann einen Profil Abschnitt mit Berechtigung zum Lesen/Schreiben öffnen. Wenn ein anderer Client einen Profil Abschnitt geöffnet hat, den Sie durch Aufrufen von **OpenProfileSection** mit dem MAPI_MODIFY-Flag-Satz öffnen, schlägt der Aufruf fehl, und es wird MAPI_E_NO_ACCESS zurückgegeben. 
  
Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profil Abschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flag und einer nicht vorhandenen **MAPIUID** -Struktur im _lpUID_ -Parameter aufrufen. Stellen Sie sicher, dass Sie MAPI_MODIFY angeben. Wenn Sie _lpUID_ so festlegen, dass auf ein nicht vorhandenes **MAPIUID** und **OpenProfileSection** auf den Standardzugriffs Modus schreibgeschützt festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

