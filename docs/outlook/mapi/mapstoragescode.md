---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 078c05c0f3355e633ab7edaed577c99b4c2a33b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595707"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Karten einen SCODE-Rückgabewert von einem OLE-Speicherobjekt an einen HRESULT-Typ zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parameter

 _StgSCode_
  
> [in] MAPI-SCODE-Rückgabewert aus einem OLE-Speicherobjekt, das einem HRESULT-Wert zugeordnet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert zurückgegeben.
    
MAPI_E_CALL_FAILED 
  
> Die Funktion kann keinen übereinstimmenden Wert finden.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI stellt die **MapStorageSCode-Funktion** für die interne Verwendung von MAPI-Komponenten bereit, die ihre Nachrichtenimplementierungen auf der Nachrichten-DLL basieren. Da diese Komponenten den OLE-Speicher selbst öffnen, müssen sie zurückgegebene Fehlerwerte für Probleme mit DEM OLE-Speicher einem HRESULT-Wert zuordnen können. 
  
Weitere Informationen finden Sie unter [Strukturierte Storage](structured-storage-in-mapi.md). 
  

