---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432835"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet eine alternative Möglichkeit zum Aufrufen der OLE-Methode **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameter

 _punk_
  
> [in] Zeiger auf eine Schnittstelle, die von der **IUnknown-Schnittstelle** abgeleitet ist, d. h. auf eine beliebige MAPI-Schnittstelle. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.
    
## <a name="remarks"></a>Hinweise

 **UlAddRef gibt** den von der **IUnknown::AddRef-Methode** zurückgegebenen Wert zurück, der der neue Wert der Referenzanzahl für die Schnittstelle ist. Der Wert ist ungleich Null. 
  
Weitere Informationen zu **IUnknown::AddRef** finden Sie unter [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  

