---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 270e1486c7c33ea8655914bf9fe51e9f335fc707
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575743"
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
  
> Reserviert; muss Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **MAPIUID-Struktur** wurde erfolgreich registriert. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::SetProviderUID-Methode** ist für Adressbuch- und Nachrichtenspeicheranbieter-Supportobjekte implementiert. Diese Anbieter rufen **SetProviderUID** auf, um einen eindeutigen Bezeichner zu registrieren, der in der **MAPIUID-Struktur** beschrieben ist, auf die von  _lpProviderID_ verwiesen wird. Anbieter schließen diesen Bezeichner in alle Eintragsbezeichner ein, die sie erstellen. 
  
DIE MAPI verwendet die **MAPIUID-Struktur,** wenn ausgehende Nachrichten an den MAPI-Spooler gesendet werden, und um den geeigneten Anbieter für die Verarbeitung von Clientanforderungen zu ermitteln. Wenn ein Client beispielsweise die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, überprüft MAPI den **MAPIUID-Teil** des Eintragsbezeichners, ordnet ihn dem Anbieter zu, der sie an **SetProviderUID** übergeben hat, und ruft **openEntry** dieses Anbieters auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **"SetProviderUID"** zur Anmeldezeit auf, um Ihre **MAPIUID-Struktur** zu registrieren. MAPI ermöglicht Es Adressbuch- und Nachrichtenspeicheranbietern, mehrere Bezeichner zu registrieren. Wenn Sie mehrere **Aufrufe von SetProviderUID** ausführen, wird immer die **MAPIUID-Struktur** zu den **MAPIUID-Strukturen** des Anbieters hinzugefügt, auch wenn die **MAPIUID** ein Duplikat ist. **SetProviderUID** kann **mapiuid** nicht entfernen. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

