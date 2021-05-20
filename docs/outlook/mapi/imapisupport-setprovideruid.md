---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437539"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine [MAPIUID-Struktur,](mapiuid.md) die den Dienstanbieter eindeutig darstellt. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpProviderID_
  
> [in] Ein Zeiger auf die **MAPIUID-Struktur,** die das Adressbuch oder den Nachrichtenspeicheranbieter identifiziert. 
    
 _ulFlags_
  
> Reserviert; muss null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **MAPIUID-Struktur** wurde erfolgreich registriert. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::SetProviderUID-Methode** wird für Unterstützungsobjekte für Adressbuch- und Nachrichtenspeicheranbieter implementiert. Diese Anbieter rufen **SetProviderUID auf,** um einen eindeutigen Bezeichner zu registrieren, der in der **MAPIUID-Struktur** beschrieben ist, auf die _von lpProviderID verwiesen wird._ Anbieter enthalten diesen Bezeichner in alle von ihnen erstellten Eintragsbezeichner. 
  
MAPI verwendet die **MAPIUID-Struktur,** wenn ausgehende Nachrichten an den MAPI-Spooler gesendet werden und um den geeigneten Anbieter für die Verarbeitung von Clientanforderungen zu ermitteln. Wenn ein Client beispielsweise die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, untersucht MAPI den **MAPIUID-Teil** des Eintragsbezeichners, ordnet ihn dem Anbieter zu, der ihn an **SetProviderUID** übergeben hat, und ruft **openEntry** dieses Anbieters auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie SetProviderUID bei** der Anmeldung auf, um Ihre **MAPIUID-Struktur zu** registrieren. MAPI ermöglicht Adressbuch- und Nachrichtenspeicheranbietern die Registrierung mehrerer Bezeichner. Wenn Sie mehrere Aufrufe von **SetProviderUID** erstellen, wird dem Satz von **MAPIUID-Strukturen** des Anbieters immer die **MAPIUID-Struktur** hinzugefügt, auch wenn **die MAPIUID** ein Duplikat ist. **SetProviderUID** kann keine **MAPIUID entfernen.** 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

