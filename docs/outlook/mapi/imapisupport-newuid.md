---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09a9a9f4e118ee1f52f4ddfb69d59f66523cb24d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584360"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue [MAPIUID-Struktur,](mapiuid.md) die als eindeutiger Bezeichner verwendet werden soll. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameter

 _lpMuid_
  
> Ein Zeiger auf die neue **MAPIUID-Struktur.** 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die neue **MAPIUID-Struktur** wurde erstellt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::NewUID-Methode** wird für alle Unterstützungsobjekte implementiert. Dienstanbieter und Nachrichtendienste rufen **NewUID** immer dann auf, wenn sie einen langfristigen eindeutigen Bezeichner generieren müssen. Beispielsweise kann ein Nachrichtenspeicheranbieter **NewUID** aufrufen, um eine **MAPIUID** abzurufen, die in die **eigenschaft PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) einer neu erstellten Nachricht eingefügt wird.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwechseln Sie die **MAPIUID-Struktur,** die Sie zur Anmeldezeit registrieren, nicht mit den **MAPIUID-Strukturen,** die von der **NewUID-Methode** erstellt werden. Die **MAPIUID-Struktur,** die Sie registrieren, wenn Sie die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) aufrufen, stellt Das Adressbuch oder den Nachrichtenspeicheranbieter für die MAPI dar und wird verwendet, um Eintragsbezeichner zu unterscheiden, die von verschiedenen Anbietern erstellt werden. Diese **MAPIUID-Struktur** sollte hartcodiert sein und nicht über einen Aufruf von **NewUID** abgerufen werden.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

