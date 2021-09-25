---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f4b69c62f78805e93f28db73691830515997fa3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586789"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert die durch ein Array von [SPropValue-Strukturen](spropvalue.md) definierten Eigenschaften an ein neues Ziel. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der zu kopierenden Eigenschaften. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die zu kopierenden Eigenschaften definieren. Der  _rgprop-Parameter_ muss nicht auf den Anfang des Arrays zeigen, sondern auf den Anfang einer der **SPropValue-Strukturen** im Array. 
    
 _pvDst_
  
> [in] Zeiger auf die Anfangsposition im Speicher, in die diese Funktion die Eigenschaften kopiert. 
    
 _Pcb_
  
> [out] Optionaler Zeiger auf die Größe des Speicherblocks in Byte, auf den der  _PvDst-Parameter_ verweist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Eigenschaften wurden erfolgreich kopiert.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das neue Array und seine Daten befinden sich in einem Puffer, der mit einer einzelnen Zuordnung erstellt wurde, und die [ScRelocProps-Funktion](screlocprops.md) kann verwendet werden, um die Zeiger in den einzelnen [SPropValue-Strukturen](spropvalue.md) anzupassen. Vor dieser Anpassung sind die Zeiger gültig. 
  
 **ScCopyProps** behält die ursprüngliche Eigenschaftenreihenfolge für das kopierte Eigenschaftenarray bei. 
  
Der  _Parameter "parameters"_ ist optional; wenn sie nicht NULL ist, wird sie auf die Anzahl von Bytes festgelegt, die im  _pvDst-Parameter_ gespeichert sind. 
  
## <a name="see-also"></a>Siehe auch



[ScDupPropset](scduppropset.md)

