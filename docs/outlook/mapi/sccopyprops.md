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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411008"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert die durch ein Array von [SPropValue-Strukturen definierten Eigenschaften](spropvalue.md) in ein neues Ziel. 
  
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
  
> [in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die zu kopierenden Eigenschaften definieren. Der  _rgprop-Parameter_ muss nicht auf den Anfang des Arrays verweisen, sondern auf den Anfang einer **der SPropValue-Strukturen** im Array. 
    
 _pvDst_
  
> [in] Zeiger auf die Ausgangsposition im Arbeitsspeicher, in die diese Funktion die Eigenschaften kopiert. 
    
 _leiterplatte_
  
> [out] Optionaler Zeiger auf die Größe des Speicherblocks in Bytes, auf den der  _pvDst-Parameter_ verweist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Eigenschaften wurden erfolgreich kopiert.
    
MAPI_E_INVALID_PARAMETER
  
> Es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>Hinweise

Das neue Array und seine Daten befinden sich in einem Puffer, der mit einer einzigen Zuordnung erstellt wurde, und die [ScRelocProps-Funktion](screlocprops.md) kann verwendet werden, um die Zeiger in den einzelnen [SPropValue-Strukturen anzupassen.](spropvalue.md) Vor dieser Anpassung sind die Zeiger gültig. 
  
 **ScCopyProps** behält die ursprüngliche Eigenschaftsreihenfolge für das kopierte Eigenschaftenarray bei. 
  
Der  _#A0_ ist optional. Wenn er nicht NULL ist, wird er auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind. 
  
## <a name="see-also"></a>Siehe auch



[ScDupPropset](scduppropset.md)

