---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586067"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen Dienstanbietern vergangen sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameter

 _eMethod_
  
> [in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen. 
    
 _Erster_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Alle Parameter sind ungültig. 
    
MAPI_E_CALL_FAILED 
  
> Eine oder mehrere der Parameter sind ungültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **ValidateParameters** wurde durch das Makro [ValidateParms](validateparms.md) ersetzt. **ValidateParameters** funktioniert nicht ordnungsgemäß auf RISC-Plattformen und wird nun auf diese zu kompilieren verhindert. Immer noch kompiliert und auf Intel-Plattformen ordnungsgemäß funktioniert, aber **ValidateParms** wird auf allen Plattformen empfohlen. 
  

