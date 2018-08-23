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
ms.openlocfilehash: df842e633f1586d6d77441126d51b2ce44ec3beb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589070"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Registriert eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter eindeutig darstellt. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpProviderID_
  
> [in] Ein Zeiger auf die **MAPIUID** -Struktur, die den Anbieter Address Book oder einer Nachricht Store identifiziert. 
    
 _ulFlags_
  
> Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Struktur **MAPIUID** wurde erfolgreich registriert. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::SetProviderUID** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert. Diese Anbieter Aufrufen **SetProviderUID** zum Registrieren eines eindeutigen Bezeichners beschrieben in der **MAPIUID** -Struktur, die mit _LpProviderID_gezeigt wird. Anbieter: Dieser Bezeichner in allen den Eintrag-IDs, die sie erstellen. 
  
MAPI verwendet die **MAPIUID** -Struktur beim Senden ausgehender Nachrichten die Warteschlange MAPI und den entsprechenden Anbieter für die Verarbeitung von Clientanforderungen bestimmen. Beispiel: Wenn ein Client die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode aufruft, MAPI untersucht den **MAPIUID** Teil des Eintrags-ID, ordnet sie den Anbieter, der sie **SetProviderUID**übergeben, und ruft diesen Anbieter **OpenEntry** . 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SetProviderUID** bei der Anmeldung die **MAPIUID** -Struktur zu registrieren. MAPI ermöglicht Adresse Adressbuch und Nachricht Speicheranbieter mehrere Bezeichner registriert. Wenn Sie mehrere Aufrufe von **SetProviderUID**vornehmen, hinzugefügt immer die **MAPIUID** -Struktur des Anbieters Satz von **MAPIUID** -Strukturen, auch wenn die **MAPIUID** ein Duplikat ist. **SetProviderUID** kann keiner **MAPIUID**entfernt werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

