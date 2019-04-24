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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326313"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter eindeutig darstellt. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpProviderID_
  
> in Ein Zeiger auf die **MAPIUID** -Struktur, die das Adressbuch oder den Nachrichtenspeicher Anbieter identifiziert. 
    
 _ulFlags_
  
> Reserviert muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **MAPIUID** -Struktur wurde erfolgreich registriert. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: SetProviderUID** -Methode wird für Support Objekte des Adressbuchs und des Nachrichtenspeichers implementiert. Diese Anbieter rufen **SetProviderUID** auf, um einen eindeutigen Bezeichner zu registrieren, der in der **MAPIUID** -Struktur beschrieben ist, auf die von _lpProviderID_verwiesen wird. Anbieter schließen diesen Bezeichner in alle Eintrags-IDs ein, die Sie erstellen. 
  
MAPI verwendet die **MAPIUID** -Struktur beim Senden ausgehender Nachrichten an den MAPI-Spooler und zum Bestimmen des geeigneten Anbieters für die Verarbeitung von Clientanforderungen. Wenn ein Client beispielsweise die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, untersucht MAPI **den MAPIUID** -Teil der Eintrags-ID, ordnet ihn dem Anbieter zu, der ihn an **SetProviderUID**übergeben hat, und ruft den OpenEntry- **Eintrag** des Anbieters auf. . 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SetProviderUID** bei der Anmeldung auf, um Ihre **MAPIUID** -Struktur zu registrieren. MAPI ermöglicht es Adressbuch-und Nachrichtenspeicher Anbietern, mehrere Bezeichner zu registrieren. Wenn Sie mehrere Aufrufe an **SetProviderUID**durchführen, wird die **MAPIUID** -Struktur immer dem Satz von **MAPIUID** -Strukturen des Anbieters hinzugefügt, auch wenn die **MAPIUID** ein Duplikat ist. **SetProviderUID** kann keine **MAPIUID**entfernen. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

