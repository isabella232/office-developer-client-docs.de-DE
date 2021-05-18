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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406997"
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
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::NewUID-Methode** wird für alle Supportobjekte implementiert. Dienstanbieter und Nachrichtendienste rufen **NewUID** auf, wenn sie einen langfristigen eindeutigen Bezeichner generieren müssen. Ein Nachrichtenspeicheranbieter kann beispielsweise **NewUID** aufrufen, um eine **MAPIUID** zu erhalten, die in der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht gespeichert werden soll.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwechseln Sie nicht die **MAPIUID-Struktur,** die Sie bei der Anmeldung registrieren, mit den **MAPIUID-Strukturen,** die die **NewUID-Methode** erstellt. Die **MAPIUID-Struktur,** die Sie beim Aufrufen der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) registrieren, stellt Ihren Adressbuch- oder Nachrichtenspeicheranbieter für MAPI dar und wird verwendet, um Eintragsbezeichner zu unterscheiden, die von verschiedenen Anbietern erstellt werden. Diese **MAPIUID-Struktur** sollte hart codiert sein und nicht über einen Aufruf von **NewUID erhalten werden.**
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

