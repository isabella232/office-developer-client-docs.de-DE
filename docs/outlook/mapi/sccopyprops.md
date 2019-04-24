---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351331"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert die durch ein Array von [SPropValue](spropvalue.md) -Strukturen definierten Eigenschaften in ein neues Ziel. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> in Die Anzahl der zu kopierenden Eigenschaften. 
    
 _rgprop_
  
> in Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die zu kopierenden Eigenschaften definieren. Der _rgprop_ -Parameter muss nicht auf den Anfang des Arrays zeigen, sondern auf den Anfang einer der **SPropValue** -Strukturen im Array. 
    
 _pvDst_
  
> in Zeiger auf die Anfangsposition im Speicher, auf die diese Funktion die Eigenschaften kopiert. 
    
 _PCB_
  
> Out Optionaler Zeiger auf die Größe des Speicherblocks, auf den durch den _pvDst_ -Parameter verwiesen wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Eigenschaften wurden erfolgreich kopiert.
    
MAPI_E_INVALID_PARAMETER
  
> Ein unbekannter Eigenschafts wurde gefunden.
    
## <a name="remarks"></a>Bemerkungen

Das neue Array und seine Daten befinden sich in einem Puffer, der mit einer einzelnen Zuordnung erstellt wurde, und die [ScRelocProps](screlocprops.md) -Funktion kann verwendet werden, um die Zeiger in den einzelnen [SPropValue](spropvalue.md) -Strukturen anzupassen. Vor dieser Einstellung sind die Zeiger gültig. 
  
 **ScCopyProps** behält die ursprüngliche Reihenfolge der Eigenschaften für das kopierte Eigenschaftenarray bei. 
  
Der _PCB_ -Parameter ist optional; Wenn Sie nicht NULL ist, wird Sie auf die Anzahl von Bytes festgelegt, die im Parameter _pvDst_ gespeichert sind. 
  
## <a name="see-also"></a>Siehe auch



[ScDupPropset](scduppropset.md)

