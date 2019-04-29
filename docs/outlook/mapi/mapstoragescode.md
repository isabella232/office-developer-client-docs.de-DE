---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416524"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordnet einen SCODE-Rückgabewert aus einem OLE-Speicherobjekt einem HRESULT-Typ zu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parameter

 _StgSCode_
  
> in MAPI-SCODE-Rückgabewert aus einem OLE-Speicherobjekt, das einem HRESULT-Wert zugeordnet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert zurückgegeben.
    
MAPI_E_CALL_FAILED 
  
> Die Funktion kann keinen übereinstimmenden Wert finden.
    
## <a name="remarks"></a>Bemerkungen

MAPI stellt die **MapStorageSCode** -Funktion für die interne Verwendung von MAPI-Komponenten bereit, die Ihre Nachrichten Implementierungen auf die Nachrichten-DLL basieren. Da diese Komponenten OLE-Speicher selbst öffnen, müssen Sie in der Lage sein, für Probleme mit OLE-Speicher zurückgegebene Fehlerwerte einem HRESULT-Wert zuzuordnen. 
  
Weitere Informationen finden Sie unter [Structured Storage](structured-storage-in-mapi.md). 
  

