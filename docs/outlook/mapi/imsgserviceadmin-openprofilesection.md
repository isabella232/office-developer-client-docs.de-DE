---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2aa1a876af8773db22af8f35c79ee8328362356a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604875"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Profilabschnitt identifiziert. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Wenn NULL übergeben wird, wird ein Zeiger auf die Standardschnittstelle im  _Parameter "lppProfSect"_ zurückgegeben. Die Standardschnittstelle für einen Profilabschnitt ist **IProfSect.**
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt für den aufrufenden Client vollständig verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigung erteilt wurde. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch diejenigen, die im Besitz einzelner Dienstanbieter sind.
    
 _lppProfSect_
  
> [out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Profilabschnitt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf einen Profilabschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Der angeforderte Profilabschnitt ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::OpenProfileSection-Methode** öffnet einen Profilabschnitt, ein Objekt, das die [IProfSect-Schnittstelle](iprofsectimapiprop.md) unterstützt. Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet. 
  
 **OpenProfileSection** kann nur verwendet werden, wenn MAPI_FORCE_ACCESS verwendet wird, um Profilabschnitte zu öffnen, die im Besitz einzelner Dienstanbieter sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen. Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** aufrufen, wobei das MAPI_MODIFY Flag festgelegt ist, schlägt der Aufruf fehl und gibt MAPI_E_NO_ACCESS zurück. 
  
Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY Flag und einer nicht vorhandenen [MAPIUID-Struktur](mapiuid.md) im  _lpUID-Parameter_ aufrufen. Achten Sie darauf, MAPI_MODIFY anzugeben. Wenn Sie  _lpUID_ so festlegen, dass es auf eine nicht vorhandene **MAPIUID** verweist und **OpenProfileSection** so festgelegt ist, dass der Standardzugriffsmodus schreibgeschützt verwendet wird, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::OpenProfileSection-Methode,** um einen Profilabschnitt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

