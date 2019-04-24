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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330198"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden soll. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parameter

 _lpMuid_
  
> Ein Zeiger auf die neue **MAPIUID** -Struktur. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die neue **MAPIUID** -Struktur wurde erstellt. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: NewUID** -Methode wird für alle Support-Objekte implementiert. Dienstanbieter und Nachrichtendienste rufen **NewUID** auf, wenn Sie einen langfristigen eindeutigen Bezeichner generieren müssen. Ein Nachrichtenspeicher Anbieter kann beispielsweise **NewUID** aufrufen, um eine **MAPIUID** abzurufen, die in die **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht eingefügt werden soll.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwechseln Sie die **MAPIUID** -Struktur nicht, die Sie bei der Anmeldung mit den **MAPIUID** -Strukturen registrieren, die von der **NewUID** -Methode erstellt werden. Die **MAPIUID** -Struktur, die Sie beim Aufrufen der [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode registrieren, stellt das Adressbuch oder der Nachrichtenspeicher Anbieter in MAPI dar und dient zur Unterscheidung von Eintrags Bezeichnern, die von verschiedenen Anbietern erstellt werden. Diese **MAPIUID** -Struktur sollte hart codiert und nicht über einen Aufruf von **NewUID**abgerufen werden.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

