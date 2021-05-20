---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437112"
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll. Das Übergeben von NULL führt dazu, dass ein Zeiger auf die Standardschnittstelle im  _lppProfSect-Parameter zurückgegeben_ wird. Die Standardschnittstelle für einen Profilabschnitt ist **IProfSect**.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt vollständig für den aufrufenden Client verfügbar ist. Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler zur Folge haben. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
MAPI_FORCE_ACCESS
  
> Ermöglicht den Zugriff auf alle Profilabschnitte, auch die, die im Besitz einzelner Dienstanbieter sind.
    
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

Die **IMsgServiceAdmin::OpenProfileSection-Methode** öffnet einen Profilabschnitt, ein Objekt, das die [IProfSect-Schnittstelle](iprofsectimapiprop.md) unterstützt. Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet. 
  
 **OpenProfileSection** kann nicht zum Öffnen von Profilabschnitten verwendet werden, die im Besitz einzelner Dienstanbieter sind, es sei denn, MAPI_FORCE_ACCESS verwendet wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen. Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flagsatz aufrufen, wird beim Aufruf ein Fehler ausgeführt, und MAPI_E_NO_ACCESS. 
  
Ein schreibgeschützter offener Vorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist. 
  
Sie können einen Profilabschnitt erstellen, indem **Sie OpenProfileSection** mit dem flag MAPI_MODIFY und einer nicht vorhandenen [MAPIUID-Struktur](mapiuid.md) im  _lpUID-Parameter_ aufrufen. Stellen Sie sicher, dass Sie MAPI_MODIFY. Wenn Sie  _lpUID_ so festlegen, dass sie auf eine nicht vorhandene **MAPIUID** zeigt und **OpenProfileSection** auf den Standardzugriffsmodus schreibgeschützt festgelegt ist, wird beim Aufruf ein Fehler MAPI_E_NOT_FOUND. 
  
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

