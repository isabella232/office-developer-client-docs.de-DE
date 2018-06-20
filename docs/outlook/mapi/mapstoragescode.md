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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793170"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Betrifft**: Outlook 
  
Maps SCODE zurück-Wert aus einem OLE-Speicher-Objekt in einen Typ HRESULT. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parameter

 _StgSCode_
  
> [in] MAPI SCODE zurück-Wert, aus einem OLE-Speicher-Objekt ein HRESULT-Wert zugeordnet werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert zurückgegeben.
    
MAPI_E_CALL_FAILED 
  
> Die Funktion kann einen übereinstimmenden Wert nicht finden.
    
## <a name="remarks"></a>Hinweise

MAPI bietet die **MapStorageSCode** -Funktion für die interne Verwendung von MAPI-Komponenten, die ihre Nachricht Implementierungen für die Nachricht DLL basieren soll. Da diese Komponenten OLE Remotespeicher selbst zu öffnen, müssen sie zuordnen Fehlerwerte für Probleme mit OLE-Speicher an ein HRESULT-Wert zurückgegeben werden. 
  
Weitere Informationen finden Sie unter [Strukturierte Storage](structured-storage-in-mapi.md). 
  

