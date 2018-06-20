---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792386"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Betrifft**: Outlook 
  
Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameter

 _lpMuid_
  
> Ein Zeiger auf die neue **MAPIUID** -Struktur. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die neue **MAPIUID** Struktur erstellt wurde. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::NewUID** -Methode wird für alle Unterstützungsobjekte implementiert. Dienstanbieter und Message-Dienste aufrufen **NewUID** , wenn sie benötigen, um eine langfristige eindeutige ID zu generieren. Eine Nachricht Speicheranbieter, zum Beispiel, **NewUID** zum Abrufen einer **MAPIUID** in die **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht platzieren aufgerufen werden kann.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwechseln Sie nicht die **MAPIUID** -Struktur, die Sie bei der Anmeldung mit den Strukturen **MAPIUID** registrieren, die die **NewUID** -Methode erstellt. Die **MAPIUID** -Struktur, die Sie registrieren, wenn Sie die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode aufrufen, stellt Adressbuch oder Nachricht MAPI-Speicheranbieter und wird verwendet, um die Eintrags-IDs zu unterscheiden, die verschiedene Anbieter erstellen. Diese Struktur **MAPIUID** sollte hartcodierte und nicht durch einen Aufruf von **NewUID**abgerufen werden.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

